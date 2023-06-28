---
title: 'Version'
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
### Version
A version object. Right now it only allows nubered version (e.g. 0, 1, 2, 3, ...) in future
more version formats are planned.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Version::new(String)\040->\040Version</code>]

##### Description
Returns a new Version.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String                  | A numer as String formated |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Version                 | A Version object |

[/ui-accordion-item]

[ui-accordion-item title=<code>Version::as_string(Version)\040->\040String</code>]

##### Description
Returns a String with the version.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Version          | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | String.                 | A String object |

[/ui-accordion-item]
[/ui-accordion]