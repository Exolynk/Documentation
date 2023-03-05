---
title: 'Workflow / Webapp Specific API'
taxonomy:
    category: docs
process:
    markdown: true
    twig: false
---

[TOC]

## Workflow / Webapp Specific API
The following webapp APIs are only availble in workflows and executed within a users browser.

------------------------------------------------------------------------------------------

### hooks
Workflows with an ident with one in the following list will be automatically triggered by events.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>new_record</code>]

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

[/ui-accordion-item]
[/ui-accordion]



------------------------------------------------------------------------------------------
### webapp
    
[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>webapp::is_edit()\040->\040Bool</code>]

##### Description
Returns a boolean to indicate if the user is in edit mode or not.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Bool                    | Returns true when the user is in edit mode, false if he is not |

[/ui-accordion-item]
[/ui-accordion]

    
[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>webapp::set_edit(Bool)</code>]

##### Description
Defines the new edit status for the user.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Bool                    | Enable or disable the edit mode |

[/ui-accordion-item]
[/ui-accordion]

    
[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>webapp::get_environment()\040->\040Environment</code>]

##### Description
Returns the actual environment the user is logged in.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Environment             | Returns the actual the environment of the user |

[/ui-accordion-item]
[/ui-accordion]

    
[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>webapp::get_model()\040->\040Model</code>]

##### Description
Returns the model this workflow is started from.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Model                   | The model this workflow is called from |

[/ui-accordion-item]
[/ui-accordion]


[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>webapp::get_record()\040->\040Record</code>]

##### Description
Returns the record this workflow is started from.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Record                  | The record this workflow is called from |

[/ui-accordion-item]
[/ui-accordion]

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>webapp::get_user()\040->\040Record</code>]

##### Description
Returns the user record this workflow is started from.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Record                  | The user record this workflow is called from |

[/ui-accordion-item]
[/ui-accordion]

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>webapp::rpc_call()\040->\040async\040Result&lt;Any&gt;</code>]

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

[/ui-accordion-item]
[/ui-accordion]

------------------------------------------------------------------------------------------
### webapp::ui
    
[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>webapp::ui::popup(String,\040String,\040Vec&lt;Variable&gt;)\040->\040async\040Result&lt;(Bool,\040Vec&lt;Variable&gt;)&gt;</code>]

##### Description
Shows a popup to the user with the given Header, text and variables. When the user closes the popup it returns which button has been pressed and the new variables.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String                  | The header text of the popup |
> | 1         | String                  | An additional message for the user inside the poup |
> | 1         | Vec&lt;Variable&gt;     | A list of variables which should be shown to the user |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Bool                    | Returns true the user selected submit, on cancel it returns false |
> | Vec&lt;Variable&gt;     | The variables which have been updated by the users |

[/ui-accordion-item]
[/ui-accordion]