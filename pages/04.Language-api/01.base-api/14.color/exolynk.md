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

>>> Please be aware if you use the transparency attribute in RGB colors, that the font color of the records may not be adjusted automatically (can cause some accessibility issue due to low contrast) e.g. ```#C7D6C3)``` instead of ```rgb(67, 122, 54, 0.3)```. You will find all light colors with transparency as well translated in HEX format in this description.

##### Default color codes

[ui-accordion independent=true open=0]

[ui-accordion-item title=Semantic\040Colors]
##### Semantic Colors

<span style="color:#BB0000">**Negative**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#BB0000">&#11044;</span> <span style="color:#BB0000"><strong>```#BB0000```</strong></span><br>
<span style="color:rgb(187, 0, 0, 1.0)">&#11044;</span> <span style="color:rgb(187, 0, 0, 1.0)"><strong>```rgb(187, 0, 0, 1.0)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#EEBAB8">&#11044;</span> <span style="color:#EEBAB8"><strong>```#EEBAB8```</strong></span><br>
<span style="color:rgb(187, 0, 0, 0.3)">&#11044;</span> <span style="color:rgb(187, 0, 0, 0.3)"><strong>```rgb(187, 0, 0, 0.3)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#FF8888">&#11044;</span> <span style="color:#FF8888"><strong>```#FF8888```</strong></span><br>
<span style="color:rgb(255, 136, 136, 1.0)">&#11044;</span> <span style="color:rgb(255, 136, 136, 1.0)"><strong>```rgb(255, 136, 136, 1.0)```</strong></span><br>

<span style="color:#E78C07">**Critical**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#E78C07">&#11044;</span> <span style="color:#E78C07"><strong>```#E78C07```</strong></span><br>
<span style="color:rgb(231, 140, 7, 1.0)">&#11044;</span> <span style="color:rgb(231, 140, 7, 1.0)"><strong>```rgb(231, 140, 7, 1.0)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#F9DDBE">&#11044;</span> <span style="color:#F9DDBE"><strong>```#F9DDBE```</strong></span><br>
<span style="color:rgb(231, 140, 7, 0.3)">&#11044;</span> <span style="color:rgb(231, 140, 7, 0.3)"><strong>```rgb(231, 140, 7, 0.3)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#FABD64">&#11044;</span> <span style="color:#FABD64"><strong>```#FABD64```</strong></span><br>
<span style="color:rgb(250, 189, 100, 1.0)">&#11044;</span> <span style="color:rgb(250, 189, 100, 1.0)"><strong>```rgb(250, 189, 100, 1.0)```</strong></span><br>

<span style="color:#2B7D2B">**Positive**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#2B7D2B">&#11044;</span> <span style="color:#2B7D2B"><strong>```#2B7D2B```</strong></span><br>
<span style="color:rgb(43, 125, 43, 1.0)">&#11044;</span> <span style="color:rgb(43, 125, 43, 1.0)"><strong>```rgb(43, 125, 43, 1.0)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#C2D8C0">&#11044;</span> <span style="color:#C2D8C0"><strong>```#C2D8C0```</strong></span><br>
<span style="color:rgb(43, 125, 43, 0.3)">&#11044;</span> <span style="color:rgb(43, 125, 43, 0.3)"><strong>```rgb(43, 125, 43, 0.3)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#ABE2AB">&#11044;</span> <span style="color:#ABE2AB"><strong>```#ABE2AB```</strong></span><br>
<span style="color:rgb(171, 226, 171, 1.0)">&#11044;</span> <span style="color:rgb(171, 226, 171, 1.0)"><strong>```rgb(171, 226, 171, 1.0)```</strong></span><br>

<span style="color:#5E696E">**Neutral**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#5E696E">&#11044;</span> <span style="color:#5E696E"><strong>```#5E696E```</strong></span><br>
<span style="color:rgb(94, 105, 110, 1.0)">&#11044;</span> <span style="color:rgb(94, 105, 110, 1.0)"><strong>```rgb(94, 105, 110, 1.0)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#CED2D3">&#11044;</span> <span style="color:#CED2D3"><strong>```#CED2D3```</strong></span><br>
<span style="color:rgb(94, 105, 110, 0.3)">&#11044;</span> <span style="color:rgb(94, 105, 110, 0.3)"><strong>```rgb(94, 105, 110, 0.3)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#D3D7D9">&#11044;</span> <span style="color:#D3D7D9"><strong>```#D3D7D9```</strong></span><br>
<span style="color:rgb(211, 215, 217, 1.0)">&#11044;</span> <span style="color:rgb(211, 215, 217, 1.0)"><strong>```rgb(211, 215, 217, 1.0)```</strong></span><br>

<span style="color:#427cac">**Information**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#427CAC">&#11044;</span> <span style="color:#427CAC"><strong>```#427CAC```</strong></span><br>
<span style="color:rgb(66, 124, 172, 1.0)">&#11044;</span> <span style="color:rgb(66, 124, 172, 1.0)"><strong>```rgb(66, 124, 172, 1.0)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#C7D8E7">&#11044;</span> <span style="color:#C7D8E7"><strong>```#C7D8E7```</strong></span><br>
<span style="color:rgb(66, 124, 172, 0.3)">&#11044;</span> <span style="color:rgb(66, 124, 172, 0.3)"><strong>```rgb(66, 124, 172, 0.3)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#91C8F6">&#11044;</span> <span style="color:#91C8F6"><strong>```#91C8F6```</strong></span><br>
<span style="color:rgb(145, 200, 246, 1.0)">&#11044;</span> <span style="color:rgb(145, 200, 246, 1.0)"><strong>```rgb(145, 200, 246, 1.0)```</strong></span><br>

[/ui-accordion-item]


[ui-accordion-item title=Accent\040Colors]
##### Accent colors

<span style="color:#E09D00">**Yellow**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#E09D00">&#11044;</span> <span style="color:#E09D00"><strong>```#E09D00```</strong></span><br>
<span style="color:rgb(224, 157, 0, 1.0)">&#11044;</span> <span style="color:rgb(224, 157, 0, 1.0)"><strong>```rgb(224, 157, 0, 1.0)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#F7E1BE">&#11044;</span> <span style="color:#F7E1BE"><strong>```#F7E1BE```</strong></span><br>
<span style="color:rgb(224, 157, 0, 0.3)">&#11044;</span> <span style="color:rgb(224, 157, 0, 0.3)"><strong>```rgb(224, 157, 0, 0.3)```</strong></span><br>

<span style="color:#E6600D">**Orange**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#E6600D">&#11044;</span> <span style="color:#E6600D"><strong>```#E6600D```</strong></span><br>
<span style="color:rgb(230, 96, 13, 1.0)">&#11044;</span> <span style="color:rgb(230, 96, 13, 1.0)"><strong>```rgb(230, 96, 13, 1.0)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#FAD0BC">&#11044;</span> <span style="color:#FAD0BC"><strong>```#FAD0BC```</strong></span><br>
<span style="color:rgb(230, 96, 13, 0.3)">&#11044;</span> <span style="color:rgb(230, 96, 13, 0.3)"><strong>```rgb(230, 96, 13, 0.3)```</strong></span><br>

<span style="color:#C14646">**Red**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#C14646">&#11044;</span> <span style="color:#C14646"><strong>```#C14646```</strong></span><br>
<span style="color:rgb(193, 70, 70, 1.0)">&#11044;</span> <span style="color:rgb(193, 70, 70, 1.0)"><strong>```rgb(193, 70, 70, 1.0)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#EEC9C7">&#11044;</span> <span style="color:#EEC9C7"><strong>```#EEC9C7```</strong></span><br>
<span style="color:rgb(193, 70, 70, 0.3)">&#11044;</span> <span style="color:rgb(193, 70, 70, 0.3)"><strong>```rgb(193, 70, 70, 0.3)```</strong></span><br>

<span style="color:#AB218E">**Purpur**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#AB218E">&#11044;</span> <span style="color:#AB218E"><strong>```#AB218E```</strong></span><br>
<span style="color:rgb(171, 33, 142, 1.0)">&#11044;</span> <span style="color:rgb(171, 33, 142, 1.0)"><strong>```rgb(171, 33, 142, 1.0)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#E8BEDE">&#11044;</span> <span style="color:#E8BEDE"><strong>```#E8BEDE```</strong></span><br>
<span style="color:rgb(171, 33, 142, 0.3)">&#11044;</span> <span style="color:rgb(171, 33, 142, 0.3)"><strong>```rgb(171, 33, 142, 0.3)```</strong></span><br>

<span style="color:#678BC7">**Darkblue**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#678BC7">&#11044;</span> <span style="color:#678BC7"><strong>```#678BC7```</strong></span><br>
<span style="color:rgb(103, 139, 199, 1.0)">&#11044;</span> <span style="color:rgb(103, 139, 199, 1.0)"><strong>```rgb(103, 139, 199, 1.0)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#D1DCEF">&#11044;</span> <span style="color:#D1DCEF"><strong>```#D1DCEF```</strong></span><br>
<span style="color:rgb(103, 139, 199, 0.3)">&#11044;</span> <span style="color:rgb(103, 139, 199, 0.3)"><strong>```rgb(103, 139, 199, 0.3)```</strong></span><br>

<span style="color:#0092D1">**Blue**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#0092D1">&#11044;</span> <span style="color:#0092D1"><strong>```#0092D1```</strong></span><br>
<span style="color:rgb(0, 146, 209, 1.0)">&#11044;</span> <span style="color:rgb(0, 146, 209, 1.0)"><strong>```rgb(0, 146, 209, 1.0)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#BFDEF1">&#11044;</span> <span style="color:#BFDEF1"><strong>```#BFDEF1```</strong></span><br>
<span style="color:rgb(0, 146, 209, 0.3)">&#11044;</span> <span style="color:rgb(0, 146, 209, 0.3)"><strong>```rgb(0, 146, 209, 0.3)```</strong></span><br>

<span style="color:#1A9898">**Turquoise**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#1A9898">&#11044;</span> <span style="color:#1A9898"><strong>```#1A9898```</strong></span><br>
<span style="color:rgb(26, 152, 152, 1.0)">&#11044;</span> <span style="color:rgb(26, 152, 152, 1.0)"><strong>```rgb(26, 152, 152, 1.0)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#C2E0E1">&#11044;</span> <span style="color:#C2E0E1"><strong>```#C2E0E1```</strong></span><br>
<span style="color:rgb(26, 152, 152, 0.3)">&#11044;</span> <span style="color:rgb(26, 152, 152, 0.3)"><strong>```rgb(26, 152, 152, 0.3)```</strong></span><br>

<span style="color:#759421">**Green**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#759421">&#11044;</span> <span style="color:#759421"><strong>```#759421```</strong></span><br>
<span style="color:rgb(117, 148, 33, 1.0)">&#11044;</span> <span style="color:rgb(117, 148, 33, 1.0)"><strong>```rgb(117, 148, 33, 1.0)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#D5DEC0">&#11044;</span> <span style="color:#D5DEC0"><strong>```#D5DEC0```</strong></span><br>
<span style="color:rgb(117, 148, 33, 0.3)">&#11044;</span> <span style="color:rgb(117, 148, 33, 0.3)"><strong>```rgb(117, 148, 33, 0.3)```</strong></span><br>

<span style="color:#925ACE">**Purple**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#925ACE">&#11044;</span> <span style="color:#925ACE"><strong>```#925ACE```</strong></span><br>
<span style="color:rgb(146, 90, 206, 1.0)">&#11044;</span> <span style="color:rgb(146, 90, 206, 1.0)"><strong>```rgb(146, 90, 206, 1.0)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#DFCDF1">&#11044;</span> <span style="color:#DFCDF1"><strong>```#DFCDF1```</strong></span><br>
<span style="color:rgb(146, 90, 206, 0.3)">&#11044;</span> <span style="color:rgb(146, 90, 206, 0.3)"><strong>```rgb(146, 90, 206, 0.3)```</strong></span><br>

<span style="color:#647987">**Gray**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#647987">&#11044;</span> <span style="color:#647987"><strong>```#647987```</strong></span><br>
<span style="color:rgb(100, 121, 135, 1.0)">&#11044;</span> <span style="color:rgb(100, 121, 135, 1.0)"><strong>```rgb(100, 121, 135, 1.0)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#D0D6DA">&#11044;</span> <span style="color:#D0D6DA"><strong>```#D0D6DA```</strong></span><br>
<span style="color:rgb(100, 121, 135, 0.3)">&#11044;</span> <span style="rgb(100, 121, 135, 0.3)"><strong>```rgb(100, 121, 135, 0.3)```</strong></span><br>

[/ui-accordion-item]

[ui-accordion-item title=Indicator\040Colors]
##### Indicator colors

<span style="color:#880000">**UI Indication 1**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#880000">&#11044;</span> <span style="color:#880000"><strong>```#880000```</strong></span><br>
<span style="color:rgb(136, 0, 0, 1.0)">&#11044;</span> <span style="color:rgb(136, 0, 0, 1.0)"><strong>```rgb(136, 0, 0, 1.0)```</strong></span><br>
<span style="">Light Flavor 50% transparency</span><br>
<span style="color:#C68784">&#11044;</span> <span style="color:#C68784"><strong>```#C68784```</strong></span><br>
<span style="color:rgb(136, 0, 0, 0.5)">&#11044;</span> <span style="color:rgb(136, 0, 0, 0.5)"><strong>```rgb(136, 0, 0, 0.5)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#DEB8B5">&#11044;</span> <span style="color:#DEB8B5"><strong>```#DEB8B5```</strong></span><br>
<span style="color:rgb(136, 0, 0, 0.3)">&#11044;</span> <span style="color:rgb(136, 0, 0, 0.3)"><strong>```rgb(136, 0, 0, 0.3)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#FF8888">&#11044;</span> <span style="color:#FF8888"><strong>```#FF8888```</strong></span><br>
<span style="color:rgb(255, 136, 136, 1.0)">&#11044;</span> <span style="color:rgb(255, 136, 136, 1.0)"><strong>```rgb(255, 136, 136, 1.0)```</strong></span><br>

<span style="color:#BB0000">**UI Indication 2**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#BB0000">&#11044;</span> <span style="color:#BB0000"><strong>```#BB0000```</strong></span><br>
<span style="color:rgb(171, 34, 23, 1.0)">&#11044;</span> <span style="color:rgb(171, 34, 23, 1.0)"><strong>```rgb(171, 34, 23, 1.0)```</strong></span><br>
<span style="">Light Flavor 50% transparency</span><br>
<span style="color:#D8948E">&#11044;</span> <span style="color:#D8948E"><strong>```#D8948E```</strong></span><br>
<span style="color:rgb(171, 34, 23, 0.5)">&#11044;</span> <span style="color:rgb(171, 34, 23, 0.5)"><strong>```rgb(171, 34, 23, 0.5)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#E8BEBB">&#11044;</span> <span style="color:#E8BEBB"><strong>```#E8BEBB```</strong></span><br>
<span style="color:rgb(171, 34, 23, 0.3)">&#11044;</span> <span style="color:rgb(171, 34, 23, 0.3)"><strong>```rgb(171, 34, 23, 0.3)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#FFBBBB">&#11044;</span> <span style="color:#FFBBBB"><strong>```#FFBBBB```</strong></span><br>
<span style="color:rgb(255, 187, 187, 1.0)">&#11044;</span> <span style="color:rgb(255, 187, 187, 1.0)"><strong>```rgb(255, 187, 187, 1.0)```</strong></span><br>

<span style="color:#E78C07">**UI Indication 3**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#E78C07">&#11044;</span> <span style="color:#E78C07"><strong>```#E78C07```</strong></span><br>
<span style="color:rgb(219, 144, 52, 1.0)">&#11044;</span> <span style="color:rgb(219, 144, 52, 1.0)"><strong>```rgb(219, 144, 52, 1.0)```</strong></span><br>
<span style="">Light Flavor 50% transparency</span><br>
<span style="color:#EEC89E">&#11044;</span> <span style="color:#EEC89E"><strong>```#EEC89E```</strong></span><br>
<span style="color:rgb(219, 144, 52, 0.5)">&#11044;</span> <span style="color:rgb(219, 144, 52, 0.5)"><strong>```rgb(219, 144, 52, 0.5)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#F5DDC5">&#11044;</span> <span style="color:#F5DDC5"><strong>```#F5DDC5```</strong></span><br>
<span style="color:rgb(219, 144, 52, 0.3)">&#11044;</span> <span style="color:rgb(219, 144, 52, 0.3)"><strong>```rgb(219, 144, 52, 0.3)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#FABD64">&#11044;</span> <span style="color:#FABD64"><strong>```#FABD64```</strong></span><br>
<span style="color:rgb(250, 189, 100, 1.0)">&#11044;</span> <span style="color:rgb(250, 189, 100, 1.0)"><strong>```rgb(250, 189, 100, 1.0)```</strong></span><br>

<span style="color:#2B7C2B">**UI Indication 4**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#2B7C2B">&#11044;</span> <span style="color:#2B7C2B"><strong>```#2B7C2B```</strong></span><br>
<span style="color:rgb(67, 122, 54, 1.0)">&#11044;</span> <span style="color:rgb(67, 122, 54, 1.0)"><strong>```rgb(67, 122, 54, 1.0)```</strong></span><br>
<span style="">Light Flavor 50% transparency</span><br>
<span style="color:#A2BD9B">&#11044;</span> <span style="color:#A2BD9B"><strong>```#A2BD9B```</strong></span><br>
<span style="color:rgb(67, 122, 54, 0.5)">&#11044;</span> <span style="color:rgb(67, 122, 54, 0.5)"><strong>```rgb(67, 122, 54, 0.5)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#C7D6C3">&#11044;</span> <span style="color:#C7D6C3"><strong>```#C7D6C3```</strong></span><br>
<span style="color:rgb(67, 122, 54, 0.3)">&#11044;</span> <span style="color:rgb(67, 122, 54, 0.3)"><strong>```rgb(67, 122, 54, 0.3)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#ABE2AB">&#11044;</span> <span style="color:#ABE2AB"><strong>```#ABE2AB```</strong></span><br>
<span style="color:rgb(171, 226, 171, 1.0)">&#11044;</span> <span style="color:rgb(171, 226, 171, 1.0)"><strong>```rgb(171, 226, 171, 1.0)```</strong></span><br>

<span style="color:#427CAC">**UI Indication 5**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#427CAC">&#11044;</span> <span style="color:#427CAC"><strong>```#427CAC```</strong></span><br>
<span style="color:rgb(80, 123, 168, 1.0)">&#11044;</span> <span style="color:rgb(80, 123, 168, 1.0)"><strong>```rgb(80, 123, 168, 1.0)```</strong></span><br>
<span style="">Light Flavor 50% transparency</span><br>
<span style="color:#A8BDD3">&#11044;</span> <span style="color:#A8BDD3"><strong>```#A8BDD3```</strong></span><br>
<span style="color:rgb(80, 123, 168, 0.5)">&#11044;</span> <span style="color:rgb(80, 123, 168, 0.5)"><strong>```rgb(80, 123, 168, 0.5)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#CBD7E5">&#11044;</span> <span style="color:#CBD7E5"><strong>```#CBD7E5```</strong></span><br>
<span style="color:rgb(80, 123, 168, 0.3)">&#11044;</span> <span style="color:rgb(80, 123, 168, 0.3)"><strong>```rgb(80, 123, 168, 0.3)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#91C8F6">&#11044;</span> <span style="color:#91C8F6"><strong>```#91C8F6```</strong></span><br>
<span style="color:rgb(145, 200, 246, 1.0)">&#11044;</span> <span style="color:rgb(145, 200, 246, 1.0)"><strong>```rgb(145, 200, 246, 1.0)```</strong></span><br>

<span style="color:#1A9898">**UI Indication 6**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#1A9898">&#11044;</span> <span style="color:#1A9898"><strong>```#1A9898```</strong></span><br>
<span style="color:rgb(26, 152, 152, 1.0)">&#11044;</span> <span style="color:rgb(26, 152, 152, 1.0)"><strong>```rgb(26, 152, 152, 1.0)```</strong></span><br>
<span style="">Light Flavor 50% transparency</span><br>
<span style="color:#98CBCC">&#11044;</span> <span style="color:#98CBCC"><strong>```#98CBCC```</strong></span><br>
<span style="color:rgb(26, 152, 152, 0.5)">&#11044;</span> <span style="color:rgb(26, 152, 152, 0.5)"><strong>```rgb(26, 152, 152, 0.5)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#C2E0E1">&#11044;</span> <span style="color:#C2E0E1"><strong>```#C2E0E1```</strong></span><br>
<span style="color:rgb(26, 152, 152, 0.3)">&#11044;</span> <span style="color:rgb(26, 152, 152, 0.3)"><strong>```rgb(26, 152, 152, 0.3)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#7FC6C6">&#11044;</span> <span style="color:#7FC6C6"><strong>```#7FC6C6```</strong></span><br>
<span style="color:rgb(127, 198, 198, 1.0)">&#11044;</span> <span style="color:rgb(127, 198, 198, 1.0)"><strong>```rgb(127, 198, 198, 1.0)```</strong></span><br>

<span style="color:#925ACE">**UI Indication 7**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#925ACE">&#11044;</span> <span style="color:#925ACE"><strong>```#925ACE```</strong></span><br>
<span style="color:rgb(146, 90, 206, 1.0)">&#11044;</span> <span style="color:rgb(146, 90, 206, 1.0)"><strong>```rgb(146, 90, 206, 1.0)```</strong></span><br>
<span style="">Light Flavor 50% transparency</span><br>
<span style="color:#C9ACE7">&#11044;</span> <span style="color:#C9ACE7"><strong>```#C9ACE7```</strong></span><br>
<span style="color:rgb(146, 90, 206, 0.5)">&#11044;</span> <span style="color:rgb(146, 90, 206, 0.5)"><strong>```rgb(146, 90, 206, 0.5)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#DFCDF1">&#11044;</span> <span style="color:#DFCDF1"><strong>```#DFCDF1```</strong></span><br>
<span style="color:rgb(146, 90, 206, 0.3)">&#11044;</span> <span style="color:rgb(146, 90, 206, 0.3)"><strong>```rgb(146, 90, 206, 0.3)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#B995E0">&#11044;</span> <span style="color:#B995E0"><strong>```#B995E0```</strong></span><br>
<span style="color:rgb(185, 149, 224, 1.0)">&#11044;</span> <span style="color:rgb(185, 149, 224, 1.0)"><strong>```rgb(185, 149, 224, 1.0)```</strong></span><br>

<span style="color:#AB218E">**UI Indication 8**</span><br>
<span style="">Light Flavor</span><br>
<span style="color:#AB218E">&#11044;</span> <span style="color:#AB218E"><strong>```#AB218E```</strong></span><br>
<span style="color:rgb(171, 33, 142, 1.0)">&#11044;</span> <span style="color:rgb(171, 33, 142, 1.0)"><strong>```rgb(171, 33, 142, 1.0)```</strong></span><br>
<span style="">Light Flavor 50% transparency</span><br>
<span style="color:#D893C7">&#11044;</span> <span style="color:#D893C7"><strong>```#D893C7```</strong></span><br>
<span style="color:rgb(171, 33, 142, 0.5)">&#11044;</span> <span style="color:rgb(171, 33, 142, 0.5)"><strong>```rgb(171, 33, 142, 0.5)```</strong></span><br>
<span style="">Light Flavor 30% transparency</span><br>
<span style="color:#E8BEDE">&#11044;</span> <span style="color:#E8BEDE"><strong>```#E8BEDE```</strong></span><br>
<span style="color:rgb(171, 33, 142, 0.3)">&#11044;</span> <span style="color:rgb(171, 33, 142, 0.3)"><strong>```rgb(171, 33, 142, 0.3)```</strong></span><br>
<span style="">Dark Flavor</span><br>
<span style="color:#E269C9">&#11044;</span> <span style="color:#E269C9"><strong>```#E269C9```</strong></span><br>
<span style="color:rgb(226, 105, 200, 1.0)">&#11044;</span> <span style="color:rgb(226, 105, 200, 1.0)"><strong>```rgb(226, 105, 200, 1.0)```</strong></span><br>

[/ui-accordion-item]
[/ui-accordion]