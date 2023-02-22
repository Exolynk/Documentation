---
title: Try Operator
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Try operator

The try operator (`?`) is a control flow operator which causes a function to
return early in case the value being tried over has a certain value.

For `Option`, this causes the function to return if it has the `Option::None`
variant.

```rust
fn checked_div_mod(a, b) {
    let div = a.checked_div(b)?;
    Some((div, a % b))
}

pub fn main() {
    if let Some((div, m)) = checked_div_mod(5, 2) {
        println!("Result: {}, {}", div, m);
    }

    if let Some((div, m)) = checked_div_mod(5, 0) {
        println!("Result: {}, {}", div, m);
    }
}
```

```bash
$> cargo run --bin rune -- run scripts/book/try_operator/basic_try.rn
Result: 2, 1
== () (7.4912ms)
```
