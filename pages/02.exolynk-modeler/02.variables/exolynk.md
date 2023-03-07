---
title: Variables
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
##### Description
Predefined by system (basic functions needed). Defines if this is a default Variable (System Variable) or not. Cannot be changed by user.
[/ui-accordion-item]

[ui-accordion-item title=<b>Released</b>\040(fig.5)]
##### Description
Defines if Variable is already released or not (in draft state)
[/ui-accordion-item]

[ui-accordion-item title=<b>Ident</b>\040(fig.6)]
##### Description
Human readable ID (unique in context). Can contain only small letters, subline, full numbers, first possition need to be a letter (will automatically change to small if big letters are entered).
[/ui-accordion-item]

[ui-accordion-item title=<b>Name</b>\040(fig.7)]
##### Description
Variable Name, full text no limitations. Translations can be added with the Globe-Button (fig.7.a).
[/ui-accordion-item]

[ui-accordion-item title=<b>Description</b>\040(fig.8)]
##### Description
Variable Description, full text no limitations. Translations can be added with the Globe-Button (fig.8.a).
[/ui-accordion-item]

[ui-accordion-item title=<b>Required</b>\040(fig.9)]
##### Description
Defines if this variable is required or not.
[/ui-accordion-item]

[ui-accordion-item title=<b>Access</b>\040(fig.10)]
##### Variable Access Rights<br>
<code>Change</code> = write + change of additional options<br>
<code>Write</code> =  general write access<br>
<code>Hide</code> = Variable hidden in front-end eg. required for a password<br>
<code>Read</code> = general read access<br>
[/ui-accordion-item]


[ui-accordion-item title=<b>Value type</b>\040(fig.11)]
Value Type defines the Datetype of this variable.<br>
**Variable Datatypes:**<br>
<code>Bool</code> = <br>
<code>Float</code> =  <br>
<code>Ident</code> = <br>
<code>Integer</code> = <br>
<code>Language</code> = fulltext translatable for each language<br>
<code>List</code> = Setting just visible if "change" access right<br>
<code>Reference</code> = Reference to another record (UUID internal) will alwys displayed Ident<br>
<code>Selection</code> = selectionlist and dropdown<br>
<code>String</code> = fulltext no limitations<br>
<code>Version</code> = full numbers<br>
[/ui-accordion-item]

[ui-accordion-item title=<b>Default value type</b>\040(fig.12)]
[/ui-accordion-item]

[/ui-accordion]

## Layout

## Code

### Wokflows

### Services

### History