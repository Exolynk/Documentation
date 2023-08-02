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
> | Version                 | A Version object                                                      |

[/ui-accordion-item]

[ui-accordion-item title=<code>version.to_string()\040->\040String</code>]

##### Description
Returns a String with the version.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | String                  | A String object                                                       |

[/ui-accordion-item]

[ui-accordion-item title=<code>version.next_version()</code>]

##### Description
Counts version one number up.

[/ui-accordion-item]
[/ui-accordion]