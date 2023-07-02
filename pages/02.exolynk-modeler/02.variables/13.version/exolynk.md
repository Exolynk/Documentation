---
title: 'Version'
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
### Version
A version object. Right now it only allows nubered version (e.g. 0, 1, 2, 3, ...) in future more version formats are planned. More details here: <a href="../../language-api/base-api/version#version" target="_blank">Base API Version</a>

### UI Example
![Version](version.gif?resize=800&classes=left)

### UI Layout Example
````html
<variable ident="version_name" access="write" />
````

### Attributes
[ui-accordion independent=true open=none]

[ui-accordion-item title=Variable attributes]

##### Variable attributes
> | attributes      | data type           | Description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | Required    | Bool                  | mandatory to fill out (Yes or No)  |
> | Access    | Selection               | Access right `change`, `hide`, `read`, `write`  |
> | Default Value    | Integer   | version which is field in per default  |

[/ui-accordion-item]

[ui-accordion-item title=Layout attributes]

##### Layout attributes (html tags)
> | attributes      | data type           | Description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `access`    | String                  | front end access right `change`, `hide`, `read`, `write`  |


[/ui-accordion-item]
[/ui-accordion]