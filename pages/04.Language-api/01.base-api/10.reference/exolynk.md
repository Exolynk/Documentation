---
title: 'Reference'
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
### Reference
A reference is a Uuid v4 which points towards another record. In special cases this can also point to
a model or an environment. In this cases, this will not displayed correctly within the UI.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Reference::new()\040->\040Reference</code>]

##### Description
Returns a new Reference with a uuid of nil/all zeros.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Reference               | A Reference object |

[/ui-accordion-item]

[ui-accordion-item title=<code>Reference::as_string(Version)\040->\040String</code>]

##### Description
Returns a String with the uuid.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Reference        | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | String                  | A String object |

[/ui-accordion-item]

[ui-accordion-item title=<code>Reference::from_str(String)\040->\040Result&lt;Reference&gt;</code>]

##### Description
Tries to create a new Reference from a string.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String                  | A uuid string |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Result&lt;Reference&gt; | The reference or an error |

[/ui-accordion-item]
[/ui-accordion]