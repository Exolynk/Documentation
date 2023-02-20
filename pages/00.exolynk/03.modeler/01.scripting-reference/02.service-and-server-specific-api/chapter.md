---
title: 'Service / Server Specific API'
taxonomy:
    category: docs
process:
    twig: true
---

[TOC]

## Service / Server Specific API
The following server APIs are only availble in services and executed on the server.

------------------------------------------------------------------------------------------
### test
### server
Generale functions to interact with the server.

------------------------------------------------------------------------------------------
### server::db
Generale functions to interact with the database of the server.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>server::db::get_environment()\040->\040async\040Result&lt;Environment&gt;</code>]
##### Description
Returns the actual environment the user is logged into.
##### Returns
> | data type                       | description                                                 |
> |---------------------------------|-------------------------------------------------------------|
> | async Result&lt;Environment&gt; | Returns the actual the environment of the user |
[/ui-accordion-item]

[ui-accordion-item title=<code>server::db::get_record(String)\040->\040async\040Result&lt;Record&gt;</code>]
##### Description
Fetches a record from the database.
##### Parameters
> | parameter | data type               | description                                       |
> |-----------|-------------------------|---------------------------------------------------|
> | 0         | String                  | The uuid of the record to query |
##### Returns
> | data type                  | description                                                |
> |----------------------------|------------------------------------------------------------|
> | async Result&lt;Record&gt; | The answer from the executed service |
[/ui-accordion-item]

[ui-accordion-item title=<code>server::db::insert_record(Record)\040->\040async\040Result&lt;()&gt;</code>]
##### Description
Inserts a new Record into the database.
##### Parameters
> | parameter | data type               | description                                       |
> |-----------|-------------------------|---------------------------------------------------|
> | 0         | Record                  | The Record which should be inserted into the db |
##### Returns
> | data type                  | description                                                |
> |----------------------------|------------------------------------------------------------|
> | async Result&lt;()&gt; | Thorws an error when something went wrong |
[/ui-accordion-item]

[ui-accordion-item title=<code>server::db::update_record(Record)\040->\040async\040Result&lt;()&gt;</code>]
##### Description
Updates a Record which already exist in the database. This also informs all subscribed clients about this change.
##### Parameters
> | parameter | data type               | description                                       |
> |-----------|-------------------------|---------------------------------------------------|
> | 0         | Record                  | The Record which should be updated |
##### Returns
> | data type                  | description                                                |
> |----------------------------|------------------------------------------------------------|
> | async Result&lt;()&gt; | Thorws an error when something went wrong |
[/ui-accordion-item]

[/ui-accordion]