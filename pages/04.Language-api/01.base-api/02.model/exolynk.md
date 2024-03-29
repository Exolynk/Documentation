---
title: 'Model'
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
### Model
A model represents a record type or a database table within the system. The model defines, which
custom variables a record has and stores the workflows and services for these specific record types.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Getter</code>]

##### Parameters
> | name      | data type               | description                                                         |
> |-----------|-------------------------|---------------------------------------------------------------------|
> | `uuid`    | String                  | The unique uuid of the model                                        |
> | `ident`   | Ident                   | The unique textual identifier for the model                         |
> | `version` | Version                 | The actual version of the model                                     |
> | `status`  | String                  | The status of the model                                             |
> | `icon`    | String                  | The icon of the model for the previews                              |
> | `layout`  | String                  | The layout in html to define how the records should be visuualized  |
> | `system`  | Bool                    | Implies if this model is defined by the system or customer specific |
> | `name`    | Language                | The display name of the model                                       |
> | `description`   | Language          | The display description of the model                                |
> | `record_status` | Selection         | Defines the different status options the record should have         |
> | `variables`     | &lt;Variable&gt;  | The list of variables of this model                                 |

[/ui-accordion-item]

[ui-accordion-item title=<code>Setter</code>]

##### Parameters
> | name            | data type          | description                                                 |
> |-----------------|--------------------|-------------------------------------------------------------|
> | `icon`          | String             | The icon of the model (either Icon or String)               |
> | `layout`        | String             | The html layout of the model for its records                |
> | `name`          | Language           | Set the display name of the model                           |
> | `description`   | Language           | Set the display descritption of the model                   |
> | `record_status` | Selection          | Defines the different status options the record should have |
> | `variables`     | &lt;Variable&gt;   | Set the list of variables of this model                     |

[/ui-accordion-item]

[ui-accordion-item title=<code>model.create_record()\040->\040Result&lt;Record&gt;</code>]

##### Description
Creates a new record from the model. Parameter 0 is always a reference to the own object

##### Parameters
> | parameter | data type            | description                                                    |
> |-----------|----------------------|----------------------------------------------------------------|
> | 0         | Self / Model         | A reference to the own object                                  |
> | 1         | Ident \| String      | Define the ident name of the new record                        |
> | 2         | Version \| String    | Set the version of the new record                              |
> | 3         | Language \| String   | Set the name of the new record (if string language is per default EN) |
> | 4         | Language \| String   | Set the description of the new record (if string language is per default EN) |

[/ui-accordion-item]
[/ui-accordion]