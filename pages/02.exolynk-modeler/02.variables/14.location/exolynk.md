---
title: 'Location'
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
### Location
A location object with the <a href="https://www.openstreetmap.org/" target="_blank">OpenStreetMap</a> API and the follwing attributes:
- Street
- House Number
- ZIP Code
- City
- Country
- Latitude
- Longitude

Works on two ways:
1) filling out the string variables with the help of autocomplete based on the OpenStreetMap datas.
2) click "Set actual position" button to geolocate yourself and autofill your location automatically

### UI Example
![Location](location.gif?resize=800&classes=left)

### UI Layout Example
````html
<variable ident="location_name" access="write" />
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