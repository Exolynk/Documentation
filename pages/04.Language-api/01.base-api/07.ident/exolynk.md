---
title: 'Ident'
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
### Ident
An Identifier is like a String but only allows small letters, underscore and numbers. The first character
needs to be a small letter. When creating an ident from a String, it automatically transforms the String
to a fitting ident.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Ident::new(String)\040->\040Ident</code>]

##### Description
Returns a new Ident.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String                  | A ident as String formated |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Ident                   | A Ident object |

[/ui-accordion-item]

[ui-accordion-item title=<code>Ident::as_string(Ident)\040->\040String</code>]

##### Description
Returns a String whith the ident value.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Ident.           | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | String.                 | A String object |

[/ui-accordion-item]
[/ui-accordion]