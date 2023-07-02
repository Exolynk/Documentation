---
title: 'List'
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
### List
The List element can be used to list one data type per rows. All avilable data types can be used to list

### UI Example (List String)
![List-String](list-string.gif?resize=800&classes=left)


### UI Layout Example
````html
<variable ident="list_name" access="write" />
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
> | Data type    | Selection         | Data type for list `Integer`, `Float`, `Bool`, `String`, `Selection`, `Reference`, `Ident`, `DateTime`, `Language`, `Color`, `Version`  |

[/ui-accordion-item]

[ui-accordion-item title=Layout attributes]

##### Layout attributes (html tags)
> | attributes      | data type           | Description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `access`    | String                  | front end access right `change`, `hide`, `read`, `write`  |


[/ui-accordion-item]
[/ui-accordion]