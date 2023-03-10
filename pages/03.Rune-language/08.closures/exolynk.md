---
title: Closures
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Closures

We've gone over functions before, and while incredibly useful there's a few more
tricks worth mentioning.

We'll also be talking about closures, an anonymous function with the ability to
*close over* its environment, allowing the function to use and manipulate things
from its environment.

## Function pointers

Every function can be converted into a function pointer simply by referencing
its name without calling it.

This allows for some really neat tricks, like passing in a function which
represents the operation you want another function to use.

```rust
fn do_thing(op) {
    op(1, 2)
}

fn add(a, b) {
    a + b
}

fn sub(a, b) {
    a - b
}

pub fn main() {
    println!("{}", do_thing(add));
    println!("{}", do_thing(sub));
}
```

```bash
$> cargo run --bin rune -- run scripts/book/closures/function_pointers.rn
Result: 3
Result: -1
== () (5.4354ms)
```

## Closures

Closures are anonymous functions which closes over their environment.
This means that they capture any variables used inside of the closure, allowing
them to be used when the function is being called.

```rust
fn work(op) {
    op(1, 2)
}

pub fn main() {
    let n = 1;
    println!("Result: {}", work(|a, b| n + a + b));
    println!("Result: {}", work(|a, b| n + a * b));
}
```

```bash
$> cargo run --bin rune -- run scripts/book/closures/basic_closure.rn
Result: 4
Result: 3
== () (5.4354ms)
```

>>>>> Closures which do not capture their environment are *identical* in
>>>>> representation to a function.
