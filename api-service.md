## Service / Server Specific API
The following server APIs are only availble in services and executed on the server.

------------------------------------------------------------------------------------------
### server
Generale functions to interact with the server.

------------------------------------------------------------------------------------------
### server::db
Generale functions to interact with the database of the server.
<details>
 <summary><code>server::db::get_environment() -> Environment</code></summary>

##### Description
Returns the actual environment the user is logged into.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Environment             | Returns the actual the environment of the user |

</details>