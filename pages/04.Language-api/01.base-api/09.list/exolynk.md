---
title: 'List'
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
### List
A can store multiple values at once. A list can be restricted to a specific value typ.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>List::new()\040->\040List</code>]

##### Description
Returns a empty List with no typ restriction.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | List                    | A List object                                                         |

[/ui-accordion-item]

[ui-accordion-item title=<code>list.add(Value)</code>]

##### Description
Adds a new value to the list collection.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Value                   | The value which should be added to the list (can also be a String, Ident, Icon,..) |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Result&lt;()&gt;        | Returns error when input was wrong                                    |
[/ui-accordion-item]

[ui-accordion-item title=<code>list.get(Integer)\040->\040Option&lt;Value&gt;</code>]

##### Description
Gets an entry from the list
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Integer                 | The position in the list we want the entry of |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Value&gt;     | A Value which is the actual restriction                               |

[/ui-accordion-item]

[ui-accordion-item title=<code>list.replace(Integer,\040Any)\040->\040Result&lt;()&gt;</code>]

##### Description
Replaces an entry at the defined position.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Integer                 | The index of the entry inside the list to replace                     |
> | 1         | Any                     | The new value to replace the old one with                             |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Result&lt;()&gt;        | Returns error when input was wrong                                    |
[/ui-accordion-item]

[ui-accordion-item title=<code>list.remove(Integer)\040->\040Result&lt;()&gt;</code>]

##### Description
Remove an entry at the given positon.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Integer                 | Position where the entry should be removed                            |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Result&lt;()&gt;        | Returns error when input was wrong                                    |
[/ui-accordion-item]

[ui-accordion-item title=<code>list.clear()</code>]

##### Description
Clears the complete list.
[/ui-accordion-item]

[ui-accordion-item title=<code>list.len()\040->\040usize</code>]

##### Description
Returns the length of the list
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | usize                   | Length of the list |

[/ui-accordion-item]

[ui-accordion-item title=<code>list.is_empty()\040->\040bool</code>]

##### Description
Returns if the list is empty or has entries inside.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | bool                    | True when empty false when it has entries                             |

[/ui-accordion-item]
[/ui-accordion]