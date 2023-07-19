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

<span style="color:#BB0000">**Negative**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#BB0000">&#11044;</span> <span style="color:#BB0000"><strong>```#BB0000```</strong></span><br>
<span style="color:rgb(187, 0, 0, 1.0)">&#11044;</span> <span style="color:rgb(187, 0, 0, 1.0)"><strong>```rgb(187, 0, 0, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#f4afb1">&#11044;</span> <span style="color:#f4afb1"><strong>```#F4AFB1```</strong></span><br>
<span style="color:rgb(187, 0, 0, 0.3)">&#11044;</span> <span style="color:rgb(187, 0, 0, 0.3)"><strong>```rgb(187, 0, 0, 0.3)```</strong></span><br>

<span style="color:#E78C07">**Critical**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#E78C07">&#11044;</span> <span style="color:#E78C07"><strong>```#E78C07```</strong></span><br>
<span style="color:rgb(231, 140, 7, 1.0)">&#11044;</span> <span style="color:rgb(231, 140, 7, 1.0)"><strong>```rgb(231, 140, 7, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#FEDBAE">&#11044;</span> <span style="color:#FEDBAE"><strong>```#FEDBAE```</strong></span><br>
<span style="color:rgb(231, 140, 7, 0.3)">&#11044;</span> <span style="color:rgb(231, 140, 7, 0.3)"><strong>```rgb(231, 140, 7, 0.3)```</strong></span><br>

<span style="color:#2B7D2B">**Positive**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#2B7D2B">&#11044;</span> <span style="color:#2B7D2B"><strong>```#2B7D2B```</strong></span><br>
<span style="color:rgb(43, 125, 43, 1.0)">&#11044;</span> <span style="color:rgb(43, 125, 43, 1.0)"><strong>```rgb(43, 125, 43, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#B8D9BC">&#11044;</span> <span style="color:#B8D9BC"><strong>```#B8D9BC```</strong></span><br>
<span style="color:rgb(43, 125, 43, 0.3)">&#11044;</span> <span style="color:rgb(43, 125, 43, 0.3)"><strong>```rgb(43, 125, 43, 0.3)```</strong></span><br>

<span style="color:#5E696E">**Neutral**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#5E696E">&#11044;</span> <span style="color:#5E696E"><strong>```#5E696E```</strong></span><br>
<span style="color:rgb(94, 105, 110, 1.0)">&#11044;</span> <span style="color:rgb(94, 105, 110, 1.0)"><strong>```rgb(94, 105, 110, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#CDD2D3">&#11044;</span> <span style="color:#CDD2D3"><strong>```#CDD2D3```</strong></span><br>
<span style="color:rgb(94, 105, 110, 0.3)">&#11044;</span> <span style="color:rgb(94, 105, 110, 0.3)"><strong>```rgb(94, 105, 110, 0.3)```</strong></span><br>

<span style="color:#427cac">**Information**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#427CAC">&#11044;</span> <span style="color:#427CAC"><strong>```#427CAC```</strong></span><br>
<span style="color:rgb(66, 124, 172, 1.0)">&#11044;</span> <span style="color:rgb(66, 124, 172, 1.0)"><strong>```rgb(66, 124, 172, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#C2D7E8">&#11044;</span> <span style="color:#C2D7E8"><strong>```#C2D7E8```</strong></span><br>
<span style="color:rgb(66, 124, 172, 0.3)">&#11044;</span> <span style="color:rgb(66, 124, 172, 0.3)"><strong>```rgb(66, 124, 172, 0.3)```</strong></span><br>

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