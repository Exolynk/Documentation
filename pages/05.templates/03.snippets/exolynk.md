---
title: 'Snippets'
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

<br><br><br><br><br>

## Code Snippets

A collection of some helpfull code snippets to faster integrate workflows.

[ui-accordion independent=true open=0]
[ui-accordion-item title=Status\040Workflow\040and\040Service]

### Set Status

#### Set Status Workflow

Simple Status Workflow with user inbox notification and higlight color.

```rust
pub fn show() {
    let record = webapp::get_record()?;
    if record.status.to_string() == "status_0" {
        return true;
    }
    else if record.status.to_string() == "status_1" {
        return true;
    }
    return false;
}

pub async fn main() {
    let record = webapp::get_record()?;
    webapp::rpc_call("model","set_status", ["status_2", "#2B7D2B"]).await?; //highlight color green
    // set in inbox
    let usr = record.get_value("assigned_user_1")?.get_reference()?.to_string();
    dbg(usr);
    dbg(record.uuid);
    webapp::rpc_call("model", "set_user_inbox", [usr, record.uuid]).await?;
    Ok(())
}

pub async fn test() {
    //let x = show();
    //println!("Show {}", x);
    main().await?;
}
```

#### Set Status Service

```rust
pub async fn main(ident, color) {
    dbg(ident);
    dbg(color);
    let status = Ident::new(ident);
    let record = server::get_record()?;
    server::db::update_record_value(record.uuid, Ident::new("status"), Value::Ident(status)).await?;
    server::db::update_record_value(record.uuid, Ident::new("highlight_color"), Value::Color(Color::new(color))).await?;
    Ok(true)
}

pub async fn test() {
    main("new","").await?;
}
```

#### Set Inbox Service

```rust
pub async fn main(user, rec_uuid) {
    dbg(user);
    dbg(rec_uuid);
    server::db::add_inbox(user, rec_uuid).await?;
    Ok(true)
}

pub async fn test() {
}
```


[/ui-accordion-item]

[ui-accordion-item title=Set\040User\040Password]

### Set User Password

Workflow and Service code to set user passwords.

#### Set User Password Workflow

Icon: ```two-keys```

```rust
pub fn show() {
    true
}

pub async fn main() {
    let vars = [Variable::new(Ident::new("password"), Value::String(""))?];
    let result = webapp::ui::popup("Reset Password", "", vars).await?;
    if result.0 == false {
        return;
    }
    let new_pw = result.1;
    let new_pw = new_pw[0].value.get_string()?;
    dbg(new_pw);
    webapp::rpc_call("model", "set_user_password_service", new_pw).await?;
}

pub async fn test() {
    main().await?;
}
```

#### Set User Password Service

Icon: ```two-keys```

```rust
pub async fn main(inp) {
    // todo - check for user rights - API still missing
    dbg(inp);
    let user=server::get_record()?.uuid;
    server::db::reset_password(user, inp).await?;
}

pub async fn test() {
}
```

[/ui-accordion-item]

[ui-accordion-item title=Add\040Favorite]

### Add Favorite

#### Add Favorite Workflow

Icon: ```favorite```

```rust

```

#### Add Favorite Service

Icon: ```favorite```

```rust

```
[/ui-accordion-item]

[ui-accordion-item title=Remove\040Favorite]

### Remove Favorite

#### Remove Favorite Workflow

Icon: ```unfavorite```

```rust

```

#### Remove Favorite Service

Icon: ```unfavorite```

```rust

```

[/ui-accordion-item]
[/ui-accordion]