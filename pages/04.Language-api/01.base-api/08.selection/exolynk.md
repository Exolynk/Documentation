---
title: 'Selection'
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
### Selection
A selection is mostly used as dropdown fields to select one or multiple options.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Selection::new()\040->\040Selection</code>]

##### Description
Returns a empty Selection object.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Selection               | A Selection object |

[/ui-accordion-item]

[ui-accordion-item title=<code>Selection::new_languages()\040->\040Selection</code>]

##### Description
Returns a Selection object, where the defaul languages (en, de, it, fr) are set with the translations.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Selection               | A Selection object |

[/ui-accordion-item]

[ui-accordion-item title=<code>selection.get(String)\040->\040Option&lt;Language&gt;</code>]

##### Description
Returns the Language object for the defined option, when found
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String                  | The option ident |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&gt;Language&gt;  | Returns the language if found |

[/ui-accordion-item]

[ui-accordion-item title=<code>selection.insert(String,\040Language)\040->\040Result&lt;()&gt;</code>]

##### Description
Inserts a new option to the selection with the given ident and Language.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String                  | The option ident  |
> | 1         | Language                | The language text |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Result&lt;()&gt;        | Returns error when input was wrong                                    |
[/ui-accordion-item]

[ui-accordion-item title=<code>selection.get_selected()\040->\040Vec&lt;String&gt;</code>]

##### Description
Returns the idents of the selected options
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Vec&gt;String&gt;       | Returns a list with the selected idents |

[/ui-accordion-item]

[ui-accordion-item title=<code>selection.get_selected_single()\040->\040String</code>]

##### Description
Returns the idents of the selected options
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | String                  | Returns the first selected ident                                      |

[/ui-accordion-item]

[ui-accordion-item title=<code>selection.set_selected(Vec&lt;String&gt;)</code>]

##### Description
Sets the selected options of the given selection
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Vec&lt;String&gt;       | The selected option idents in a list  |

[/ui-accordion-item]
[/ui-accordion]