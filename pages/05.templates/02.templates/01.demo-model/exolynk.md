---
title: 'Demo Model and Workflow'
taxonomy:
    category:
        - docs
markdown.extra: true
process:
    markdown: true
    twig: false
downloads:
    enabled: true
    include_all_files: true
markdown:
    extra: true
---

[TOC]


<p class="ui5-icon" style="font-size: 4em;" name="wrench">&#xe16d</p>

<br><br><br><br>

## Demo Model and Workflow

[downloads route="/downloads/model-templates/demo-model" layout="list-files" width="300" /]

<br>


[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Description"]

This is a simple predefined demo model which includes all available variables and attributes.

[/ui-tab]

[ui-tab title="Predefined Variables"]
> | Variable ident     | data type         | Description
> |--------------------|-------------------|---------------------------------------------------------------------------------|
> | string_demo        | String            | String (Text, Number and Symbols  )                                             |
> | bool_demo          | Bool              | Bool (True or False)                                                            |
> | float_demo         | Float             | double-precision floating-point numbers                                         |
> | integer_demo       | Integer           | simple Number                                                                   |
> | list_demo          | List              | List Element                                                                    |
> | reference_demo     | Reference         | Reference to other records                                                      |
> | selection_demo     | Selection         | Selection (Drop-Down)                                                           |
> | datetime_demo      | DateTime          | Date and Time                                                                   |
> | ident_demo         | Ident             | Unique Identifier                                                               |
> | language_demo      | Language          | Languege Field                                                                  |
> | version_demo       | Version           | Version                                                                         |
> | multiline_demo     | Multiline String  | String with more than one line                                                  |
> | table_demo         | Table             | Table element with columns and rows                                             |
> | color_demo         | Color             | HTML Color Codes representing a color                                           |
> | location_demo      | Location          | Location Element wit Map, Street, No, City, Country, Latitude and Longitude     |
> | signature_demo     | Signature         | Signature Element to handsign a document or form with a legally valid signature |

[/ui-tab]

[ui-tab title="Dashboard Layout"]
```html
<home>
    <!-- Line Break -->
    <new-line />    
    <!-- <highlight-button title="Hinzufügen" text="Record hinzufügen" icon="add" link="#/search/add" /> -->
    <highlight-button title="All User" text="List of all User" icon="person-placeholder" link="#/search?lang=en&query=&offset=0&model=user" />
    <highlight-button title="Rights" text="Alle Rechte" icon="key" link="#/search?lang=en&query=&model=right&status=&view=List&print=false&tab=" />
    <highlight-button title="Role" text="Alle Rollen" icon="role" link="#/search?lang=en&query=&model=role&status=&view=List&print=false&tab=" />
    <highlight-button title="Dateien" text="Alle Anhänge" icon="attachment-photo" link="#/search?lang=en&query=&offset=0&model=file" />
    <highlight-button title="Hinzufügen" text="Record hinzufügen" icon="add" link="#/search?lang=en&query=&offset=0&model=maintenance_request&add=maintenance_request" />
    <!-- Line Break -->
    <new-line />    
    <highlight-button title="All Records" text="All Demo Records" icon="example" link="#/search?lang=en&query=&offset=0&model=model_demo" />
    <highlight-button title="Status new" text="Model Demo" icon="example" link="#/search?lang=en&query=&model=model_demo&status=new" />
    <highlight-button title="Status pending" text="Model Demo" icon="example" link="#/search?lang=en&query=&model=model_demo&status=pending" />
    <highlight-button title="Status done" text="Model Demo" icon="example" link="#/search?lang=en&query=&model=model_demo&status=done" />
    <highlight-button title="Exolynk Website" text="External URL" icon="chain-link" link="https://exolynk.com" />
</home>
```
[/ui-tab]

[ui-tab title="Screenshots"]

**Usage**

![Usage](demo-model.gif?resize=600&classes=left)

[/ui-tab]

[/ui-tabs]

<footer>
    <link rel="stylesheet" type="text/css" href="https://ui5.sap.com/resources/sap/ui/core/themes/base/SAP-icons.css">
    <style>
      .laptop::before {
        font-family: SAP-icons;
        content: "\e027";
      }
      .accelerated::before {
        font-family: SAP-icons;
        content: "\e0e0";
      }
      @font-face {
      font-family: "ui5-icon-font";
      src: url(https://docs.exolynk.com/cdn/SAP-icons.ttf) format("truetype");
      }
      p.ui5-icon { 
      font-family: "ui5-icon-font";
    }
    </style>
</footer>