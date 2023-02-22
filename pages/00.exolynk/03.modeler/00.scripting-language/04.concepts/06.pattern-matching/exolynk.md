---
title: Pattern matching
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Pattern matching

In this section we will be discussing *Pattern Matching*.

Pattern matching is a flexible mechanism that allows for validating the
structure and type of the argument, while also destructuring it to give easy
access to what you need.

Below are some examples of its common uses to match on branch conditions:

```rust
fn match_input(n) {
    match n {
        1 => println!("The number one."),
        n if n is int => println!("Another number: {}.", n),
        [1, 2, n, ..] => println!("A vector starting with one and two, followed by {}.", n),
        "one" => println!("One, but this time as a string."),
        _ => println!("Something else. Can I go eat now?"),
    }
}

pub fn main() {
    match_input(1);
    match_input(2);
    match_input([1, 2, 42, 84]);
    match_input("one");
    match_input(#{field: 42});
}
```

```bash
$> cargo run --bin rune -- run scripts/book/pattern_matching/big_match.rn
The number one.
Another number: 2.
A vector starting with one and two, followed by 42.
One, but this time as a string.
Something else. Can I go eat now?
== () (5.691ms)
```

We will be covering each of these variants in detail in the coming sections.

## Patterns

Things that can be matched over are called *patterns*, and there's a fairly
large number of them. In this section we'll try to document the most common
ones.

Patterns that can be matched over are the following:

* A unit, simply `()`.
* A boolean value, like `true` or `false`.
* A byte, like `b'a'` or `b'\x10'`.
* A character, like `'a'` or `'あ'`.
* An integer, like `42`.
* A string, like `"Steven Universe"`.
* A vector, like the numbers `[1, _, ..]`, or simply the empty vector `[]`. The
  values in the vectors are patterns themselves.
* A tuple, like `("Steven Universe", _, 42)`. The values in the tuple are
  patterns themselves.
* An object, like the numbers `{"name": "Steven Universe", "age": _}`, or the
  empty `{}`. The values in the object are patterns themselves.

Structs can be matched over by prefixing the match with their name:
* A unit struct: `Foo`.
* A tuple struct: `Foo(1, _)`.
* An object struct: `Foo { bar: 1, .. }`.

Similarly, variants in an enum can be matched over as well in the same way:
* A unit variant: `Foo::Variant`.
* A tuple variant: `Foo::Variant(1, _)`.
* An object variant: `Foo::Variant { bar: 1, .. }`.

Patterns can be almost *any* combination of the above. Even `{"items": ["Sword",
"Bow", "Axe"]}` is a pattern that can be matched over.

Anything that qualifies as a collection can have `..` as a suffix to match the
case that there are extra fields or values which are not covered in the pattern.
This is called a *rest pattern*.

```rust
pub fn main() {
    let value = #{ a: 0, b: 1 };

    let matched = match value {
        // this doesn't match, because a pattern without a rest pattern in it
        // must match exactly.
        #{ a } => false,
        // this matches, because it only requires `a` to be present.
        #{ a, .. } => true,
    };

    assert!(matched, "rest pattern matched");
}
```

```bash
$> cargo run --bin rune -- run scripts/book/pattern_matching/rest_pattern.rn
== () (89.8µs)
```

## Binding and ignoring

In a pattern, every value can be replaced with a *binding* or an *ignore
pattern*. The ignore pattern is a single underscore `_`, which informs Rune that
it should ignore that value, causing it to match unconditionally regardless of
what it is.

```rust
fn test_ignore(vector) {
    match vector {
        [_, 2] => println("Second item in vector is 2."),
    }
}

pub fn main() {
    test_ignore([1, 2]);
}
```

```bash
$> cargo run --bin rune -- run scripts/book/pattern_matching/ignore.rn
Second item in vector is 2.
== () (281.3µs)
```

In contrast to ignoring, we can also *bind* the value to a variable that is then
in scope of the match arm. This will also match the value unconditionally, but
give us access to it in the match arm.

```rust
fn test_ignore(vector) {
    match vector {
        [_, b] => println!("Second item in vector is {}.", b),
    }
}

pub fn main() {
    test_ignore([1, 2]);
}
```

```bash
$> cargo run --bin rune -- run scripts/book/pattern_matching/bind.rn
Second item in vector is 2.
== () (6.25ms)
```

Here are some more examples:

* `[_, a, b]` which will ignore the first value in the vector, but then bind the
  second and third as `a` and `b`.
* `{"name": name}` will bind the value `name` out of the specified object.

```rust
fn describe_car(car) {
    match car {
        #{"make": year, ..} if year < 1950 => "What, where did you get that?",
        #{"model": "Ford", "make": year, ..} if year >= 2000 => "Pretty fast!",
        _ => "Can't tell 😞",
    }
}

pub fn main() {
    println!("{}", describe_car(#{"model": "Ford", "make": 2000}));
    println!("{}", describe_car(#{"model": "Honda", "make": 1980}));
    println!("{}", describe_car(#{"model": "Volvo", "make": 1910}));
}
```

```bash
$> cargo run --bin rune -- run scripts/book/pattern_matching/fast_cars.rn
Pretty fast!
Can't tell 😞
What, where did you get that?
== () (5.3533ms)
```
