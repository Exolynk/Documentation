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
A variable wich stores a color code.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Color::new(String)\040->\040Settings</code>]

##### Description
Create a new Color object from the given string.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String                  | The color code in hex, rgb or as name  |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Settings                | A Settings object |

[/ui-accordion-item]

[ui-accordion-item title=<code>Color::as_string(Self)\040->\040String</code>]

##### Description
Returns the color as string.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Color            | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | String                  | Color as string |

[/ui-accordion-item]
