---
title: 'Getting started with Rune'
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Getting Started

The first thing you need to learn about in Rune is the `dbg` function. This is used to "debug" values provided to it in order to understand them. Anything can be provided to it, and it will do its best to describe it.

```rust
pub fn main() {
    let a = [1, 2, 3];
    let b = '今';
    let closure = || println("Hello");

    dbg(a);
    dbg(b);
    dbg(function);
    dbg(drop);
    dbg(closure);
}

fn function() {
    42
}
```
>>>>> by convention Rune uses files ending in .rn.

```bash
$> cargo run --bin rune -- run scripts/book/getting_started/dbg.rn
[1, 2, 3]
'今'
dynamic function (at: 0x17)
native function (0x2959efc1c70)
Type(0x9aa62663879132fb)
== () (8.3679ms)
```

The default `dbg` implementation outputs information on its arguments to stdout. But its exact behavior can differ depending on how the environment is configured. When Rune is embedded into a larger application it might for example be more suitable to output to a log file.

Rune also provides `print!` and `println!` macros which can be used to format directly to stdout, but these cannot be relied on to be present to the same degree as `dbg`. However for our purposes we will be using `rune-cli`, which has all of these modules installed. This is also what was used to run the above code.

So for a more formal introduction, here is the official Rune `"Hello World"`:

```rust
pub fn main() {
    println!("Hello World");
}
```

```bash
$> cargo run --bin rune -- run scripts/book/getting_started/hello_world.rn
Hello World
== () (1.0864ms)
```

At the end of the script's output, you see this rather odd looking line:

```bash
== () (1.0864ms)
```

This simply means that the script evaluated to a unit, or a `()`.
And that the script took `1.0864` milliseconds to run.

>>>>> Any function that doesn't have a return value returns a unit.

So now you know how to run Rune scripts. Well done! Let's move on to the next chapter.

<br>

## Rune Playground

>>>>> For quick testing the the Rune Language we recommend to use this Playground: [Rune Playground](https://rune-rs.github.io/play)

<iframe src="https://rune-rs.github.io/play/" style="border:0px #ffffff none;" name="Rune Playground" scrolling="no" frameborder="0" marginheight="0px" marginwidth="0px" height="800px" width="1000px" allowfullscreen></iframe>
