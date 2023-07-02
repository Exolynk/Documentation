---
title: 'Color'
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
### Color
Color value type (HTML formats as defined here: https://docs.exolynk.com/language-api/base-api/color#color)

[I'm a relative reference to a repository file](../blob/master/LICENSE)

<a href="https://docs.exolynk.com/language-api/base-api/color#color" target="_blank">Color Format</a>
<a href="../language-api/base-api/color#color" target="_blank">Color Format</a>
<a href="../../language-api/base-api/color#color" target="_blank">Color Format</a>
<a href="../../../language-api/base-api/color#color" target="_blank">Color Format</a>
<a href="../../../../language-api/base-api/color#color" target="_blank">Color Format</a>

### UI Example
![Color](color.gif?resize=426&classes=left)

### UI Layout Example
````html
<variable ident="color_name" access="write" />
````

### Attributes
[ui-accordion independent=true open=none]

[ui-accordion-item title=Variable attributes]

##### Variable attributes
> | attributes      | data type           | Description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | Required    | Bool                  | mandatory to fill out (Yes or No)  |
> | Access    | Selection               | Access right `change`, `hide`, `read`, `write`  |
> | Default Value    | <a href="https://docs.exolynk.com/language-api/base-api/color#color" target="_blank">Color Format</a>       | color which is field in per default  |

[/ui-accordion-item]

[ui-accordion-item title=Layout attributes]

##### Layout attributes (html tags)
> | attributes      | data type           | Description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `access`    | String                  | front end access right `change`, `hide`, `read`, `write`  |


[/ui-accordion-item]
[/ui-accordion]