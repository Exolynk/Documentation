---
title: 'Selection'
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
### Selection
The Selection list or dropdown can be used to select one or multiple options.
More details here: <a href="../../language-api/base-api/selection#selection" target="_blank">Base API - Selection</a>

>>>>>> UX Considerations: Use dropdowns for numerous or similar options. If the number of options is more than 6–7 you should consider putting them in the dropdown (selection instead of e.g. bool) as users anyway will not be able to keep all of them in mind.

### UI Example
![Selection](selection.gif?resize=800&classes=left)

### UI Layout Example
````html
<variable ident="selection_name" access="write" />
````

### Attributes
[ui-accordion independent=true open=none]

[ui-accordion-item title=Variable attributes]

##### Variable attributes
> | attributes      | data type           | Description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | Required    | Bool                  | mandatory to fill out (Yes or No)  |
> | Access    | Selection               | Access right `change`, `hide`, `read`, `write`  |
> | Default Value    | Selection         | element which is selected per default  |
> | Selection Elements   | String         | elements which can be selected  |

[/ui-accordion-item]

[ui-accordion-item title=Layout attributes]

##### Layout attributes (html tags)
> | attributes      | data type           | Description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `access`    | String                  | front end access right `change`, `hide`, `read`, `write`  |


[/ui-accordion-item]
[/ui-accordion]