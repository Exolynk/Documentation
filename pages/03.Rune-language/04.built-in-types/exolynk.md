---
title: Rune types
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Rune types

Types in Rune are identified uniquely by their *item*. An item path is a
scope-separated identifier, like `std::float`. This particular item identifies
a type.

These items can be used to perform basic type checking using the `is` and `is
not` operations, like this:

```rust
pub fn main() {
    assert!(() is unit, "units should be units");
    assert!(true is bool, "bools should be bools");
    assert!('a' is char, "chars should be chars");
    assert!(b'a' is byte, "bytes should be bytes");
    assert!(42 is int, "integers should be integers");
    assert!(42.1 is float, "floats should be floats");
    assert!("hello" is String, "strings should be strings");
    assert!("x" is not char, "strings are not chars");
    assert!(#{"hello": "world"} is Object, "objects should be objects");
    assert!(["hello", "world"] is Vec, "vectors should be vectors");
}
```

```bash
$> cargo run --bin rune -- run scripts/book/types/types.rn
== () (120µs)
```

Conversely, the type check would fail if you're providing a value which is not
of that type.

```rust
pub fn main() {
    assert!(["hello", "world"] is String, "vectors should be strings");
}
```

```bash
$> cargo run --bin rune -- run scripts/book/types/bad_type_check.rn
== ! (panicked `assertion failed: vectors should be strings` (at 12)) (133.3µs)
error: virtual machine error
  ┌─ scripts/book/types/bad_type_check.rn:2:5
  │
2 │     assert!(["hello", "world"] is String, "vectors should be strings");
  │     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ panicked `assertion failed: vectors should be strings`
```

This gives us insight at runtime which type is which, and allows Rune scripts to
make decisions depending on what type a value has.

```rust
fn dynamic_type(n) {
    if n is String {
        "n is a String"
    } else if n is Vec {
        "n is a vector"
    } else {
        "n is unknown"
    }
}

pub fn main() {
    println!("{}", dynamic_type("Hello"));
    println!("{}", dynamic_type([1, 2, 3, 4]));
    println!("{}", dynamic_type(42));
}
```

```bash
$> cargo run --bin rune -- run scripts/book/types/type_check.rn
n is a String
n is a vector
n is unknown
== () (1.0544ms)
```

A tighter way to accomplish this would be by using pattern matching, a mechanism
especially suited for many conditional branches. Especially when the branches
are different types or variants in an enum.

```rust
fn dynamic_type(n) {
    match n {
        n if n is String => "n is a String",
        n if n is Vec => "n is a vector",
        _ => "n is unknown",
    }
}

pub fn main() {
    println!("{}", dynamic_type("Hello"));
    println!("{}", dynamic_type([1, 2, 3, 4]));
    println!("{}", dynamic_type(42));
}
```

```bash
$> cargo run --bin rune -- run scripts/book/types/type_check_patterns.rn
n is a String
n is a vector
n is unknown
== () (1.0341ms)
```
