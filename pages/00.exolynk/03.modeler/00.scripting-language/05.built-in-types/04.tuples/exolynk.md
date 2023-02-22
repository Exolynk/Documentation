---
title: Tuples
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Tuples

Tuples in Rune are fixed-size sequences of values. Similarly to a vector, tuples
can contain any sequence of values. But there's no way to change the size of a
tuple.

```rust
pub fn main() {
    let values = ("Now", "You", "See", "Me");
    dbg(values);

    values.2 = "Don't";
    values.3 = "!";
    dbg(values);
}
```

```bash
$> cargo run --bin rune -- run scripts/book/tuples/tuple_masquerade.rn
("Now", "You", "See", "Me")
("Now", "You", "Don\'t", "!")
== () (38.3136ms)
```

The following is a simple example of a function returning a tuple:

```rust
fn foo() {
    (1, "test")
}

pub fn main() {
    dbg(foo());
}
```

```bash
$> cargo run --bin rune -- run scripts/book/tuples/basic_tuples.rn
(1, "test")
== () (387.6µs)
```

Tuples can also be pattern matched:

```rust
pub fn main() {
    match ("test", 1) {
        ("test", n) => {
            dbg("the first part was a number:", n);
        }
        _ => {
            dbg("matched something we did not understand");
        }
    }
}
```

```bash
$> cargo run --bin rune -- run scripts/book/tuples/tuple_patterns.rn
"the first part was a number:"
1
== () (7.7892ms)
```
