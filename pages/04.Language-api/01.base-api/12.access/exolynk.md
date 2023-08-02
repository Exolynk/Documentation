---
title: 'Access'
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
### Access
Access is a enum to control how variables can be seen and changed within the UI and on the server side

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Variants</code>]

##### Variants
> | data type                   | description                                                               |
> |-----------------------------|---------------------------------------------------------------------------|
> | Access::Write               | Allows the user to write/change the value of an input                     |
> | Access::Change              | Allows the user to change the field e.g. insert new options               |
> | Access::Read                | Allows the user to just read the value                                    |
> | Access::Hide                | Hide the value from the user. Be aware this is only for the ui rendering! |

[/ui-accordion-item]

[ui-accordion-item title=<code>Access::from_str(String)\040->\040Access</code>]

##### Description
Creates the access enum from a string. When a wrong string is given, it returns Access::Hide as default.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String                  | The access name as String |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Access                  | The access struct generated from the string                           |

[/ui-accordion-item]

[ui-accordion-item title=<code>access.to_string()\040->\040String</code>]

##### Description
Returns a String whith the access value.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | String                  | A String with the access                                              |

[/ui-accordion-item]
[/ui-accordion]