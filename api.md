## Base API
------------------------------------------------------------------------------------------
### Environment
The environment is the system root and holds all models, records, configurations etc.
Global settings, translations are stored within this object.
<details>
 <summary><code>Getter</code></summary>

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

</details>

<details>
 <summary><code>Setter</code></summary>

##### Parameters
> | name           | data type          | description                                                  |
> |----------------|--------------------|--------------------------------------------------------------|
> | `name`         | Language           | Set the display name of the environment |
> | `languages`    | Selection          | Set the supported languages for this environment  |
> | `translations` | Selection          | Set the translations for this environment  |
> | `settings`     | Settings           | Set the detail settings of the environment  |

</details>




------------------------------------------------------------------------------------------
### Model
A model represents a record type or a database table within the system. The model defines, which
custom variables a record has and stores the workflows and services for these specific record types.
<details>
 <summary><code>Getter</code></summary>

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

</details>

<details>
 <summary><code>Setter</code></summary>

##### Parameters
> | name      | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `icon`    | String                  | The icon of the model  |
> | `layout`  | String                  | The html layout of the model for its records  |
> | `name`    | Language                | Set the display name of the model |
> | `description`   | Language          | Set the display descritption of the model |
> | `record_status` | Selection         | Defines the different status options the record should have  |
> | `variables`     | &lt;Variable&gt;  | Set the list of variables of this model  |

</details>




------------------------------------------------------------------------------------------
### Record
A record is a single dataset inside the system. It is stored as row within the internal database inside
a table which is uunique for this record type / model.
<details>
 <summary><code>Getter</code></summary>

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

</details>

<details>
 <summary><code>Setter</code></summary>

##### Parameters
> | name      | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `uuid`    | String                  | Set the uuid. This fails if the uuid has a wrong format  |
> | `ident`   | Ident                   | Set the ident for the record, converts automatically to a valid form  |
> | `status`  | String                  | Set the status for the record  |
> | `released`| Bool                    | Is the record released and not changeable anymore  |
> | `name`    | Language                | Set the display name of the record |
> | `description`   | Language          | Set the display descritption of the record |

</details>

<details>
 <summary><code>Record::set_value(Record, Ident, Value)</code></summary>

##### Description
Sets the value inside of a record. Providing the Ident "name", "description", "status", sets the standard record values. All other Idents will set a custom value.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Record           | A reference to the own object |
> | 1         | Ident                   | Define which value should be set |
> | 2         | Value                   | The value which should be set |

</details>

<details>
 <summary><code>Record::get_variable(Record, Model, Ident) -> Option&lt;Variable&gt;</code></summary>

##### Description
Returns a Variable for the given ident when found. The model is needed to abstract the right values.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Record           | A reference to the own object |
> | 1         | Model                   | A reference to the model this record belongs to |
> | 2         | Ident                   | The Ident we want to have teh variable for |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Variable&gt;  | The variable when found |

</details>





------------------------------------------------------------------------------------------
### Variable
A variable defines how a value should be handled, which type it has, etc. It's used mostly in the model
to define how customer specific fields look like.
<details>
 <summary><code>Getter</code></summary>

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

</details>

<details>
 <summary><code>Setter</code></summary>

##### Parameters
> | name      | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | `ident`   | String                  | The unique textual identifier for the variable  |
> | `required`| Bool                    | Shows if the variable is required to the user in edit mode |
> | `access`  | Access                  | Shows with which access rights the variable is shown to the user |
> | `value`   | Value                   | The value type of the variable and default value when created |
> | `name`    | Language                | The display name of the variable |
> | `description`   | Language          | The display description of the variable |

</details>





------------------------------------------------------------------------------------------
### Value
A value is an enum with a unit variant for each different value it can store. This strictly typed
Value is used within the record and variable to store values.
<details>
 <summary><code>Variants</code></summary>

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

</details>

<details>
 <summary><code>Value::as_string(Value) -> String</code></summary>

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

</details>






------------------------------------------------------------------------------------------
### Language
A language is an object with holds text translated in multiple languages.
<details>
 <summary><code>Language::new() -> Language</code></summary>

##### Description
Returns a empty Language object.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Language                | A Language object |

</details>

<details>
 <summary><code>Language::new_en(String) -> Language</code></summary>

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

</details>

<details>
 <summary><code>Language::get(Self, String) -> Option&lt;String&gt;</code></summary>

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

</details>

<details>
 <summary><code>Language::set(Self, String, String)</code></summary>

##### Description
Sets the language text for the given language ident.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Language         | A reference to the own object |
> | 1         | String                  | The language ident (en, de, fr, it, ...) |
> | 2         | String                  | The language text |

</details>




------------------------------------------------------------------------------------------
### Ident
An Identifier is like a String but only allows small letters, underscore and numbers. The first character
needs to be a small letter. When creating an ident from a String, it automatically transforms the String
to a fitting ident.
<details>
 <summary><code>Ident::new(String) -> Ident</code></summary>

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

</details>

<details>
 <summary><code>Ident::as_string(Ident) -> String</code></summary>

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

</details>




------------------------------------------------------------------------------------------
### Selection
A selection is mostly used as dropdown fields to select one or multiple options.
<details>
 <summary><code>Selection::new() -> Selection</code></summary>

##### Description
Returns a empty Selection object.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Selection               | A Selection object |

</details>

<details>
 <summary><code>Selection::new_languages() -> Selection</code></summary>

##### Description
Returns a Selection object, where the defaul languages (en, de, it, fr) are set with the translations.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Selection               | A Selection object |

</details>

<details>
 <summary><code>Selection::get(Self, String) -> Option&lt;Language&gt;</code></summary>

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

</details>

<details>
 <summary><code>Selection::insert(Self, String, Language)</code></summary>

##### Description
Inserts a new option to the selection with the given ident and Language.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Selection        | A reference to the own object |
> | 1         | String                  | The option ident  |
> | 2         | Language                | The language text |

</details>

<details>
 <summary><code>Selection::get_mode(Self) -> SelectionMode</code></summary>

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

</details>

<details>
 <summary><code>Selection::set_mode(Self, SelectionMode)</code></summary>

##### Description
Defines with selection mode (Single, Multi, Show) the selection should use.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Selection        | A reference to the own object |
> | 1         | SelectionMode           | Set the mode |

</details>

<details>
 <summary><code>Selection::get_selected(Self) -> Vec&lt;String&gt;</code></summary>

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

</details>

<details>
 <summary><code>Selection::set_selected(Self, Vec&lt;String&gt;)</code></summary>

##### Description
Sets the selected options of the given selection
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Selection        | A reference to the own object |
> | 1         | Vec&lt;String&gt;       | The selected option idents in a list  |

</details>




------------------------------------------------------------------------------------------
### Version
A version object. Right now it only allows nubered version (e.g. 0, 1, 2, 3, ...) in future
more version formats are planned.
<details>
 <summary><code>Version::new(String) -> Version </code></summary>

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

</details>

<details>
 <summary><code>Version::as_string(Version) -> String</code></summary>

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

</details>







------------------------------------------------------------------------------------------
### Access
Access is a enum to control how variables can be seen and changed within the UI and on the server side
<details>
 <summary><code>Variants</code></summary>

##### Variants
> | data type                   | description                                                           |
> |-----------------------------|-----------------------------------------------------------------------|
> | Access::Write               | Allows the user to write/change the value of an input |
> | Access::Change              | Allows the user to change the field e.g. insert new options |
> | Access::Read                | Allows the user to just read the value |
> | Access::Hide                | Hide the value from the user. Be aware this is only for the ui rendering! |

</details>

<details>
 <summary><code>Access::from_str(String) -> Access</code></summary>

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

</details>

<details>
 <summary><code>Access::as_string(Access) -> String</code></summary>

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

</details>






------------------------------------------------------------------------------------------
### Settings
A map of keys and values wich stores detail settings for the system.
<details>
 <summary><code>Settings::new() -> Settings</code></summary>

##### Description
Returns a empty Settings object.
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Settings                | A Settings object |

</details>

<details>
 <summary><code>Settings::get(Self, String) -> Option&lt;String&gt;</code></summary>

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

</details>

<details>
 <summary><code>Settings::insert(Self, String, String)</code></summary>

##### Description
Inserts a new setting in the settings object. An existing setting with the same ident will be overwritten.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Settings         | A reference to the own object |
> | 1         | String                  | The settings ident |
> | 2         | String                  | The detail setting |

</details>

<details>
 <summary><code>Settings::remove(Self, String)</code></summary>

##### Description
Removes a specific setting from the object.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Settings         | A reference to the own object |
> | 1         | String                  | The setting ident to be removed |

</details>



<br/>

