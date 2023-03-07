---
title: Modeler
taxonomy:
    category: docs
markdown.extra: true
process:
    twig: false
    markdown: true
---

[TOC]

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

# Modeler

In the Modeler view you find in the left section (fig.14) the overview of all existing models (including default models like access right or custome models).

>>> Please be aware that models for which the logged-in user doesn`t have read access may be not visible in this view.

With the button **+ New** you can add a new model (this will appear with a logo but no title) click on this new element to configure the details.

## General

In the detail in the section **General Settings** can be edited with activating the **Edit** mode (fig. 2 -> toggle between 'edit' and 'finish').

![Modeler General](modeler-general.png?lightbox=1024&cropResize=900,900) {.left}

>>> Please be aware that models cannot be deleted yet.

### General Settings and Default Parameters:

[ui-accordion independent=true open=0]

[ui-accordion-item title=<b>Uuid</b>\040(fig.4)]
Universally unique identifier (128-bit label) used for identifying the object
[/ui-accordion-item]


[ui-accordion-item title=<b>Ident</b>\040(fig.5)]
Human readable ID (unique in context). Can contain only small letters, subline, full numbers, first possition need to be a letter (will automatically change to small if big letters are entered).
[/ui-accordion-item]


[ui-accordion-item title=<b>Version</b>\040(fig.6)]
The version of the model. Will be encreased with any new release. the version is not editable.
[/ui-accordion-item]


[ui-accordion-item title=<b>Status</b>\040(fig.7)]
**Model Statis:**<br>
<code>draft</code> = in draft state, not released yet<br>
<code>active</code> =  in use and latest released<br>
<code>released</code> = frozen, records points to model version initially released<br>

[/ui-accordion-item]


[ui-accordion-item title=<b>System\040Model</b>\040(fig.8)]
Predefined by system (basic functions needed). Defines if this is a default Model (System Model) or not. Cannot be changed by user.
[/ui-accordion-item]


[ui-accordion-item title=<b>Name</b>\040(fig.9)]
Object Name, full text no limitations.
[/ui-accordion-item]


[ui-accordion-item title=<b>Description</b>\040(fig.10)]
Object Description, full text no limitations
[/ui-accordion-item]


[ui-accordion-item title=<b>Icon</b>\040(fig.11)]
The Object/Model Icon. For the icon shortcodes, please refere to the [UI5 Icon library](https://sapui5.hana.ondemand.com/sdk/test-resources/sap/m/demokit/iconExplorer/webapp/index.html#/overview/SAP-icons)
[/ui-accordion-item]


[ui-accordion-item title=<b>Record\040Status</b>\040(fig.12)]
The record status defines the state of the object record. The options and its translations can be defined free by clicking on the Globe-Icon Figure 12.a<br>
![Record Status](record-status-detail.png?lightbox=1024&cropResize=500,500) {.left}
[/ui-accordion-item]


[ui-accordion-item title=<b>Model\040right</b>\040(fig.13)]
With the parameter Model right, the access right of the model can be selected from a predefined set of user or file rights.<br>
![Model right](model-right-detail.png?lightbox=1024&cropResize=500,500) {.left}
[/ui-accordion-item]

[/ui-accordion]


##### Description
Returns a Variable for the given ident when found. The model is needed to abstract the right values.
...


## Variables

In the Section **Variables** the variables of the model can be added and defined. To add a new variable click on the **+ Add** button (fig.2). To close the left parameter section use the **Back** button (fig.1).
Already added variables will be shown with the icon and name (fig.3). New/drafted variables will be shown without a name only with the default icon (fig.4).

**Overview View**

![Modeler Variables](model-variables.png?lightbox=1024&cropResize=900,900) {.left}

>>> Please be aware that variables cannot be deleted yet.

**Edit View**

![Modeler Variables Detail](model-variables-detail.png?lightbox=1024&cropResize=900,900) {.left}

### General Settings and Default Parameters:

[ui-accordion independent=true open=0]

[ui-accordion-item title=<b>System\040Variable</b>\040(fig.4)]
Predefined by system (basic functions needed). Defines if this is a default Variable (System Variable) or not. Cannot be changed by user.
[/ui-accordion-item]

[ui-accordion-item title=<b>Released</b>\040(fig.5)]
Defines if Variable is already released or not (in draft state)
[/ui-accordion-item]

[ui-accordion-item title=<b>Ident</b>\040(fig.6)]
Human readable ID (unique in context). Can contain only small letters, subline, full numbers, first possition need to be a letter (will automatically change to small if big letters are entered).
[/ui-accordion-item]

[ui-accordion-item title=<b>Name</b>\040(fig.7)]
Variable Name, full text no limitations. Translations can be added with the Globe-Button (fig.7.a).
[/ui-accordion-item]

[ui-accordion-item title=<b>Description</b>\040(fig.8)]
Variable Description, full text no limitations. Translations can be added with the Globe-Button (fig.8.a).
[/ui-accordion-item]

[ui-accordion-item title=<b>Required</b>\040(fig.9)]
Defines if this variable is required or not.
[/ui-accordion-item]

[ui-accordion-item title=<b>Access</b>\040(fig.10)]
**Variable Access Rights:**<br>
<code>Change</code> = write + delete of additional options<br>
<code>Write</code> =  general write access<br>
<code>Hide</code> = Variable hidden in front-end eg. required for a password<br>
<code>Read</code> = general read access<br>
[/ui-accordion-item]


[ui-accordion-item title=<b>Value type</b>\040(fig.11)]
Value Type defines the Datetype of this variable.<br>
**Variable Datatypes:**<br>
<code>Change</code> = write + delete of additional options<br>
<code>Write</code> =  general write access<br>
<code>Hide</code> = Variable hidden in front-end eg. required for a password<br>
<code>Read</code> = general read access<br>
[/ui-accordion-item]

[ui-accordion-item title=<b>Default value type</b>\040(fig.12)]
[/ui-accordion-item]



[/ui-accordion]

## Layout

## Code

### Wokflows

### Services

### History