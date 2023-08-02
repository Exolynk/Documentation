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
> | Table                   | A Table object                                                        |

[/ui-accordion-item]


[ui-accordion-item title=<code>table.get_value(Integer,\040Ident)\040->\040Option&lt;Value&gt;</code>]

##### Description
Get a value from a row and column.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Integer                 | The row number                                                        |
> | 1         | Ident                   | The ident of the column                                               |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Value&gt;     | The value of the cell when found                                      |

[/ui-accordion-item]

[ui-accordion-item title=<code>table.set_value(Integer,\040Ident,\040Value)\040->\040Result&lt;()&gt;</code>]

##### Description
Set a value into a row and column.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Integer                 | The row number                                                        |
> | 1         | Ident                   | The ident of the column                                               |
> | 2         | Value                   | The value to set                                                      |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Result&lt;()&gt;        | Returns error when input was wrong                                    |
[/ui-accordion-item]

[ui-accordion-item title=<code>table.remove(Integer)</code>]

##### Description
Removes the given row.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Integer                 | The row number to delete                                              |

[/ui-accordion-item]


[ui-accordion-item title=<code>table.clear()</code>]

##### Description
Removes all rows and columns

[/ui-accordion-item]


[ui-accordion-item title=<code>table.len()\040->\040Integer</code>]

##### Description
Returns the amount of columns inside the table.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Integer                 | The number of columns                                                 |

[/ui-accordion-item]


[ui-accordion-item title=<code>table.is_empty()\040->\040bool</code>]

##### Description
Returns true, when there are no entries inside the table.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | bool                    | Is the table empty?                                                   |

[/ui-accordion-item]
[/ui-accordion]