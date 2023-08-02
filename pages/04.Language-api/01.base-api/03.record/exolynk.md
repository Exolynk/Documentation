---
title: 'Record'
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
### Record
A record is a single dataset inside the system. It is stored as row within the internal database inside
a table which is uunique for this record type / model.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Getter</code>]

##### Parameters
> | name      | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `uuid`    | String                  | The unique uuid of the record  |
> | `ident`   | Ident                   | The unique textual identifier for the record  |
> | `version` | Version                 | The version for the record  |
> | `model`   | String                  | The uuid of the model as String  |
> | `status`  | Ident                   | The status of the record  |
> | `released`| Bool                    | Implies if this model is released and not changeable anymore |
> | `name`    | Language                | The display name of the record |
> | `description`   | Language          | The display description of the record |
> | `right`  | Reference                | The access right of the record  |
> | `icon`   | String                   | The icon of the record  |

[/ui-accordion-item]

[ui-accordion-item title=<code>Setter</code>]

##### Parameters
> | name      | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `uuid`    | String                  | Set the uuid. This fails if the uuid has a wrong format  |
> | `ident`   | Ident                   | Set the ident for the record, converts automatically to a valid form  |
> | `status`  | Ident                   | Set the status for the record  |
> | `released`| Bool                    | Is the record released and not changeable anymore  |
> | `name`    | Language                | Set the display name of the record |
> | `description`   | Language          | Set the display descritption of the record |
> | `right`  | Reference                | The access right of the record  |
> | `icon`   | String                   | The icon of the record  |

[/ui-accordion-item]

[ui-accordion-item title=<code>record.set_value(Ident,\040Value)\040->\040&lt;Result&lt;</code>]

##### Description
Sets the value inside of a record. Providing the Ident "name", "description", "status", sets the standard record values. All other Idents will set a custom value.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Ident                   | Define which value should be set |
> | 1         | Value                   | The value which should be set |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Result | The result |

[/ui-accordion-item]

[ui-accordion-item title=<code>record.get_value(Ident)\040->\040&lt;Result&lt;</code>]

##### Description
Returns a Value for the given ident when found.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Ident                   | The Ident we want to have the value for |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Result | The result |

[/ui-accordion-item]

[ui-accordion-item title=<code>Record::get_variable(Model,\040Ident)\040->\040Option&lt;Variable&gt;</code>]

##### Description
Returns a Variable for the given ident when found. The model is needed to abstract the right values.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Model                   | A reference to the model this record belongs to |
> | 1         | Ident                   | The Ident we want to have the variable for |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Variable&gt;  | The variable when found |

[/ui-accordion-item]
[/ui-accordion]