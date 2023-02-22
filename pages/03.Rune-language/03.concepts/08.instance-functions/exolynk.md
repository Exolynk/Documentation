---
title: Instance functions
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Instance functions

Instance functions are functions that are associated to a specific type of
variable. When called they take the form `value.foo()`, where the *instance*
is the first part `value`. And the *instance function* is `foo()`.

These are a bit special in Rune. Since Rune is a dynamic programming language we
can't tell at compile time which instance any specific `value` can be. So
instance functions must be looked up at runtime.

```rust
struct Foo;

impl Foo {
    fn new() {
        Foo
    }
}

pub fn main() {
    let foo = Foo::new();
    foo.bar();
}
```

```bash
$> cargo run --bin rune -- run scripts/book/instance_functions/missing_instance_fn.rn
error: virtual machine error
   ┌─ scripts/book/instance_functions/missing_instance_fn.rn:11:5
   │
11 │     foo.bar();
   │     ^^^^^^^^^ missing instance function `0xfb67fa086988a22d` for `type(0xc153807c3ddc98d7)``
```

>>>>> The error is currently a bit nondescript. But in the future we will be
>>>>> able to provide better diagnostics by adding debug information.

What you're seeing above are type and function hashes. These uniquely identify
the item in the virtual machine and is the result of a deterministic computation
based on its item. So the hash for the item `Foo::new` will always be the same.