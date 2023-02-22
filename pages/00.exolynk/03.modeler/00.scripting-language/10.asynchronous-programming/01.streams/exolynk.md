---
title: Streams
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Streams

Streams are the asynchronous version of [Generators](../../08.generators/exolynk.md).

They have almost identical `next` and `resume` functions, but each must be used
with `.await`, and we are now allowed to use asynchronous functions inside of
the generator.

```rust
async fn send_requests(list) {
    let client = http::Client::new();

    let do_request = async |url| {
        let response = client.get(url).await?;
        Ok(response.send().await?.status())
    };

    for url in list {
        yield do_request(url).await;
    }
}

pub async fn main() {
    let requests = send_requests([
        "https://google.com",
        "https://amazon.com",
    ]);

    while let Some(status) = requests.next().await.transpose()? {
        println!("{}", status);
    }
}
```

```bash
$> cargo run --bin rune -- run scripts/book/streams/basic_stream.rn
200 OK
200 OK
== () (754.3946ms)
```
