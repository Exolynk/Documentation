# Tuples

Tuples in Rune are fixed-size sequences of values. Similarly to a vector, tuples
can contain any sequence of values. But there's no way to change the size of a
tuple.

```rune
{{#include ../../scripts/book/tuples/tuple_masquerade.rn}}
```

```text
$> cargo run --bin rune -- run scripts/book/tuples/tuple_masquerade.rn
("Now", "You", "See", "Me")
("Now", "You", "Don\'t", "!")
== () (38.3136ms)
```

The following is a simple example of a function returning a tuple:

```rune
{{#include ../../scripts/book/tuples/basic_tuples.rn}}
```

```text
$> cargo run --bin rune -- run scripts/book/tuples/basic_tuples.rn
(1, "test")
== () (387.6µs)
```

Tuples can also be pattern matched:

```rune
{{#include ../../scripts/book/tuples/tuple_patterns.rn}}
```

```text
$> cargo run --bin rune -- run scripts/book/tuples/tuple_patterns.rn
"the first part was a number:"
1
== () (7.7892ms)
```