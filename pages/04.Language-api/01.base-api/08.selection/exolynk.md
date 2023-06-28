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

[ui-accordion-item title=<code>Selection::get(Self,\040String)\040->\040Option&lt;Language&gt;</code>]

##### Description
Returns the Language object for the defined option, when found
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Selection        | A reference to the own object |
> | 1         | String                  | The option ident |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&gt;Language&gt;  | Returns the language if found |

[/ui-accordion-item]

[ui-accordion-item title=<code>Selection::insert(Self,\040String,\040Language)</code>]

##### Description
Inserts a new option to the selection with the given ident and Language.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Selection        | A reference to the own object |
> | 1         | String                  | The option ident  |
> | 2         | Language                | The language text |

[/ui-accordion-item]

[ui-accordion-item title=<code>Selection::get_mode(Self)\040->\040SelectionMode</code>]

##### Description
Returns the SelectionMode enum for this selection
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Selection        | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | SelectionMode           | Returns the selection mode |

[/ui-accordion-item]

[ui-accordion-item title=<code>Selection::set_mode(Self,\040SelectionMode)</code>]

##### Description
Defines with selection mode (Single, Multi, Show) the selection should use.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Selection        | A reference to the own object |
> | 1         | SelectionMode           | Set the mode |

[/ui-accordion-item]

[ui-accordion-item title=<code>Selection::get_selected(Self)\040->\040Vec&lt;String&gt;</code>]

##### Description
Returns the idents of the selected options
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Selection        | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Vec&gt;Language&gt;     | Returns a list with the selected idents |

[/ui-accordion-item]

[ui-accordion-item title=<code>Selection::set_selected(Self,\040Vec&lt;String&gt;)</code>]

##### Description
Sets the selected options of the given selection
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Selection        | A reference to the own object |
> | 1         | Vec&lt;String&gt;       | The selected option idents in a list  |

[/ui-accordion-item]
[/ui-accordion]