---
title: Vectors
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Vectors

A vector is a native data structure of Rune which is a dynamic list of values. A
vector isn't typed, and can store *any* Rune values.

```rust
pub fn main() {
    let values = ["Hello", 42];

    println!("{}", values[0]);
    println!("{}", values.1); // items in vectors can be accessed like tuple fields.

    for v in values {
        println!("{}", v);
    }
}
```

```bash
$> cargo run --bin rune -- run scripts/book/vectors/vectors.rn
Hello
42
Hello
42
== () (5.0674ms)
```

As you can see, you can iterate over a vector because it implements the iterator
protocol. It is also possible to create and use an iterator manually using
`Vec::iter`, giving you more control over it.

```rust
pub fn main() {
    let values = ["Hello", 42];

    for v in values.iter().rev() {
        println!("{}", v);
    }
}
```

```bash
$> cargo run --bin rune -- run scripts/book/vectors/vectors_rev.rn
42
Hello
== () (2.9116ms)
```