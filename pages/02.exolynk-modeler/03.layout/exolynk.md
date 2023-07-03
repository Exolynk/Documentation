---
title: Layout
taxonomy:
    category: docs
markdown.extra: true
process:
    twig: false
    markdown: true
---

[TOC]

<br>
<br>
<br>
<br>

## Layout
The Layouter is used to configure the front end form for the models and its records. A simple html syntax is used without head and body tags.

### Structure Elements

#### Tabs

```html
<tab name="Tab_Name" active="true">
    ...
</tab>
```

#### Collapse Panel

```html
<data name="Properties">
    <variable ident="ident_name" />
</data>
```

### OOTB Elements

#### Calendar Start & End Date

```html
<variable ident="calendar_start" access="write" />
<variable ident="calendar_end" access="write" />
```