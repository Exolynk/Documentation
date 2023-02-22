---
title: Objects
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

# Objects

Objects are anonymous maps, which support defining and using arbitrary string
keys.

```rust
pub fn main() {
    let values = #{};
    values["first"] = "bar";
    values["second"] = 42;

    dbg(values["first"]);
    dbg(values.second); // items be accessed like struct fields.

    if let Some(key) = values.get("not a key") {
        dbg(key);
    } else {
        println("key did not exist");
    }

    for entry in values {
        dbg(entry);
    }
}
```

```bash
$> cargo run --bin rune -- run scripts/book/objects/objects.rn
"bar"
42
key did not exist
("second", 42)
("first", "bar")
== () (3.3527ms)
```

These are useful because they allow their data to be specified dynamically,
which is exactly the same use case as storing unknown JSON.

One of the biggest motivations for Rune to have anonymous objects is so that
we can natively handle data with unknown structure.

```rust
async fn get_commits(repo, limit) {
    let limit = limit.unwrap_or(10);

    let client = http::Client::new();
    let request = client.get(`https://api.github.com/repos/${repo}/commits`).await?;
    let response = request.header("User-Agent", "Rune").send().await?;
    let text = response.text().await?;
    let json = json::from_string(text)?;

    let commits = json.iter().take(limit).map(|e| e.sha).collect::<Vec>();
    Ok(commits)
}

pub async fn main() {
    for commit in get_commits("rune-rs/rune", Some(5)).await? {
        println!("{}", commit);
    }
}
```

```bash
$> cargo run --bin rune -- run scripts/book/objects/json.rn
9c4bdaf194410d8b2f5d7f9f52eb3e64709d3414
06419f2580e7a18838f483321055fc06c0d75c4c
cba225dad143779a0a9543cfb05cde9710083af5
15133745237c014ff8bae53d8ff8f3c137c732c7
39ac97ab4ebe26118e807eb91c7656ab95b1fcac
3f6310eeeaca22d0373cc11d8b34d346bd12a364
== () (331.3324ms)
```
