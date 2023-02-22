---
title: Dynamic Types
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Dynamic types

Dynamic types are types which can be defined and used solely within a Rune
script. They provide the ability to structure data and associate functions with
it.

The following is a quick example of a `struct`:

```rust
struct Person {
    name,
}

impl Person {
    fn greet(self) {
        println!("Greetings from {}, and good luck with this section!", self.name);
    }
}

pub fn main() {
    let person = Person {
        name: "John-John Tedro",
    };

    person.greet();
}
```

```bash
$> cargo run --bin rune -- run scripts/book/dynamic_types/greeting.rn
Greetings from John-John Tedro, and good luck with this section!
== () (2.7585ms)
```
