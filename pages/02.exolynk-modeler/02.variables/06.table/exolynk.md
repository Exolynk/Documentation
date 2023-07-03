---
title: 'Table'
taxonomy:
    category:
        - docs
process:
    markdown: true
    twig: false
---

[TOC]

<br><br><br><br>

------------------------------------------------------------------------------------------
### Table
The Table can be used to combine many different data types in a table form. E.g. for a reporting sheet with Amount (Integer), Description (String), and Customer (Reference to Customer Object).

### UI Example (Table String)
![Table-String](table-string.gif?resize=800&classes=left)

### UI Example (3 columns Table with Integer, String and Reference)
Data types in tables can be combined and defined per column:

![Table-Mixed](table-mixed.gif?resize=800&classes=left)

### UI Layout Example
````html
<variable ident="table_name" access="write" />
````

### Attributes
[ui-accordion independent=true open=none]

[ui-accordion-item title=Variable attributes]

##### Variable attributes
> | attributes      | data type           | Description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | Required    | Bool                  | mandatory to fill out (Yes or No)  |
> | Access    | Selection               | Access right `change`, `hide`, `read`, `write`  |
> | Default Value    | String         | value which is field in per default  |
> | Data type    | Selection         | Data type for list columns `Integer`, `Float`, `Bool`, `String`, `Selection`, `Reference`, `Ident`, `DateTime`, `Language`, `Color`, `Version`  |

[/ui-accordion-item]

[ui-accordion-item title=Layout attributes]

##### Layout attributes (html tags)
> | attributes      | data type           | Description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `access`    | String                  | front end access right `change`, `hide`, `read`, `write`  |


[/ui-accordion-item]
[/ui-accordion]