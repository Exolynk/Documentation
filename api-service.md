## Service / Server Specific API
The following server APIs are only availble in services and executed on the server.

------------------------------------------------------------------------------------------
### server
Generale functions to interact with the server.

------------------------------------------------------------------------------------------
### server::db
Generale functions to interact with the database of the server.
<details>
 <summary><code>server::db::get_environment() -> async Result&lt;Environment&gt;</code></summary>

##### Description
Returns the actual environment the user is logged into.
##### Returns
> | data type                       | description                                                 |
> |---------------------------------|-------------------------------------------------------------|
> | async Result&lt;Environment&gt; | Returns the actual the environment of the user |

</details>

<details>
 <summary><code>server::db::get_record(String) -> async Result&lt;Record&gt;</code></summary>

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

</details>

<details>
 <summary><code>server::db::insert_record(Record) -> async Result&lt;()&gt;</code></summary>

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

</details>

<details>
 <summary><code>server::db::update_record(Record) -> async Result&lt;()&gt;</code></summary>

##### Description
UUpdates a Record which already exist in the database.
##### Parameters
> | parameter | data type               | description                                       |
> |-----------|-------------------------|---------------------------------------------------|
> | 0         | Record                  | The Record which should be updated |
##### Returns
> | data type                  | description                                                |
> |----------------------------|------------------------------------------------------------|
> | async Result&lt;()&gt; | Thorws an error when something went wrong |

</details>