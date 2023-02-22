---
title: Structs
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Structs

Structs are like objects, except that they have a predefined structure with a
set of keys that are known at compile time and guaranteed to be defined.

Structs can also, like most types, have an `impl` block associated with them
which creates instance functions that you can call on an instance of that
struct.

```rust
struct User {
    username,
    active,
}

impl User {
    fn set_active(self, active) {
        self.active = active;
    }

    fn describe(self) {
        if self.active {
            println(`${self.username} is active`);
        } else {
            println(`${self.username} is inactive`);
        }
    }
}

pub fn main() {
    let user = User {
        username: "setbac",
        active: false,
    };

    user.describe();
    user.set_active(true);
    user.describe();
}
```

```bash
$> cargo run --bin rune -- run scripts/book/structs/user_database.rn
setbac is inactive
setbac is active
== () (6.2095ms)
```

Structs can also be pattern matched, like most types.

But since the fields of a struct are known at compile time, the compiler can
ensure that you're only using fields which are defined.

```rust
struct User {
    username,
    active,
}

impl User {
    fn describe(self) {
        match self {
            User { username: "setbac", .. } => {
                println("Yep, it's setbac.");
            }
            User { username, .. } => {
                println(`Other user: ${username}.`);
            }
        }
    }
}

pub fn main() {
    let user = User {
        username: "setbac",
        active: false,
    };

    user.describe();
    user.username = "newt";
    user.describe();
}
```

```bash
$> cargo run --bin rune -- run scripts/book/structs/struct_matching.rn
Yep, it's setbac.
Other user: newt.
== () (1.0652ms)
```
