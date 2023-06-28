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
> | List.                   | A List object |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::new_restriction(Value)\040->\040List</code>]

##### Description
Returns a List with the given restriction typ in place.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 1         | Value                   | A Value to define the restriction type and default value |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | List                    | A List object |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::set_restriction(Self,\040Option&lt;Value&gt;)</code>]

##### Description
Sets or removes the restriction of the list.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / List.            | A reference to the own object |
> | 1         | Option&lt;Value&gt;     | The restriction to set or None for no restriction |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::get_restiction(Self)\040->\040Option&lt;Value&gt;</code>]

##### Description
Gets the actual restriction of the list.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / List             | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Value&gt;     | A Value which is the actual restriction |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::add(Self,\040Value)</code>]

##### Description
Adds a new value to the list collection.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Selection        | A reference to the own object |
> | 1         | Value                   | The value which should be added to the list |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::get(Self,\040usize)\040->\040Option&lt;Value&gt;</code>]

##### Description
Gets an entry from the list
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / List             | A reference to the own object |
> | 1         | usize                   | The position in the list we want the entry of |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Value&gt;     | A Value which is the actual restriction |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::replace(Self,\040usize,\040Value)</code>]

##### Description
Replaces an entry at the defined position.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / List             | A reference to the own object |
> | 1         | usize                   | The index of the entry inside the list to replace |
> | 2         | Value                   | The new value to replace the old one with |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::remove(Self,\040usize)</code>]

##### Description
Remove an entry at the given positon.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / List             | A reference to the own object |
> | 1         | usize                   | Position where the entry should be removed  |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::clear(Self)</code>]

##### Description
Clears the complete list.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / List             | A reference to the own object |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::len(Self)\040->\040usize</code>]

##### Description
Returns the length of the list
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / List             | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | usize                   | Length of the list |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::is_empty(Self)\040->\040bool</code>]

##### Description
Returns if the list is empty or has entries inside.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / List             | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | bool                    | True when empty false when it has entries |

[/ui-accordion-item]
[/ui-accordion]