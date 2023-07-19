---
title: 'Signature'
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
### Signature
A Signature object to handsign a document or a report. Uses the <a href="https://www.openstreetmap.org/" target="_blank">OpenStreetMap</a> API to locate the current position of the device to make the signature legally valid.

### UI Example
![Signature 1](signature_1.gif?resize=800&classes=left)

![Signature 2](signature_2.gif?resize=800&classes=left)

### UI Layout Example
````html
<variable ident="signature_name" access="write" />
````

### Attributes
[ui-accordion independent=true open=none]

[ui-accordion-item title=Variable attributes]

##### Variable attributes
> | attributes     | data type           | Description                                                           |
> |----------------|---------------------|-----------------------------------------------------------------------|
> | Required       | Bool                | mandatory to fill out (Yes or No)  |
> | Access         | Selection           | Access right `change`, `hide`, `read`, `write`  |

[/ui-accordion-item]

[ui-accordion-item title=Layout attributes]

##### Layout attributes (html tags)
> | attributes      | data type           | Description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `access`    | String                  | front end access right `change`, `hide`, `read`, `write`  |


[/ui-accordion-item]
[/ui-accordion]