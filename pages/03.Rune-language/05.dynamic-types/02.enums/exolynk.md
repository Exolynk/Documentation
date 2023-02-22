---
title: Enums
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Enums

Rune has support for *enumerations*. These allow you to define a type with zero
or more *variants*, where each variant can hold a distinct set of data.

In a dynamic programming language enums might not seem quite as useful, but it's
important for Rune to support them to have a level of feature parity with Rust.

Even so, in this section we'll explore some cases where enums are useful.

## The `Option` enum

Rune has native support for `Option`, the same enum available in Rust that
allows you to represent data that can either be present with `Option::Some`, or
absent with `Option::None`.

```rust
use std::iter::range;

fn count_numbers(limit) {
    let limit = limit.unwrap_or(10);

    for n in range(0, limit) {
        println!("Count: {}", n);
    }
}

pub fn main() {
    println("First count!");
    count_numbers(None);

    println("Second count!");
    count_numbers(Some(2));
}
```

```bash
$> cargo run --bin rune -- run scripts/book/enums/count_numbers.rn
First count!
Count: 0
Count: 1
Count: 2
Count: 3
Count: 4
Count: 5
Count: 6
Count: 7
Count: 8
Count: 9
Second count!
Count: 0
Count: 1
== () (9.0745ms)
```

Using an `Option` allows us to easily model the scenario where we have an
optional function parameter, with a default fallback value.

In the next section we'll be looking into a control flow construct which gives
`Option` superpowers.

The try operator.
