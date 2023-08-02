---
title: 'Language'
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
### Language
A language is an object with holds text translated in multiple languages.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Language::new()\040->\040Language</code>]

##### Description
Returns a empty Language object.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Language                | A Language object |

[/ui-accordion-item]

[ui-accordion-item title=<code>Language::from(Any)\040->\040Result\040&lt;Language&gt;</code>]

##### Description
Returns a Language object with the english languauge set.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String \| Language      | The text in the english language to initalize the Langauge object with |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Language                | A Language object |

[/ui-accordion-item]

[ui-accordion-item title=<code>Language::get(Self,\040String)\040->\040Option&lt;String&gt;</code>]

##### Description
Returns the text in the defined language if found.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Language         | A reference to the own object |
> | 1         | String                  | The language ident (en, de, fr, it, ...) |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&gt;Self&gt;      | Returns the text in the defined language if found |

[/ui-accordion-item]

[ui-accordion-item title=<code>Language::set(Self,\040String,\040String)</code>]

##### Description
Sets the language text for the given language ident.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Language         | A reference to the own object |
> | 1         | String                  | The language ident (en, de, fr, it, ...) |
> | 2         | String                  | The language text |

[/ui-accordion-item]
[/ui-accordion]