---
title: 'Environment'
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
### Environment
The environment is the system root and holds all models, records, configurations etc.
Global settings, translations are stored within this object.



[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Getter</code>]

##### Parameters
> | name      | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `uuid`    | String                  | The unique uuid for the environment  |
> | `ident`   | Ident                   | The unique textual identifier for the environment  |
> | `name`    | Language                | The display name of the environment |
> | `status`  | String                  | The status of the environment  |
> | `languages`     | Selection         | The supported languages of the environment  |
> | `translations`  | Selection         | The translations of the environment  |
> | `settings`      | Settings          | The detail settings of the environment  |

[/ui-accordion-item]

[ui-accordion-item title=<code>Setter</code>]

##### Parameters
> | name           | data type          | description                                                  |
> |----------------|--------------------|--------------------------------------------------------------|
> | `name`         | Language           | Set the display name of the environment |
> | `languages`    | Selection          | Set the supported languages for this environment  |
> | `translations` | Selection          | Set the translations for this environment  |
> | `settings`     | Settings           | Set the detail settin<code><code>Getter</code></code>gs of the environment  |

[/ui-accordion-item]
[/ui-accordion]