---
title: 'Variable'
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
### Variable
A variable defines how a value should be handled, which type it has, etc. It's used mostly in the model
to define how customer specific fields look like.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Getter</code>]

##### Parameters
> | name      | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `ident`   | String                  | The unique textual identifier for the variable  |
> | `system`  | Bool                    | Implies if this variable is defined by the system or customer specific  |
> | `released`| Bool                    | Shows if the variable has been released and deployed to the db schema  |
> | `required`| Bool                    | Shows if the variable is required to the user in edit mode |
> | `access`  | Access                  | Shows with which access rights the variable is shown to the user |
> | `value`   | Value                   | The value type of the variable and default value when created |
> | `name`    | Language                | The display name of the variable |
> | `description`   | Language          | The display description of the variable |

[/ui-accordion-item]

[ui-accordion-item title=<code>Setter</code>]

##### Parameters
> | name      | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `ident`   | String                  | The unique textual identifier for the variable  |
> | `required`| Bool                    | Shows if the variable is required to the user in edit mode |
> | `access`  | Access                  | Shows with which access rights the variable is shown to the user |
> | `value`   | Value                   | The value type of the variable and default value when created |
> | `name`    | Language                | The display name of the variable |
> | `description`   | Language          | The display description of the variable |

[/ui-accordion-item]

[ui-accordion-item title=<code>variable.new(Ident,\040Value)\040->\040Result&lt;Variable&gt;</code>]

##### Description
Creates a new variable with an ident and the value.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Ident                   | The ident of the new variable |
> | 1         | Value                   | The value of the new variable |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Result&lt;Variable&gt;  | The newly created variable |

[/ui-accordion-item]

[ui-accordion-item title=<code>variable.clone(Variable)\040->\040Variable</code>]

##### Description
Clones a variable and returns a new one with independent of the original one.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Variable         | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Variable                | The cloned new idendependet Variable |

[/ui-accordion-item]


[/ui-accordion]