---
title: 'Service / Server Specific API'
taxonomy:
    category: docs
process:
    twig: false
---

[TOC]

## Service / Server Specific API
The following server APIs are only availble in services and executed on the server.

------------------------------------------------------------------------------------------
### server
Generale functions to interact with the server.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>server::get_environment()\040->\040Environment</code>]
##### Description
Returns the actual environment the user is logged into.
##### Returns
> | data type                       | description                                                 |
> |---------------------------------|-------------------------------------------------------------|
> | Environment                     | Returns the actual the environment of the user |
[/ui-accordion-item]

[ui-accordion-item title=<code>server::get_user()\040->\040Record</code>]
##### Description
Returns the actual user which has triggered the service.
##### Returns
> | data type                       | description                                                 |
> |---------------------------------|-------------------------------------------------------------|
> | Record                          | The user record |
[/ui-accordion-item]

[ui-accordion-item title=<code>server::get_record()\040->\040Option&lt;Record&gt;</code>]
##### Description
Returns the actual record for which the service has been triggered.
##### Returns
> | data type                       | description                                                 |
> |---------------------------------|-------------------------------------------------------------|
> | Option<Record>                  | The record |
[/ui-accordion-item]

[ui-accordion-item title=<code>server::get_model()\040->\040Option&lt;Model&gt;</code>]
##### Description
Returns the actual model for which the service has been triggered.
##### Returns
> | data type                       | description                                                 |
> |---------------------------------|-------------------------------------------------------------|
> | Option<Model>                   | The model |
[/ui-accordion-item]
[/ui-accordion]


------------------------------------------------------------------------------------------
### server::db
Generale functions to interact with the database of the server.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>server::db::get_record(Reference)\040->\040async\040Result&lt;Record&gt;</code>]
##### Description
Fetches a record from the database.
##### Parameters
> | parameter | data type               | description                                       |
> |-----------|-------------------------|---------------------------------------------------|
> | 0         | String\|Reference                  | The uuid of the record to query |
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

[ui-accordion-item title=<code>server::db::update_record_value(String,\040Ident,\040Value)\040->\040async\040Result&lt;()&gt;</code>]
##### Description
Updates a Record value in the database. This also informs all subscribed clients about this change.
##### Parameters
> | parameter | data type               | description                                       |
> |-----------|-------------------------|---------------------------------------------------|
> | 0         | String                  | The uuid of the record be updated |
> | 1         | Ident                   | The ident of the value to update |
> | 2         | Value                   | The new value which should be applied to the record |
##### Returns
> | data type                  | description                                                |
> |----------------------------|------------------------------------------------------------|
> | async Result&lt;()&gt; | Thorws an error when something went wrong |
[/ui-accordion-item]

[ui-accordion-item title=<code>server::db::add_inbox(String,\040String)\040->\040async\040Result&lt;()&gt;</code>]
##### Description
Adds a record into the inbox of a user. This also informs all subscribed clients about this change.
##### Parameters
> | parameter | data type               | description                                       |
> |-----------|-------------------------|---------------------------------------------------|
> | 0         | String                  | The uuid of the user |
> | 1         | String                  | The uuid of the record to add into the inbox |
##### Returns
> | data type                  | description                                                |
> |----------------------------|------------------------------------------------------------|
> | async Result&lt;()&gt;     | Thorws an error when something went wrong |
[/ui-accordion-item]

[ui-accordion-item title=<code>server::db::remove_inbox(String,\040String)\040->\040async\040Result&lt;()&gt;</code>]
##### Description
Removes a record from the inbox of a user. This also informs all subscribed clients about this change.
##### Parameters
> | parameter | data type               | description                                       |
> |-----------|-------------------------|---------------------------------------------------|
> | 0         | String                  | The uuid of the user |
> | 1         | String                  | The uuid of the record to remove from the inbox |
##### Returns
> | data type                  | description                                                |
> |----------------------------|------------------------------------------------------------|
> | async Result&lt;()&gt;     | Thorws an error when something went wrong |
[/ui-accordion-item]

[ui-accordion-item title=<code>server::db::add_favorite(String,\040String)\040->\040async\040Result&lt;()&gt;</code>]
##### Description
Adds a record into the favorite container of a user. This also informs all subscribed clients about this change.
##### Parameters
> | parameter | data type               | description                                       |
> |-----------|-------------------------|---------------------------------------------------|
> | 0         | String                  | The uuid of the user |
> | 1         | String                  | The uuid of the record to add into the favorites |
##### Returns
> | data type                  | description                                                |
> |----------------------------|------------------------------------------------------------|
> | async Result&lt;()&gt;     | Thorws an error when something went wrong |
[/ui-accordion-item]

[ui-accordion-item title=<code>server::db::remove_favorite(String,\040String)\040->\040async\040Result&lt;()&gt;</code>]
##### Description
Removes a record from the favorites of a user. This also informs all subscribed clients about this change.
##### Parameters
> | parameter | data type               | description                                       |
> |-----------|-------------------------|---------------------------------------------------|
> | 0         | String                  | The uuid of the user |
> | 1         | String                  | The uuid of the record to remove from the favorites |
##### Returns
> | data type                  | description                                                |
> |----------------------------|------------------------------------------------------------|
> | async Result&lt;()&gt;     | Thorws an error when something went wrong |
[/ui-accordion-item]

[ui-accordion-item title=<code>server::db::reset_password(String,\040String)\040->\040async\040Result&lt;()&gt;</code>]
##### Description
Resets the password for the given user. The needs to have the `password_reset` right.
##### Parameters
> | parameter | data type               | description                                       |
> |-----------|-------------------------|---------------------------------------------------|
> | 0         | String                  | The uuid of the user to reset the password for |
> | 1         | String                  | The new password to set for the user |
##### Returns
> | data type                  | description                                                |
> |----------------------------|------------------------------------------------------------|
> | async Result&lt;()&gt;     | Thorws an error when something went wrong |
[/ui-accordion-item]

[ui-accordion-item title=<code>server::db::get_model(String)\040->\040async\040Result&lt;Model&gt;</code>]
##### Description
Fetches a model from the database.
##### Parameters
> | parameter | data type               | description                                       |
> |-----------|-------------------------|---------------------------------------------------|
> | 0         | String                  | The uuid of the model to gget |
##### Returns
> | data type                  | description                                                |
> |----------------------------|------------------------------------------------------------|
> | async Result&lt;Model&gt; | The answer from the executed service |
[/ui-accordion-item]

[ui-accordion-item title=<code>server::db::exec_sql(String)\040->\040async\040Result&lt;SqlQueryAnswer&gt;</code>]
##### Description
Executes a SqlQuery against the database.
##### Parameters
> | parameter | data type               | description                                       |
> |-----------|-------------------------|---------------------------------------------------|
> | 0         | String                  | The sql string to be executed |
##### Returns
> | data type                  | description                                                |
> |----------------------------|------------------------------------------------------------|
> | async Result&lt;SqlQueryAnswer&gt; | The answer from the executed sql |
[/ui-accordion-item]

[/ui-accordion]