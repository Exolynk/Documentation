---
title: 'DateTime'
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
### DateTime
Date and Type in the format yyyy-MM-dd, HH:mm:ss with date/time picker.

>>> If no default value is given the current date and time will be set if date/time picker is opened.

>>>>> For the Calendar function (DateTime from - until) please use the OOTB Calendar function from the layout. More details here: <a href="../../exolynk-modeler/layout#calendar-start-end-date" target="_blank">Layout - Calendar Start & End Date</a>

### UI Example
![DateTime](date-time.gif?resize=800&classes=left)

### UI Layout Example
````html
<variable ident="datetime_name" access="write" />
````

### Attributes
[ui-accordion independent=true open=none]

[ui-accordion-item title=Variable attributes]

##### Variable attributes
> | attributes      | data type           | Description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | Required    | Bool                  | mandatory to fill out (Yes or No)  |
> | Access    | Selection               | Access right `change`, `hide`, `read`, `write`  |
> | Default Value    | DateTime format        | value which is field in per default in format yyyy-MM-dd, HH:mm:ss |

[/ui-accordion-item]

[ui-accordion-item title=Layout attributes]

##### Layout attributes (html tags)
> | attributes      | data type           | Description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `access`    | String                  | front end access right `change`, `hide`, `read`, `write`  |


[/ui-accordion-item]
[/ui-accordion]