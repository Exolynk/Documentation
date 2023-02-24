---
title: 'Base API'
taxonomy:
    category:
        - docs
process:
    markdown: true
    twig: false
---

[TOC]

<br><br><br><br>

## Base API
------------------------------------------------------------------------------------------

### Environment
The environment is the system root and holds all models, records, configurations etc.
Global settings, translations are stored within this object.



[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Getter</code>]

##### Parameters
> | name      | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `uuid`    | String                  | The unique uuid for the environment  |
> | `ident`   | Ident                   | The unique textual identifier for the environment  |
> | `name`    | Language                | The display name of the environment |
> | `status`  | String                  | The status of the environment  |
> | `languages`     | Selection         | The supported languages of the environment  |
> | `translations`  | Selection         | The translations of the environment  |
> | `settings`      | Settings          | The detail settings of the environment  |

[/ui-accordion-item]

[ui-accordion-item title=<code>Setter</code>]

##### Parameters
> | name           | data type          | description                                                  |
> |----------------|--------------------|--------------------------------------------------------------|
> | `name`         | Language           | Set the display name of the environment |
> | `languages`    | Selection          | Set the supported languages for this environment  |
> | `translations` | Selection          | Set the translations for this environment  |
> | `settings`     | Settings           | Set the detail settin<code><code>Getter</code></code>gs of the environment  |

[/ui-accordion-item]
[/ui-accordion]



------------------------------------------------------------------------------------------
### Model
A model represents a record type or a database table within the system. The model defines, which
custom variables a record has and stores the workflows and services for these specific record types.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Getter</code>]

##### Parameters
> | name      | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `uuid`    | String                  | The unique uuid of the model  |
> | `ident`   | Ident                   | The unique textual identifier for the model  |
> | `version` | Version                 | The actual version of the model  |
> | `status`  | String                  | The status of the model  |
> | `icon`    | String                  | The icon of the model for the previews  |
> | `layout`  | String                  | The layout in html to define how the records should be visuualized  |
> | `system`  | Bool                    | Implies if this model is defined by the system or customer specific  |
> | `name`    | Language                | The display name of the model |
> | `description`   | Language          | The display description of the model |
> | `record_status` | Selection         | Defines the different status options the record should have  |
> | `variables`     | &lt;Variable&gt;  | The list of variables of this model  |

[/ui-accordion-item]

[ui-accordion-item title=<code>Setter</code>]

##### Parameters
> | name      | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `icon`    | String                  | The icon of the model  |
> | `layout`  | String                  | The html layout of the model for its records  |
> | `name`    | Language                | Set the display name of the model |
> | `description`   | Language          | Set the display descritption of the model |
> | `record_status` | Selection         | Defines the different status options the record should have  |
> | `variables`     | &lt;Variable&gt;  | Set the list of variables of this model  |

[/ui-accordion-item]
[/ui-accordion]



------------------------------------------------------------------------------------------
### Record
A record is a single dataset inside the system. It is stored as row within the internal database inside
a table which is uunique for this record type / model.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Getter</code>]

##### Parameters
> | name      | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `uuid`    | String                  | The unique uuid of the record  |
> | `ident`   | Ident                   | The unique textual identifier for the record  |
> | `version` | Version                 | The version for the record  |
> | `model`   | String                  | The uuid of the model as String  |
> | `status`  | String                  | The status of the record  |
> | `released`| Bool                    | Implies if this model is released and not changeable anymore |
> | `name`    | Language                | The display name of the record |
> | `description`   | Language          | The display description of the record |

[/ui-accordion-item]

[ui-accordion-item title=<code>Setter</code>]

##### Parameters
> | name      | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `uuid`    | String                  | Set the uuid. This fails if the uuid has a wrong format  |
> | `ident`   | Ident                   | Set the ident for the record, converts automatically to a valid form  |
> | `status`  | String                  | Set the status for the record  |
> | `released`| Bool                    | Is the record released and not changeable anymore  |
> | `name`    | Language                | Set the display name of the record |
> | `description`   | Language          | Set the display descritption of the record |

[/ui-accordion-item]

[ui-accordion-item title=<code>Record::set_value(Record,\040Ident,\040Value)</code>]

##### Description
Sets the value inside of a record. Providing the Ident "name", "description", "status", sets the standard record values. All other Idents will set a custom value.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Record           | A reference to the own object |
> | 1         | Ident                   | Define which value should be set |
> | 2         | Value                   | The value which should be set |

[/ui-accordion-item]

[ui-accordion-item title=<code>Record::get_value(Record,\040Ident)\040->\040Option&lt;Value&gt;</code>]

##### Description
Returns a Value for the given ident when found.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Record           | A reference to the own object |
> | 2         | Ident                   | The Ident we want to have the value for |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Value&gt;  | The value when found |

[/ui-accordion-item]

[ui-accordion-item title=<code>Record::get_variable(Record,\040Model,\040Ident)\040->\040Option&lt;Variable&gt;</code>]

##### Description
Returns a Variable for the given ident when found. The model is needed to abstract the right values.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Record           | A reference to the own object |
> | 1         | Model                   | A reference to the model this record belongs to |
> | 2         | Ident                   | The Ident we want to have the variable for |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Variable&gt;  | The variable when found |

[/ui-accordion-item]
[/ui-accordion]




------------------------------------------------------------------------------------------
### Variable
A variable defines how a value should be handled, which type it has, etc. It's used mostly in the model
to define how customer specific fields look like.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Getter</code>]

##### Parameters
> | name      | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `ident`   | String                  | The unique textual identifier for the variable  |
> | `system`  | Bool                    | Implies if this variable is defined by the system or customer specific  |
> | `released`| Bool                    | Shows if the variable has been released and deployed to the db schema  |
> | `required`| Bool                    | Shows if the variable is required to the user in edit mode |
> | `access`  | Access                  | Shows with which access rights the variable is shown to the user |
> | `value`   | Value                   | The value type of the variable and default value when created |
> | `name`    | Language                | The display name of the variable |
> | `description`   | Language          | The display description of the variable |

[/ui-accordion-item]

[ui-accordion-item title=<code>Setter</code>]

##### Parameters
> | name      | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `ident`   | String                  | The unique textual identifier for the variable  |
> | `required`| Bool                    | Shows if the variable is required to the user in edit mode |
> | `access`  | Access                  | Shows with which access rights the variable is shown to the user |
> | `value`   | Value                   | The value type of the variable and default value when created |
> | `name`    | Language                | The display name of the variable |
> | `description`   | Language          | The display description of the variable |

[/ui-accordion-item]
[/ui-accordion]




------------------------------------------------------------------------------------------
### Value
A value is an enum with a unit variant for each different value it can store. This strictly typed
Value is used within the record and variable to store values.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Variants</code>]

##### Variants
> | data type                   | description                                                           |
> |-----------------------------|-----------------------------------------------------------------------|
> | Value::Language(Language)   | Stores a Language value |
> | Value::String(String)       | Stores a String value |
> | Value::Float(f64)           | Stores a f64 floating value |
> | Value::Integer(i64)         | Stores a i64 number value |
> | Value::Bool(Bool)           | Stores a boolean value |
> | Value::Ident(Ident)         | Stores a Ident value |
> | Value::Selection(Selection) | Stores a Selection value |
> | Value::Version(Version)     | Stores a version value |
> | Value::List(List)           | Stores a list value |

##### Example
> ```rust
> // Create a Value with String typ
> let val_s = Value::String("Hello World");
> 
> // Check for the string
> match val_s {
> 	Value::String(s) => println!("String: {}", s),
> 	_ => println!("No String value")
> }
> ```

[/ui-accordion-item]

[ui-accordion-item title=<code>Value::as_string(Value)\040->\040String</code>]

##### Description
Returns a String whith the ident value type.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Value            | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | String                  | A String object with the type e.g. language/float/bool/.... |

[/ui-accordion-item]
[/ui-accordion]





------------------------------------------------------------------------------------------
### Language
A language is an object with holds text translated in multiple languages.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Language::new()\040->\040Language</code>]

##### Description
Returns a empty Language object.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Language                | A Language object |

[/ui-accordion-item]

[ui-accordion-item title=<code>Language::new_en(String)\040>\040Language</code>]

##### Description
Returns a Language object with the english languauge set.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String                  | The text in the english language to initalize the Langauge object with |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Language                | A Language object |

[/ui-accordion-item]

[ui-accordion-item title=<code>Language::get(Self,\040String)\040->\040Option&lt;String&gt;</code>]

##### Description
Returns the text in the defined language if found.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Language         | A reference to the own object |
> | 1         | String                  | The language ident (en, de, fr, it, ...) |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&gt;Self&gt;      | Returns the text in the defined language if found |

[/ui-accordion-item]

[ui-accordion-item title=<code>Language::set(Self,\040String,\040String)</code>]

##### Description
Sets the language text for the given language ident.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Language         | A reference to the own object |
> | 1         | String                  | The language ident (en, de, fr, it, ...) |
> | 2         | String                  | The language text |

[/ui-accordion-item]
[/ui-accordion]



------------------------------------------------------------------------------------------
### Ident
An Identifier is like a String but only allows small letters, underscore and numbers. The first character
needs to be a small letter. When creating an ident from a String, it automatically transforms the String
to a fitting ident.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Ident::new(String)\040->\040Ident</code>]

##### Description
Returns a new Ident.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String                  | A ident as String formated |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Ident                   | A Ident object |

[/ui-accordion-item]

[ui-accordion-item title=<code>Ident::as_string(Ident)\040->\040String</code>]

##### Description
Returns a String whith the ident value.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Ident.           | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | String.                 | A String object |

[/ui-accordion-item]
[/ui-accordion]



------------------------------------------------------------------------------------------
### Selection
A selection is mostly used as dropdown fields to select one or multiple options.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Selection::new()\040->\040Selection</code>]

##### Description
Returns a empty Selection object.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Selection               | A Selection object |

[/ui-accordion-item]

[ui-accordion-item title=<code>Selection::new_languages()\040->\040Selection</code>]

##### Description
Returns a Selection object, where the defaul languages (en, de, it, fr) are set with the translations.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Selection               | A Selection object |

[/ui-accordion-item]

[ui-accordion-item title=<code>Selection::get(Self,\040String)\040->\040Option&lt;Language&gt;</code>]

##### Description
Returns the Language object for the defined option, when found
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Selection        | A reference to the own object |
> | 1         | String                  | The option ident |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&gt;Language&gt;  | Returns the language if found |

[/ui-accordion-item]

[ui-accordion-item title=<code>Selection::insert(Self,\040String,\040Language)</code>]

##### Description
Inserts a new option to the selection with the given ident and Language.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Selection        | A reference to the own object |
> | 1         | String                  | The option ident  |
> | 2         | Language                | The language text |

[/ui-accordion-item]

[ui-accordion-item title=<code>Selection::get_mode(Self)\040->\040SelectionMode</code>]

##### Description
Returns the SelectionMode enum for this selection
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Selection        | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | SelectionMode           | Returns the selection mode |

[/ui-accordion-item]

[ui-accordion-item title=<code>Selection::set_mode(Self,\040SelectionMode)</code>]

##### Description
Defines with selection mode (Single, Multi, Show) the selection should use.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Selection        | A reference to the own object |
> | 1         | SelectionMode           | Set the mode |

[/ui-accordion-item]

[ui-accordion-item title=<code>Selection::get_selected(Self)\040->\040Vec&lt;String&gt;</code>]

##### Description
Returns the idents of the selected options
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Selection        | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Vec&gt;Language&gt;     | Returns a list with the selected idents |

[/ui-accordion-item]

[ui-accordion-item title=<code>Selection::set_selected(Self,\040Vec&lt;String&gt;)</code>]

##### Description
Sets the selected options of the given selection
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Selection        | A reference to the own object |
> | 1         | Vec&lt;String&gt;       | The selected option idents in a list  |

[/ui-accordion-item]
[/ui-accordion]



------------------------------------------------------------------------------------------
### List
A can store multiple values at once. A list can be restricted to a specific value typ.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>List::new()\040->\040List</code>]

##### Description
Returns a empty List with no typ restriction.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | List.                   | A List object |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::new_restriction(Value)\040->\040List</code>]

##### Description
Returns a List with the given restriction typ in place.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 1         | Value                   | A Value to define the restriction type and default value |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | List                    | A List object |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::set_restriction(Self,\040Option&lt;Value&gt;)</code>]

##### Description
Sets or removes the restriction of the list.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / List.            | A reference to the own object |
> | 1         | Option&lt;Value&gt;     | The restriction to set or None for no restriction |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::get_restiction(Self)\040->\040Option&lt;Value&gt;</code>]

##### Description
Gets the actual restriction of the list.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / List             | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Value&gt;     | A Value which is the actual restriction |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::add(Self,\040Value)</code>]

##### Description
Adds a new value to the list collection.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Selection        | A reference to the own object |
> | 1         | Value                   | The value which should be added to the list |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::get(Self,\040usize)\040->\040Option&lt;Value&gt;</code>]

##### Description
Gets an entry from the list
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / List             | A reference to the own object |
> | 1         | usize                   | The position in the list we want the entry of |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Value&gt;     | A Value which is the actual restriction |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::replace(Self,\040usize,\040Value)</code>]

##### Description
Replaces an entry at the defined position.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / List             | A reference to the own object |
> | 1         | usize                   | The index of the entry inside the list to replace |
> | 2         | Value                   | The new value to replace the old one with |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::remove(Self,\040usize)</code>]

##### Description
Remove an entry at the given positon.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / List             | A reference to the own object |
> | 1         | usize                   | Position where the entry should be removed  |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::clear(Self)</code>]

##### Description
Clears the complete list.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / List             | A reference to the own object |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::len(Self)\040->\040usize</code>]

##### Description
Returns the length of the list
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / List             | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | usize                   | Length of the list |

[/ui-accordion-item]

[ui-accordion-item title=<code>List::is_empty(Self)\040->\040bool</code>]

##### Description
Returns if the list is empty or has entries inside.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / List             | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | bool                    | True when empty false when it has entries |

[/ui-accordion-item]
[/ui-accordion]



------------------------------------------------------------------------------------------
### Reference
A reference is a Uuid v4 which points towards another record. In special cases this can also point to
a model or an environment. In this cases, this will not displayed correctly within the UI.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Reference::new()\040->\040Reference</code>]

##### Description
Returns a new Reference with a uuid of nil/all zeros.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Reference               | A Reference object |

[/ui-accordion-item]

[ui-accordion-item title=<code>Reference::as_string(Version)\040->\040String</code>]

##### Description
Returns a String with the uuid.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Reference        | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | String                  | A String object |

[/ui-accordion-item]

[ui-accordion-item title=<code>Reference::from_str(String)\040->\040Result&lt;Reference&gt;</code>]

##### Description
Tries to create a new Reference from a string.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String                  | A uuid string |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Result&lt;Reference&gt; | The reference or an error |

[/ui-accordion-item]
[/ui-accordion]





------------------------------------------------------------------------------------------
### Version
A version object. Right now it only allows nubered version (e.g. 0, 1, 2, 3, ...) in future
more version formats are planned.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Version::new(String)\040->\040Version</code>]

##### Description
Returns a new Version.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String                  | A numer as String formated |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Version                 | A Version object |

[/ui-accordion-item]

[ui-accordion-item title=<code>Version::as_string(Version)\040->\040String</code>]

##### Description
Returns a String with the version.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Version          | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | String.                 | A String object |

[/ui-accordion-item]
[/ui-accordion]






------------------------------------------------------------------------------------------
### Access
Access is a enum to control how variables can be seen and changed within the UI and on the server side

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Variants</code>]

##### Variants
> | data type                   | description                                                           |
> |-----------------------------|-----------------------------------------------------------------------|
> | Access::Write               | Allows the user to write/change the value of an input |
> | Access::Change              | Allows the user to change the field e.g. insert new options |
> | Access::Read                | Allows the user to just read the value |
> | Access::Hide                | Hide the value from the user. Be aware this is only for the ui rendering! |

[/ui-accordion-item]

[ui-accordion-item title=<code>Access::from_str(String)\040->\040Access</code>]

##### Description
Creates the access enum from a string. When a wrong string is given, it returns Access::Hide as default.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | String                  | The access name as String |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Access                  | The access struct generated from the string |

[/ui-accordion-item]

[ui-accordion-item title=<code>Access::as_string(Access)\040->\040String</code>]

##### Description
Returns a String whith the access value.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Access           | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | String                  | A String with the access |

[/ui-accordion-item]
[/ui-accordion]





------------------------------------------------------------------------------------------
### Settings
A map of keys and values wich stores detail settings for the system.

[ui-accordion independent=true open=none]
[ui-accordion-item title=<code>Settings::new()\040->\040Settings</code>]

##### Description
Returns a empty Settings object.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Settings                | A Settings object |

[/ui-accordion-item]

[ui-accordion-item title=<code>Settings::get(Self,String)\040->\040Option&lt;String&gt;</code>]

##### Description
Returns the specific setting if found.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Settings         | A reference to the own object |
> | 1         | String                  | The setting ident |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&gt;String&gt;    | Returns the settings as string |

[/ui-accordion-item]

[ui-accordion-item title=<code>Settings::insert(Self,\040String,\040String)</code>]

##### Description
Inserts a new setting in the settings object. An existing setting with the same ident will be overwritten.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Settings         | A reference to the own object |
> | 1         | String                  | The settings ident |
> | 2         | String                  | The detail setting |

[/ui-accordion-item]

[ui-accordion-item title=<code>Settings::remove(Self,\040String)</code>]

##### Description
Removes a specific setting from the object.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Settings         | A reference to the own object |
> | 1         | String                  | The setting ident to be removed |

[/ui-accordion-item]
[/ui-accordion]
