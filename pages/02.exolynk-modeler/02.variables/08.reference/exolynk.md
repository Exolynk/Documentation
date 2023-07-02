---
title: 'Reference'
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
### Reference
The Selection tybe can be used to refer to records of the same or another model.

More details here: <a href="../../language-api/base-api/reference#reference" target="_blank">Base API - Reference</a>

>>>>>> UX Considerations: Please restrict the available reference objects to the model from which objects can be refered (e.g. that only clients are available to select for the client field and not user to improve the usability).

### UI Example
![Reference](reference.gif?resize=800&classes=left)

### UI Layout Example
````html
<variable ident="reference_name" access="write" />
````

### Attributes
[ui-accordion independent=true open=none]

[ui-accordion-item title=Variable attributes]

##### Variable attributes
> | attributes      | data type           | Description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | Required    | Bool                  | mandatory to fill out (Yes or No)  |
> | Access    | Selection               | Access right `change`, `hide`, `read`, `write`  |
> | Default Value    | Reference         | Reference object which is refered per default  |
> | Restricted record type   | Selection         | objects which can be refered `Models`, `All records`,`Record Type` |

[/ui-accordion-item]

[ui-accordion-item title=Layout attributes]

##### Layout attributes (html tags)
> | attributes      | data type           | Description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `access`    | String                  | front end access right `change`, `hide`, `read`, `write`  |


[/ui-accordion-item]
[/ui-accordion]