---
title: 'Workflow / Webapp Specific API'
taxonomy:
    category: docs
process:
    markdown: true
    twig: true
---

## Workflow / Webapp Specific API
The following webapp APIs are only availble in workflows and executed within a users browser.

------------------------------------------------------------------------------------------
### test 2
### hooks
Workflows with an ident with one in the following list will be automatically triggered by events. 
<details>
 <summary><code>new_record</code></summary>

##### Description
This workflow is triggered whenever the user creates a new record for a model. When this workflow does not exist or is not active, the system uses the default creation logic. The new record can be received in the normal way with `webapp::get_record() -> Record`. When this workflow is executed the model workflow is responisble to create the record within the database. Otherwise it will get lost.
##### Example
> ```rust
> /// This function should not be shown in the actionbar
> pub fn show() {
>     false
> }
> 
> /// Normal main function
> pub async fn main() {
> 	 	// get the new record over api
> 		let record = webapp::get_record()
> 		// debug print it
> 		dbg(record);
> 		// TODO: Create this record in an own service within the database
> }
> ```

</details>






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