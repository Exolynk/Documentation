## Workflow / Webapp Specific API
The following webapp APIs are only availble in workflows and executed within a users browser.

------------------------------------------------------------------------------------------
### webapp
Generale functions to interact with the browser of the user.
<details>
 <summary><code>webapp::is_edit() -> Bool</code></summary>

##### Description
Returns a boolean to indicate if the user is in edit mode or not.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Bool                    | Returns true when the user is in edit mode, false if he is not |

</details>

<details>
 <summary><code>webapp::set_edit(Bool)</code></summary>

##### Description
Defines the new edit status for the user.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Bool                    | Enable or disable the edit mode |

</details>

<details>
 <summary><code>webapp::get_environment() -> Environment</code></summary>

##### Description
Returns the actual environment the user is logged in.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Environment             | Returns the actual the environment of the user |

</details>

<details>
 <summary><code>webapp::get_model() -> Model</code></summary>

##### Description
Returns the model this workflow is started from.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Model                   | The model this workflow is called from |

</details>

<details>
 <summary><code>webapp::get_record() -> Record</code></summary>

##### Description
Returns the record this workflow is started from.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Record                  | The record this workflow is called from |

</details>

<details>
 <summary><code>webapp::rpc_call() -> async Result&lt;Any&gt;</code></summary>

##### Description
Calls a service for this record on the server. Returns the response from the server, which can be either
a any kind of a value or an error string. This is an async fuunction which need to be awaited.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String                  | The ident/name of the service which should be called |
> | 1         | Any                     | A value which should be send to the service - () for none |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | async Result&lt;Any&gt; | The answer from the executed service |

</details>