---
title: 'Language'
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
### Multi-Language Text Field
A language is an object with holds text translated in multiple languages.
More details here: <a href="../../language-api/base-api/language#language" target="_blank">Base API - Language</a>

### UI Example
![Language](language.gif?resize=800&classes=left)

### UI Layout Example
````html
<variable ident="language_name" access="write" />
````

### Attributes
[ui-accordion independent=true open=none]

[ui-accordion-item title=Variable attributes]

##### Variable attributes
> | attributes      | data type           | Description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | Required    | Bool                  | mandatory to fill out (Yes or No)  |
> | Access    | Selection               | Access right `change`, `hide`, `read`, `write`  |
> | Default Value    | String        | value which is field in per default  |

[/ui-accordion-item]

[ui-accordion-item title=Layout attributes]

##### Layout attributes (html tags)
> | attributes      | data type           | Description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `access`    | String                  | front end access right `change`, `hide`, `read`, `write`  |


[/ui-accordion-item]
[/ui-accordion]