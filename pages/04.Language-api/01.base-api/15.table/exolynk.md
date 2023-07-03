---
title: 'Table'
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
### Table
A variable wich stores a table with multiple columns and rows.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Table::new()\040->\040Table</code>]

##### Description
Creates a new emtpy table.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Table.                  | A Table object |

[/ui-accordion-item]


[ui-accordion-item title=<code>Table::get_value(Self,\040usize,\040Ident)\040->\040Option&lt;Value&gt;</code>]

##### Description
Get a value from a row and column.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Table            | A reference to the own object |
> | 1         | usize                   | The row number |
> | 2         | Ident                   | The ident of the column |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Value&gt;     | The value of the cell when found |

[/ui-accordion-item]

[ui-accordion-item title=<code>Table::set_value(Self,\040usize,\040Ident,\040Value)</code>]

##### Description
Set a value into a row and column.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Table            | A reference to the own object |
> | 1         | usize                   | The row number |
> | 2         | Ident                   | The ident of the column |
> | 3         | Value                   | The value to set |

[/ui-accordion-item]



[ui-accordion-item title=<code>Table::remove(Self,\040usize)</code>]

##### Description
Removes the given row.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Table            | A reference to the own object |
> | 1         | usize                   | The row number to delete |

[/ui-accordion-item]


[ui-accordion-item title=<code>Table::clear(Self)</code>]

##### Description
Removes all rows and columns

[/ui-accordion-item]


[ui-accordion-item title=<code>Table::len(Self)\040->usize</code>]

##### Description
Returns the amount of columns inside the table.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | usize                   | The number of columns |

[/ui-accordion-item]


[ui-accordion-item title=<code>Table::is_empty(Self)\040->bool</code>]

##### Description
Returns true, when there are no entries inside the table.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | bool                    | Is the table empty? |

[/ui-accordion-item]
[/ui-accordion]