---
title: 'Env Detail Settings'
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
### Environment Detail Settings
A map of keys and values wich stores detail settings for the system.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Settings::new()\040->\040Settings</code>]

##### Description
Returns a empty Settings object.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Settings                | A Settings object                                                     |

[/ui-accordion-item]

[ui-accordion-item title=<code>settings.get(String)\040->\040Option&lt;String&gt;</code>]

##### Description
Returns the specific setting if found.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String                  | The setting ident                                                     |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&gt;String&gt;    | Returns the settings as string                                        |

[/ui-accordion-item]

[ui-accordion-item title=<code>settings.insert(String,\040String)\040->\040Result&lt;()&gt;</code>]

##### Description
Inserts a new setting in the settings object. An existing setting with the same ident will be overwritten.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String                  | The settings ident                                                    |
> | 1         | String                  | The detail setting                                                    |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Result&lt;()&gt;        | Returns error when input was wrong                                    |
[/ui-accordion-item]

[ui-accordion-item title=<code>settings.remove(String)\040->\040Result&lt;()&gt;</code>]

##### Description
Removes a specific setting from the object.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String                  | The setting ident to be removed                                       |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Result&lt;()&gt;        | Returns error when input was wrong                                    |
[/ui-accordion-item]
[/ui-accordion]