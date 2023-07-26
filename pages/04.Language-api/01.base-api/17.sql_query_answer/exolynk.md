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
[ui-accordion-item title=<code>SqlQueryAnswer::get_records(Self)\040->\040Option&lt;Vec&lt;Record&gt;&gt;</code>]

##### Description
Returns a list with the records returned from the database query.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / SqlQueryAnswer   | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Vec&lt;Record&gt;&gt; | The records if available |

[/ui-accordion-item]


[ui-accordion-item title=<code>SqlQueryAnswer::get_columns(Self)\040->\040Option&lt;Vec&lt;Object&gt;&gt;</code>]

##### Description
Returns a vector of objects, which contain the columns requested.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / SqlQueryAnswer   | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Vec&lt;Object&gt;&gt; | A list of objects with the columns inside |

[/ui-accordion-item]
[/ui-accordion]