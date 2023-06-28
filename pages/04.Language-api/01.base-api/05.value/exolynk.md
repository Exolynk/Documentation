---
title: 'Value'
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
> | Value::Reference(Reference) | Stores a reference value |

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

[ui-accordion-item title=<code>Value::get_string(Value)\040->\040Option&lt;String&gt;</code>]

##### Description
Returns an Option which includes a String, when the Value was of type String.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Value            | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;String&gt;    | A option which contains the string when the Value contianed a string |

[/ui-accordion-item]

[ui-accordion-item title=<code>Value::get_list(Value)\040->\040Option&lt;List&gt;</code>]

##### Description
Returns an Option which includes a List, when the Value was of type List.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Value            | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;List&gt;    | A option which contains the List when the Value contianed a List |

[/ui-accordion-item]

[ui-accordion-item title=<code>Value::get_reference(Value)\040->\040Option&lt;Reference&gt;</code>]

##### Description
Returns an Option which includes a Reference, when the Value was of type Reference.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Value            | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Reference&gt;    | A option which contains the Reference when the Value contianed a Reference |

[/ui-accordion-item]

[ui-accordion-item title=<code>Value::get_language(Value)\040->\040Option&lt;Language&gt;</code>]

##### Description
Returns an Option which includes a Language, when the Value was of type Language.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Value            | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Language&gt;    | A option which contains the Language when the Value contianed a Language |

[/ui-accordion-item]

[ui-accordion-item title=<code>Value::get_float(Value)\040->\040Option&lt;f64&gt;</code>]

##### Description
Returns an Option which includes a f64, when the Value was of type Float.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Value            | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;f64&gt;    | A option which contains the f64 when the Value contianed a Float |

[/ui-accordion-item]

[ui-accordion-item title=<code>Value::get_integer(Value)\040->\040Option&lt;i64&gt;</code>]

##### Description
Returns an Option which includes a i64, when the Value was of type Integer.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Value            | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;i64&gt;    | A option which contains the i64 when the Value contianed a Integer |

[/ui-accordion-item]

[ui-accordion-item title=<code>Value::get_bool(Value)\040->\040Option&lt;bool&gt;</code>]

##### Description
Returns an Option which includes a bool, when the Value was of type Bool.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Value            | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;bool&gt;    | A option which contains the bool when the Value contianed a Bool |

[/ui-accordion-item]

[ui-accordion-item title=<code>Value::get_ident(Value)\040->\040Option&lt;Ident&gt;</code>]

##### Description
Returns an Option which includes a Ident, when the Value was of type Ident.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Value            | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Ident&gt;    | A option which contains the Ident when the Value contianed a Ident |

[/ui-accordion-item]

[ui-accordion-item title=<code>Value::get_selection(Value)\040->\040Option&lt;Selection&gt;</code>]

##### Description
Returns an Option which includes a Selection, when the Value was of type Selection.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Value            | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Selection&gt;    | A option which contains the Selection when the Value contianed a Selection |

[/ui-accordion-item]

[ui-accordion-item title=<code>Value::get_version(Value)\040->\040Option&lt;Version&gt;</code>]

##### Description
Returns an Option which includes a Version, when the Value was of type Version.
##### Parameters
> | parameter | data type               | description                                                           |
> |-----------|-------------------------|-----------------------------------------------------------------------|
> | 0         | Self / Value            | A reference to the own object |
##### Returns
> | data type               | description                                                           |
> |-------------------------|-----------------------------------------------------------------------|
> | Option&lt;Version&gt;    | A option which contains the Version when the Value contianed a Version |

[/ui-accordion-item]
[/ui-accordion]