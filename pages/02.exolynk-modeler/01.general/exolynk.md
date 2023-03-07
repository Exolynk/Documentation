---
title: General
taxonomy:
    category: docs
markdown.extra: true
process:
    twig: false
    markdown: true
---

[TOC]



In the Modeler view you find in the left section (fig.14) the overview of all existing models (including default models like access right or custome models).
![Modeler General](modeler-general.png?lightbox=1024&cropResize=900,900) {.left}

>>> Please be aware that models for which the logged-in user doesn`t have read access may be not visible in this view.

With the button **+ New** you can add a new model (this will appear with a logo but no title) click on this new element to configure the details.

## General Section

In the detail in the section **General Settings** can be edited with activating the **Edit** mode (fig. 2 -> toggle between 'edit' and 'finish').

>>> Please be aware that models cannot be deleted yet.

<br>

### General Settings and Default Parameters:

[ui-accordion independent=true open=0]

[ui-accordion-item title=<b>Uuid</b>\040(fig.4)]
##### Description
Universally unique identifier (128-bit label) used for identifying the object
[/ui-accordion-item]


[ui-accordion-item title=<b>Ident</b>\040(fig.5)]
##### Description
Human readable ID (unique in context). Can contain only small letters, subline, full numbers, first possition need to be a letter (will automatically change to small if big letters are entered).
[/ui-accordion-item]


[ui-accordion-item title=<b>Version</b>\040(fig.6)]
##### Description
The version of the model. Will be encreased with any new release. the version is not editable.
[/ui-accordion-item]


[ui-accordion-item title=<b>Status</b>\040(fig.7)]
##### Model Statis<br>
<code>draft</code> = in draft state, not released yet<br>
<code>active</code> =  in use and latest released<br>
<code>released</code> = frozen, records points to model version initially released<br>

[/ui-accordion-item]


[ui-accordion-item title=<b>System\040Model</b>\040(fig.8)]
##### Description
Predefined by system (basic functions needed). Defines if this is a default Model (System Model) or not. Cannot be changed by user.
[/ui-accordion-item]


[ui-accordion-item title=<b>Name</b>\040(fig.9)]
##### Description
Object Name, full text no limitations.
[/ui-accordion-item]


[ui-accordion-item title=<b>Description</b>\040(fig.10)]
##### Description
Object Description, full text no limitations
[/ui-accordion-item]


[ui-accordion-item title=<b>Icon</b>\040(fig.11)]
##### Description
The Object/Model Icon. For the icon shortcodes, please refere to the [UI5 Icon library](https://sapui5.hana.ondemand.com/sdk/test-resources/sap/m/demokit/iconExplorer/webapp/index.html#/overview/SAP-icons)
[/ui-accordion-item]


[ui-accordion-item title=<b>Record\040Status</b>\040(fig.12)]
##### Description
The record status defines the state of the object record. The options and its translations can be defined free by clicking on the Globe-Icon Figure 12.a<br>
![Record Status](record-status-detail.png?lightbox=1024&cropResize=500,500) {.left}
[/ui-accordion-item]


[ui-accordion-item title=<b>Model\040right</b>\040(fig.13)]
##### Description
With the parameter Model right, the access right of the model can be selected from a predefined set of user or file rights.<br>
![Model right](model-right-detail.png?lightbox=1024&cropResize=500,500) {.left}
[/ui-accordion-item]

[/ui-accordion]

