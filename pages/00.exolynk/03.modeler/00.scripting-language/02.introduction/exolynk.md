---
title: Introduction
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Introduction

Rune is a dynamic programming language that is easily embeddable and has support for an exciting set of language features.

## Asynchronous first

Rune prioritized excellent support for async with support for async functions, closures, blocks, and generators. And native support for select, a popular control flow mechanism for asynchronous code.

```rust
use std::future;

struct Timeout;

const SITE = "https://httpstat.us";

async fn request(timeout) {
    let request = http::get(`${SITE}/200?sleep=${timeout}`);
    let timeout = time::delay_for(time::Duration::from_secs(1));

    let result = select {
        res = request => res,
        _ = timeout => Err(Timeout),
    }?;

    let text = result.text().await?;
    Ok(text)
}

pub async fn main() {
    let result = future::join((request(0), request(1500))).await;
    dbg(result);
}
```

Asynchronous programming using select

## const evaluation

Rune has support for constant evaluation using the const keyword. Which can perform complex work at compile time.

```rust
const BASE = 10;
const LIMIT = 0b1 << 10;

const VALUE = {
    let timeout = BASE;

    while timeout < LIMIT {
        timeout = timeout * 2;
    }

    `https://httpstat.us/200?timeout=${timeout}`
};

pub fn main() {
    dbg(VALUE, LIMIT);
}
```
```VALUE``` and ```LIMIT``` is calculated once, reducing the work needed at runtime

<br><br>