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

<span style="color:#E09D00">**Yellow**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#E09D00">&#11044;</span> <span style="color:#E09D00"><strong>```#E09D00```</strong></span><br>
<span style="color:rgb(224, 157, 0, 1.0)">&#11044;</span> <span style="color:rgb(224, 157, 0, 1.0)"><strong>```rgb(224, 157, 0, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#FAE0AB">&#11044;</span> <span style="color:#FAE0AB"><strong>```#FAE0AB```</strong></span><br>
<span style="color:rgb(224, 157, 0, 0.3)">&#11044;</span> <span style="color:rgb(224, 157, 0, 0.3)"><strong>```rgb(224, 157, 0, 0.3)```</strong></span><br>

<span style="color:#E6600D">**Orange**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#E6600D">&#11044;</span> <span style="color:#E6600D"><strong>```#E6600D```</strong></span><br>
<span style="color:rgb(230, 96, 13, 1.0)">&#11044;</span> <span style="color:rgb(230, 96, 13, 1.0)"><strong>```rgb(230, 96, 13, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#FECDB1">&#11044;</span> <span style="color:#FECDB1"><strong>```#FECDB1```</strong></span><br>
<span style="color:rgb(230, 96, 13, 0.3)">&#11044;</span> <span style="color:rgb(230, 96, 13, 0.3)"><strong>```rgb(230, 96, 13, 0.3)```</strong></span><br>

<span style="color:#C14646">**Red**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#C14646">&#11044;</span> <span style="color:#C14646"><strong>```#C14646```</strong></span><br>
<span style="color:rgb(193, 70, 70, 1.0)">&#11044;</span> <span style="color:rgb(193, 70, 70, 1.0)"><strong>```rgb(193, 70, 70, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#F3C5C6">&#11044;</span> <span style="color:#F3C5C6"><strong>```#F3C5C6```</strong></span><br>
<span style="color:rgb(193, 70, 70, 0.3)">&#11044;</span> <span style="color:rgb(193, 70, 70, 0.3)"><strong>```rgb(193, 70, 70, 0.3)```</strong></span><br>

<span style="color:#AB218E">**Violet**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#AB218E">&#11044;</span> <span style="color:#AB218E"><strong>```#AB218E```</strong></span><br>
<span style="color:rgb(171, 33, 142, 1.0)">&#11044;</span> <span style="color:rgb(171, 33, 142, 1.0)"><strong>```rgb(171, 33, 142, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#EDB9DF">&#11044;</span> <span style="color:#EDB9DF"><strong>```#EDB9DF```</strong></span><br>
<span style="color:rgb(171, 33, 142, 0.3)">&#11044;</span> <span style="color:rgb(171, 33, 142, 0.3)"><strong>```rgb(171, 33, 142, 0.3)```</strong></span><br>

<span style="color:#678BC7">**Darkblue**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#678BC7">&#11044;</span> <span style="color:#678BC7"><strong>```#678BC7```</strong></span><br>
<span style="color:rgb(103, 139, 199, 1.0)">&#11044;</span> <span style="color:rgb(103, 139, 199, 1.0)"><strong>```rgb(103, 139, 199, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#CEDCEF">&#11044;</span> <span style="color:#CEDCEF"><strong>```#CEDCEF```</strong></span><br>
<span style="color:rgb(103, 139, 199, 0.3)">&#11044;</span> <span style="color:rgb(103, 139, 199, 0.3)"><strong>```rgb(103, 139, 199, 0.3)```</strong></span><br>

<span style="color:#0092D1">**Blue**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#0092D1">&#11044;</span> <span style="color:#0092D1"><strong>```#0092D1```</strong></span><br>
<span style="color:rgb(0, 146, 209, 1.0)">&#11044;</span> <span style="color:rgb(0, 146, 209, 1.0)"><strong>```rgb(0, 146, 209, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#A6DFF3">&#11044;</span> <span style="color:#A6DFF3"><strong>```#A6DFF3```</strong></span><br>
<span style="color:rgb(0, 146, 209, 0.3)">&#11044;</span> <span style="color:rgb(0, 146, 209, 0.3)"><strong>```rgb(0, 146, 209, 0.3)```</strong></span><br>

<span style="color:#1A9898">**Turquoise**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#1A9898">&#11044;</span> <span style="color:#1A9898"><strong>```#1A9898```</strong></span><br>
<span style="color:rgb(26, 152, 152, 1.0)">&#11044;</span> <span style="color:rgb(26, 152, 152, 1.0)"><strong>```rgb(26, 152, 152, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#B0E1E1">&#11044;</span> <span style="color:#B0E1E1"><strong>```#B0E1E1```</strong></span><br>
<span style="color:rgb(26, 152, 152, 0.3)">&#11044;</span> <span style="color:rgb(26, 152, 152, 0.3)"><strong>```rgb(26, 152, 152, 0.3)```</strong></span><br>

<span style="color:#759421">**Green**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#759421">&#11044;</span> <span style="color:#759421"><strong>```#759421```</strong></span><br>
<span style="color:rgb(117, 148, 33, 1.0)">&#11044;</span> <span style="color:rgb(117, 148, 33, 1.0)"><strong>```rgb(117, 148, 33, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#D2DFB8">&#11044;</span> <span style="color:#D2DFB8"><strong>```#D2DFB8```</strong></span><br>
<span style="color:rgb(117, 148, 33, 0.3)">&#11044;</span> <span style="color:rgb(117, 148, 33, 0.3)"><strong>```rgb(117, 148, 33, 0.3)```</strong></span><br>

<span style="color:#925ACE">**Purple**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#925ACE">&#11044;</span> <span style="color:#925ACE"><strong>```#925ACE```</strong></span><br>
<span style="color:rgb(146, 90, 206, 1.0)">&#11044;</span> <span style="color:rgb(146, 90, 206, 1.0)"><strong>```rgb(146, 90, 206, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#E1CCF3">&#11044;</span> <span style="color:#E1CCF3"><strong>```#E1CCF3```</strong></span><br>
<span style="color:rgb(146, 90, 206, 0.3)">&#11044;</span> <span style="color:rgb(146, 90, 206, 0.3)"><strong>```rgb(146, 90, 206, 0.3)```</strong></span><br>

<span style="color:#647987">**Gray**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#647987">&#11044;</span> <span style="color:#647987"><strong>```#647987```</strong></span><br>
<span style="color:rgb(100, 121, 135, 1.0)">&#11044;</span> <span style="color:rgb(100, 121, 135, 1.0)"><strong>```rgb(100, 121, 135, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#CED7DB">&#11044;</span> <span style="color:#CED7DB"><strong>```#CED7DB```</strong></span><br>
<span style="color:rgb(100, 121, 135, 0.3)">&#11044;</span> <span style="rgb(100, 121, 135, 0.3)"><strong>```rgb(100, 121, 135, 0.3)```</strong></span><br>

[/ui-accordion-item]

[ui-accordion-item title=Indicator Colors]
##### Accent colors

<span style="color:#880000">**UI Indication 1**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#880000">&#11044;</span> <span style="color:#880000"><strong>```#880000```</strong></span><br>
<span style="color:rgb(136, 0, 0, 1.0)">&#11044;</span> <span style="color:rgb(136, 0, 0, 1.0)"><strong>```rgb(136, 0, 0, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#FAE0AB">&#11044;</span> <span style="color:#FAE0AB"><strong>```#FAE0AB```</strong></span><br>
<span style="color:rgb(136, 0, 0, 0.3)">&#11044;</span> <span style="color:rgb(136, 0, 0, 0.3)"><strong>```rgb(136, 0, 0, 0.3)```</strong></span><br>

RGB 171/34/23
<span style="color:#BB0000">**UI Indication 2**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#BB0000">&#11044;</span> <span style="color:#BB0000"><strong>```#BB0000```</strong></span><br>
<span style="color:rgb(230, 96, 13, 1.0)">&#11044;</span> <span style="color:rgb(230, 96, 13, 1.0)"><strong>```rgb(230, 96, 13, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#FECDB1">&#11044;</span> <span style="color:#FECDB1"><strong>```#FECDB1```</strong></span><br>
<span style="color:rgb(230, 96, 13, 0.3)">&#11044;</span> <span style="color:rgb(230, 96, 13, 0.3)"><strong>```rgb(230, 96, 13, 0.3)```</strong></span><br>

RGB 219/144/52
<span style="color:#E78C07">**UI Indication 3**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#E78C07">&#11044;</span> <span style="color:#E78C07"><strong>```#E78C07```</strong></span><br>
<span style="color:rgb(193, 70, 70, 1.0)">&#11044;</span> <span style="color:rgb(193, 70, 70, 1.0)"><strong>```rgb(193, 70, 70, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#F3C5C6">&#11044;</span> <span style="color:#F3C5C6"><strong>```#F3C5C6```</strong></span><br>
<span style="color:rgb(193, 70, 70, 0.3)">&#11044;</span> <span style="color:rgb(193, 70, 70, 0.3)"><strong>```rgb(193, 70, 70, 0.3)```</strong></span><br>

RGB 67/122/54
<span style="color:#2B7C2B">**UI Indication 4**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#2B7C2B">&#11044;</span> <span style="color:#2B7C2B"><strong>```#2B7C2B```</strong></span><br>
<span style="color:rgb(171, 33, 142, 1.0)">&#11044;</span> <span style="color:rgb(171, 33, 142, 1.0)"><strong>```rgb(171, 33, 142, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#EDB9DF">&#11044;</span> <span style="color:#EDB9DF"><strong>```#EDB9DF```</strong></span><br>
<span style="color:rgb(171, 33, 142, 0.3)">&#11044;</span> <span style="color:rgb(171, 33, 142, 0.3)"><strong>```rgb(171, 33, 142, 0.3)```</strong></span><br>

RGB 80/123/168
<span style="color:#427CAC">**UI Indication 5**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#427CAC">&#11044;</span> <span style="color:#427CAC"><strong>```#427CAC```</strong></span><br>
<span style="color:rgb(103, 139, 199, 1.0)">&#11044;</span> <span style="color:rgb(103, 139, 199, 1.0)"><strong>```rgb(103, 139, 199, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#CEDCEF">&#11044;</span> <span style="color:#CEDCEF"><strong>```#CEDCEF```</strong></span><br>
<span style="color:rgb(103, 139, 199, 0.3)">&#11044;</span> <span style="color:rgb(103, 139, 199, 0.3)"><strong>```rgb(103, 139, 199, 0.3)```</strong></span><br>

RGB 26/152/152
<span style="color:#1A9898">**UI Indication 6**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#1A9898">&#11044;</span> <span style="color:#1A9898"><strong>```#1A9898```</strong></span><br>
<span style="color:rgb(0, 146, 209, 1.0)">&#11044;</span> <span style="color:rgb(0, 146, 209, 1.0)"><strong>```rgb(0, 146, 209, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#A6DFF3">&#11044;</span> <span style="color:#A6DFF3"><strong>```#A6DFF3```</strong></span><br>
<span style="color:rgb(0, 146, 209, 0.3)">&#11044;</span> <span style="color:rgb(0, 146, 209, 0.3)"><strong>```rgb(0, 146, 209, 0.3)```</strong></span><br>

RGB 146/90/206
<span style="color:#925ACE">**UI Indication 7**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#925ACE">&#11044;</span> <span style="color:#925ACE"><strong>```#925ACE```</strong></span><br>
<span style="color:rgb(26, 152, 152, 1.0)">&#11044;</span> <span style="color:rgb(26, 152, 152, 1.0)"><strong>```rgb(26, 152, 152, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#B0E1E1">&#11044;</span> <span style="color:#B0E1E1"><strong>```#B0E1E1```</strong></span><br>
<span style="color:rgb(26, 152, 152, 0.3)">&#11044;</span> <span style="color:rgb(26, 152, 152, 0.3)"><strong>```rgb(26, 152, 152, 0.3)```</strong></span><br>

RGB 171/33/142
<span style="color:#AB218E">**UI Indication 8**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#AB218E">&#11044;</span> <span style="color:#AB218E"><strong>```#AB218E```</strong></span><br>
<span style="color:rgb(117, 148, 33, 1.0)">&#11044;</span> <span style="color:rgb(117, 148, 33, 1.0)"><strong>```rgb(117, 148, 33, 1.0)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#D2DFB8">&#11044;</span> <span style="color:#D2DFB8"><strong>```#D2DFB8```</strong></span><br>
<span style="color:rgb(117, 148, 33, 0.3)">&#11044;</span> <span style="color:rgb(117, 148, 33, 0.3)"><strong>```rgb(117, 148, 33, 0.3)```</strong></span><br>

[/ui-accordion-item]
[/ui-accordion]