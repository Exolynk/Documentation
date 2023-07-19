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
[/ui-accordion]

##### Supported color codes
Following html color code types are allowed:

**Names:** ```red``` <br>
**HEX:** ```#ff0000``` <br>
**RGB:** ```rgb(255, 0, 0)``` <br>
**HSL:** ```hsl(360deg, 100%, 50%)``` <br>

##### Default color codes

[ui-accordion independent=true open=0]

[ui-accordion-item title=Semantic Colors]
##### Semantic Colors

<span style="color:000000">**Negative**</span><br>
<span style="color:#BB0000">&#11044;</span> <span style="color:#BB0000"><strong>```#BB0000```</strong></span><br>
<span style="color:rgb(187, 0, 0, 1.0)">&#11044;</span> <span style="color:#BB0000"><strong>```rgb(187, 0, 0, 1.0)```</strong></span><br>

<span style="color:#E78C07">**Critical**</span><br>
HEX: ```#E78C07``` <br>
RGB: ```231/140/7``` <br>

<span style="color:#2B7D2B">**Positive**</span><br>
HEX: ```#2B7D2B``` <br>
RGB: ```43/125/43``` <br>

<span style="color:#5E696E">**Neutral**</span><br>
HEX: ```#5E696E``` <br>
RGB: ```94/105/110``` <br>

<span style="color:#427cac">**Information**</span><br>
HEX: ```#427cac``` <br>
RGB: ```66/124/172``` <br>
[/ui-accordion-item]


[ui-accordion-item title=Accent Colors]
##### Accent colors

HEX: ```#E09D00``` <br>
RGB: ```224/157/0``` <br>

HEX: ```#E6600D``` <br>
RGB: ```230/96/13``` <br>

HEX: ```#C14646``` <br>
RGB: ```193/70/70``` <br>

HEX: ```#AB218E``` <br>
RGB: ```171/33/142``` <br>

HEX: ```#678BC7``` <br>
RGB: ```103/139/199``` <br>

HEX: ```#0092D1``` <br>
RGB: ```0/146/209``` <br>

HEX: ```#1A9898``` <br>
RGB: ```26 152 152``` <br>

HEX: ```#759421``` <br>
RGB: ```117/148/33``` <br>

HEX: ```#925ACE``` <br>
RGB: ```146/90/206``` <br>

HEX: ```#647987``` <br>
RGB: ```100/121/135``` <br>
[/ui-accordion-item]
[/ui-accordion]