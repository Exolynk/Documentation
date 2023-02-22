# Vectors

A vector is a native data structure of Rune which is a dynamic list of values. A
vector isn't typed, and can store *any* Rune values.

```rune
{{#include ../../scripts/book/vectors/vectors.rn}}
```

```text
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

```rune
{{#include ../../scripts/book/vectors/vectors_rev.rn}}
```

```text
$> cargo run --bin rune -- run scripts/book/vectors/vectors_rev.rn
42
Hello
== () (2.9116ms)
```