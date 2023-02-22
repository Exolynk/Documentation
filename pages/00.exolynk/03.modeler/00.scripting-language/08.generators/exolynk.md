---
title: Generators
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Generators

Generators are a convenient method for constructing functions which are capable
of suspending themselves and their state.

The simplest use case for generators is to create a kind of iterator, whose
state is stored in the generator function.

With this, we can create a fairly efficient generator to build fibonacci
numbers.

```rust
fn fib() {
    let a = 0;
    let b = 1;

    loop {
        yield a;
        let c = a + b;
        a = b;
        b = c;
    }
}

pub fn main() {
    let g = fib();

    while let Some(n) = g.next() {
        println!("{}", n);

        if n > 100 {
            break;
        }
    }
}
```

```bash
$> cargo run --bin rune -- run scripts/book/generators/fib_generator.rn
0
1
1
2
3
5
8
13
21
34
55
89
144
== () (14.9441ms)
```

## Advanced generators with `GeneratorState`

Generators internally are a bit more complex than that.
The `next` function simply slates over some of that complexity to make simple
things easier to do.

The first thing to know is that `yield` itself can actually *produce* a value,
allowing the calling procedure to send values to the generator.

```rust
fn printer() {
    loop {
        let out = yield;
        println!("{:?}", out);
    }
}

pub fn main() {
    let printer = printer();
    printer.resume(1);
    printer.resume("John");
    printer.resume((1, 2, 3));
}
```

```bash
$> cargo run --bin rune -- run scripts/book/generators/send_values.rn
"John"
(1, 2, 3)
== () (883.2µs)
```

But wait, what happened to the first value we sent, `1`?

Well, generators don't run immediately, they need to be "warmed up" by calling
resume once.
At that point it runs the block prior to the first yield, we can see this by
instrumenting our code a little.

```rust
fn printer() {
    loop {
        println("waiting for value...");
        let out = yield;
        println!("{:?}", out);
    }
}

pub fn main() {
    let printer = printer();

    println("firing off the printer...");
    printer.resume(());
    println("ready to go!");

    printer.resume("John");
    printer.resume((1, 2, 3));
}
```

```bash
$> cargo run --bin rune -- run scripts/book/generators/bootup.rn
firing off the printer...
waiting for value...
ready to go!
"John"
waiting for value...
(1, 2, 3)
waiting for value...
== () (8.8014ms)
```

Ok, so we understand how to *send* values into a generator.
But how do we *receive* them?

This adds a bit of complexity, since we need to pull out `GeneratorState`.
This enum has two variants: `Yielded` and `Complete`, and represents all the
possible states a generator can suspend itself into.

```rust
fn print_once() {
    let out = yield 1;
    println!("{:?}", out);
    2
}

pub fn main() {
    let printer = print_once();
    dbg(printer.resume(()));
    dbg(printer.resume("John"));
}
```

```bash
$> cargo run --bin rune -- run scripts/book/generators/states.rn
Yielded(1)
"John"
Complete(2)
== () (712.7µs)
```

After the first call to resume, we see that the generator produced `Yielded(1)`.
This corresponds to the `yield 1` statement in the generator.

The second value we get is `Complete(2)`.
This corresponds to the *return value* of the generator.

Trying to resume the generator after this will cause the virtual machine to
error.

```rust
fn print_once() {
    yield 1
}

pub fn main() {
    let printer = print_once();
    dbg(printer);
    dbg(printer.resume(()));
    dbg(printer.resume("John"));
    dbg(printer);
    dbg(printer.resume(()));
}
```

```bash
$> cargo run --bin rune -- run scripts/book/generators/error.rn
Generator { completed: false }
Yielded(1)
Complete("John")
Generator { completed: true }
error: virtual machine error
   ┌─ scripts/book/generators/error.rn:11:9
   │
11 │     dbg(printer.resume(()));
   │         ^^^^^^^^^^^^^^^^^^ cannot resume a generator that has completed
```
