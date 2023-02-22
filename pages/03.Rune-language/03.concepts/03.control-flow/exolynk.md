---
title: Control Flow
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Control Flow

Rune supports a number of control flow expressions. We will be dedicating this
section to describe the most common ones.

## `return` expression

In the previous section we talked about functions. And one of the primary things
a function does is return things. The `return` expression allows for returning
from the current function. If used without an argument, the function will return
a unit `()`.

The last statement in a function is known as an *implicit return*, and will be
what the function returns by default unless a `return` is specified.

```rust
fn foo(n) {
    if n < 1 {
        return "less than one";
    }

    "something else"
}

pub fn main() {
    println!("{}", foo(0)); // => outputs: "less than one"
    println!("{}", foo(10)); // => outputs: "something else"
}
```

```bash
$> cargo run --bin rune -- run scripts/book/control_flow/numbers_game.rn
less than one
something else
== () (3.8608ms)
```

## `if` expressions

If expressions allow you to provide a condition with one or more code branches.
If the condition is `true`, the provided block of code will run.

```rust
pub fn main() {
    let number = 3;

    if number < 5 {
        println!("The number is smaller than 5");
    }
}
```

```bash
$> cargo run --bin rune -- run scripts/book/control_flow/conditional.rn
The number *is* smaller than 5
== () (5.108ms)
```

Optionally, we can add another branch under `else`, which will execute in case
the condition is false.

```rust
pub fn main() {
    let number = 3;

    if number < 5 {
        println!("the number is smaller than 5");
    } else {
        println!("the number is 5 or bigger");
    }
}
```

```bash
$> cargo run --bin rune -- run scripts/book/control_flow/conditional_else.rn
the number is smaller than 5
== () (196.1µs)
```

We can also add an arbitrary number of `else if` branches, which allow us to
specify many different conditions.

```rust
pub fn main() {
    let number = 3;

    if number < 5 {
        println!("the number is smaller than 5");
    } else if number == 5 {
        println!("the number is exactly 5");
    } else {
        println!("the number is bigger than 5");
    }
}
```

```bash
$> cargo run --bin rune -- run scripts/book/control_flow/conditional_else_ifs.rn
the number is smaller than 5
== () (227.9µs)
```

Do note however that if you have *many* conditions, it might be cleaner to use
a `match`.

This will be covered in a later section, but here is a sneak peek:

```rust
pub fn main() {
    let number = 3;

    match number {
        n if n < 5 => {
            println!("the number is smaller than 5");
        }
        5 => {
            println!("the number is exactly 5");
        }
        n => {
            println!("the number is bigger than 5");
        }
    }
}
```

```bash
$> cargo run --bin rune -- run scripts/book/control_flow/first_match.rn
the number is smaller than 5
== () (124.2µs)
```
