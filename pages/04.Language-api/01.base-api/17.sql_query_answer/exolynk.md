---
title: 'SqlQueryAnswer'
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
### SqlQueryAnswer
A struct which is returned from a successfull executed SqlQuery. It either contains full records or defined record columns.


[ui-accordion independent=true open=none]

[ui-accordion-item title=<code>Variants</code>]

##### Variants
> | data type                   | description                                                               |
> |-----------------------------|---------------------------------------------------------------------------|
> | SqlQueryAnswer::Records     | List if records returned from an SQL query                                |
> | SqlQueryAnswer::Columns     | Mutliple columns returned from an SQL query                               |

[/ui-accordion-item]

[ui-accordion-item title=<code>sqlqueryanswer.get_records()\040->\040Option&lt;Vec&lt;Record&gt;&gt;</code>]

##### Description
Returns a list with the records returned from the database query.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Vec&lt;Record&gt;&gt; | The records if available |

[/ui-accordion-item]


[ui-accordion-item title=<code>sqlqueryanswer.get_columns()\040->\040Option&lt;Vec&lt;Object&gt;&gt;</code>]

##### Description
Returns a vector of objects, which contain the columns requested.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Vec&lt;Object&gt;&gt; | A list of objects with the columns inside |

[/ui-accordion-item]
[/ui-accordion]