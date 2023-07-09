---
title: 'DateTime'
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
### DateTime
A variable wich stores the date and time in the format: ```yyyy-MM-dd, HH:mm:ss``` as a string.


[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>DateTime::new()\040->\040DateTime</code>]

##### Description
Creates a new emtpy table.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | DateTime                | A DateTime object |

[/ui-accordion-item]


[ui-accordion-item title=<code>DateTime::as_string(Self)\040->\040String</code>]

##### Description
Get a value from a row and column.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / DateTime         | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | String                  | DateTime as string in format ```yyyy-MM-dd, HH:mm:ss``` |

[/ui-accordion-item]

[ui-accordion-item title=<code>DateTime::to_local_string(Self)\040->\040String</code>]

##### Description
Get a value to local string.

##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / DateTime         | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | String                  | DateTime as string in format ```yyyy-MM-dd, HH:mm:ss``` |

[/ui-accordion-item]


[ui-accordion-item title=<code>DateTime::from_local_string(String)\040->\040Result&lt;DateTime&gt;</code>]

##### Description
Get a value from local string.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String / DateTime         | DateTime as string in format ```yyyy-MM-dd, HH:mm:ss``` |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | DateTime                | A DateTime object                                                     |

[/ui-accordion-item]
[/ui-accordion]