---
title: Functions
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Functions

One of the most common things in all of programming are functions. These are
stored procedures which take a arguments, do some work, and then return.
Functions are used because they encapsulate what they do so that the programmer
only needs to concern itself with the protocol of the function.

What does it do? What kind of arguments does it take? The alternative would be
to copy the code around and that wouldn't be very modular. Functions instead
provide a modular piece of code that can be called and re-used. Over and over
again.

## `fn` keyword

In Rune, functions are declared with the `fn` keyword. You've already seen one
which is used in every example, `main`. This is not a special function, but is
simply what the Rune cli looks for when deciding what to execute.

```rust
pub fn main() {
    println("Hello World");
}
```

```bash
$> cargo run --bin rune -- run scripts/book/functions/main_function.rn
Hello World
== () (277.8µs)
```

In Rune, you don't have to specify the return type of a function. Given that
Rune is a dynamic programming language, this allows a function to return
anything, even completely distinct types.

```rust
fn foo(condition) {
    if condition {
        "Hello"
    } else {
        1
    }
}

pub fn main() {
    println!("{}", foo(true));
    println!("{}", foo(false));
}
```

```bash
$> cargo run --bin rune -- run scripts/book/functions/return_value.rn
Hello
1
== () (8.437ms)
```

Depending on who you talk to, this is either the best thing since sliced bread
or quite scary. It allows for a larger ability to express a program, but at the
same time it can be harder to reason on what your program will do.
