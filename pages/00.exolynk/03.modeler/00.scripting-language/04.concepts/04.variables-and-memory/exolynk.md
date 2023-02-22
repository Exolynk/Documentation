---
title: Variables and memory
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Variables and memory

Variables in Rune are defined using the `let` keyword. In contrast to Rust, all
variables in Rune are mutable and can be changed at any time.

```rust
pub fn main() {
    let x = 5;
    println!("The value of x is: {}", x);
    x = 6;
    println!("The value of x is: {}", x);
}
```

```text
$> cargo run --bin rune -- run scripts/book/variables/variables.rn
The value of x is: 5
The value of x is: 6
```

Rune is a memory safe language. Regardless of what you write in a Rune script,
we maintain the same memory safety guarantees as safe Rust. This is accomplished
through reference counting.

[Unless a value is `Copy`](../../05.built-in-types/01.primitives-and-references/primitives.md), they are reference counted and
can be used at multiple locations. This means that they have *shared ownership*.
Every variable that points to that value therefore points to *the same instance*
of that value. You can think of every nontrivial value being automatically
wrapped in an `Rc<RefCell<T>>` if that helps you out.

>>>>> This is not exactly what's going on. If you're interested to learn more, Rune
>>>>> uses a container called [`Shared<T>`](https://docs.rs/shared/) which is *like* an `Rc<RefCell<T>>`, but
>>>>> has a few more tricks.

We can see how this works by sharing and mutating one object across two
variables:

```rust
pub fn main() {
    let object = #{field: 1};
    let object2 = object;
    println!("{}", object.field);
    object2.field = 2;

    // Note: we changed `object2`, but read out `object`
    println!("{}", object.field);
}
```

```text
$> cargo run --bin rune -- run scripts/book/variables/shared_ownership.rn
1
2
== () (913.4µs)
```

This can cause issues if we call an external function which expects to take
ownership of its arguments. We say that functions like these *move* their
argument, and if we try to use a variable which has been moved an error will be
raised in the virtual machine.

>>>>> Note: Below we use the `drop` function, which is a built-in function that will take its argument and free it.

```rust
pub fn main() {
    let object = #{field: 1};
    let object2 = object;
    println!("field: {}", object.field);
    drop(object2);
    println!("field: {}", object.field);
}
```

```text
$> cargo run --bin rune -- run scripts/book/variables/take_argument.rn
field: 1
== ! (cannot read, value is moved (at 14)) (469µs)
error: virtual machine error
  ┌─ scripts/book/variables/take_argument.rn:6:27
  │
6 │     println!("field: {}", object.field);
  │                           ^^^^^^^^^^^^ cannot read, value is moved
```

If you need to, you can test if a variable is still accessible for reading with
`is_readable`, and for writing with `is_writable`. These are both imported in
the prelude. An object which is writable is also *movable*, and can be provided
to functions which need to move the value, like `drop`.

```rust
pub fn main() {
    let object = #{field: 1};
    let object2 = object;
    println!("field: {}", object.field);
    drop(object2);

    if is_readable(object) {
        println!("field: {}", object.field);
    } else {
        println!("object is no longer readable 😢");
    }
}
```

```text
$> cargo run --bin rune -- run scripts/book/variables/is_readable.rn
field: 1
object is no longer readable 😢
== () (943.8µs)
```

[`Shared<T>`]: https://docs.rs/rune/0/rune/struct.Shared.html
