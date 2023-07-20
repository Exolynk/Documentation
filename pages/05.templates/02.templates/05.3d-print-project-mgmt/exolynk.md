---
title: '3D Print Projects'
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


<p class="ui5-icon" style="font-size: 4em;" name="machine">&#xe109;</p>

<br><br><br><br>

## 3D Print Project Management Tool

[downloads route="/downloads/model-templates/3d-print-project-mgmt" layout="list-files" width="300" /]

<br>


[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Description"]

A project management tool to for a 3D Print Factory who produces prototypes for industrial use. Track Projects with client data, project informations, plans, *.STL Files, etc. Filament library to reference in projects and maintain the filament and material stock.

Please find more about the usage of this Template in this <a href="https://www.linkedin.com/feed/update/urn:li:activity:7060585973184638976" target="_blank">LinkedIn Article</a>.

**Supported features:**
- Project Information
    - Staus: Draft, In Construction, In Production, In Delivery, Closed
    - Project Name, Description, Delivery Date, Price, Files, Client Information,..
- Filament Library
    - Fillament Type, Images, Supplier, Price, Color, Type
- Project Status chart
- Record log for all user interactions
- User access management with roles and rights (can be configured per variable and layout)

![Thingseneer](exolynk-zoomed_Thinineer.png?resize=600&classes=left)


[/ui-tab]

[ui-tab title="Predefined Model Variables"]

Model Project
> | Variable ident             | data type                       | Description
> |----------------------------|---------------------------------|-----------------------------------------------------------------------|
> | filamenttype               | List                            | List of Filament Types used for Project
> | weight                     | String                          | Weight of the prototype
> | deliverydate               | Date/time                       | Delivery Date
> | files                      | File                            | File Attachements like PDF Plans, STL files etc.
> | client_name                | String                          | Client Name
> | client_address             | String                          | Client Address
> | material                   | Selection                       | Options:  ABS, PA, PC, PLA, PETG (PET, PETT), TPE, TPU, TPC (Flexible)
> | client_email               | String                          | Client Email
> | client_phone               | String                          | Client Phone
> | price_agreed               | String                          | Agreed Price for Prototype
> | material_color             | String                          | Color of the Material (Filament)
> | filament_prod              | Reference -> Filter: Filament   | Filament Type Reference
> | amount                     | Integer                         | Amount of Prototypes
> | einkaufspreis              | String                          | Purchasing price

Model Filament
> | Variable ident             | data type                       | Description
> |----------------------------|---------------------------------|-----------------------------------------------------------------------|
> | filament_material          | Selection                       | Options: ABS, PA, PC, PLA, PETG (PET, PETT), TPE, TPU, TPC (Flexible)
> | filament_color             | Selection                       | Options: black, blue, red, green, white, transparent
> | filament_img               | List Reference -> Filter File   | List with Images
> | filament_supplier_url      | String                          | Product URL of suppliert
> | on_stock                   | Integer                         | Amount on stock
[/ui-tab]

[ui-tab title="Dashboard Layout"]
```html
<home>
    <highlight-button title="All User" text="List of all User" icon="person-placeholder" link="#/search?lang=en&query=&offset=0&model=user" />
    <highlight-button title="Rights" text="Alle Rechte" icon="key" link="#/search?lang=en&query=&model=right&status=&view=List&print=false&tab=" />
    <highlight-button title="Role" text="Alle Rollen" icon="role" link="#/search?lang=en&query=&model=role&status=&view=List&print=false&tab=" />
    <highlight-button title="Dateien" text="Alle Anhänge" icon="attachment-photo" link="#/search?lang=en&query=&offset=0&model=file" />
    <highlight-button title="Hinzufügen" text="Record hinzufügen" icon="add" link="#/search?lang=en&query=&offset=0&model=maintenance_request&add=maintenance_request" />
    <!-- Line Break -->
    <new-line />
    <highlight-button title="Neues Projekt" text="Projekt hinzufügen" icon="add" link="#/search?lang=en&query=&model=project&status=&view=List&add=project&print=false&tab=" />
    <highlight-button title="Projekt Übersicht" text="Alle Projekte" icon="factory" link="#/search?lang=en&query=&model=project&status=&view=Table&print=false&tab=&cols=name+client_name+status+" />
    <highlight-button title="Kalender" text="Kalender Ansicht" icon="accelerated" link="#/search?lang=en&query=&model=project&status=&view=Calendar&print=false&tab=" />
    <highlight-button title="In Produktion" text="Projekte in Produktion" icon="busy" link="#/search?lang=en&query=&offset=0&model=project&status=in-production" />
    <highlight-button title="Filamente" text="Alle Filamente" icon="goalseek" link="#/search?lang=en&query=&offset=0&model=filament" />
    <highlight-button title="thingineer.ch" text="Thingineer Website" icon="chain-link" link="https://thingineer.ch/" />
    
    <!-- Line Break -->
    <new-line />   
    <!-- Pipline Chart -->
    <chart typ="bar" name="Projects by status">
        <chart-data model="project" action="count" variable="status" group_by="ident" name="Draft">
            <data-filter variable="status" operator="equal" value="draft" />
        </chart-data>
        <chart-data model="project" action="count" variable="status" group_by="ident" name="1/4 in Construction">
            <data-filter variable="status" operator="equal" value="in_construction" />
        </chart-data>
        <chart-data model="project" action="count" variable="status" group_by="ident" name="2/4 in Production">
            <data-filter variable="status" operator="equal" value="in_production" />
        </chart-data>
        <chart-data model="project" action="count" variable="status" group_by="ident" name="3/4 in Delivery">
            <data-filter variable="status" operator="equal" value="in_delivery" />
        </chart-data>
        <chart-data model="project" action="count" variable="status" group_by="ident" name="4/4 Closed">
            <data-filter variable="status" operator="equal" value="closed" />
        </chart-data>
    </chart>
</home>
```
[/ui-tab]

[ui-tab title="Screenshots"]

**Dashboard**

![Screenshot](dashboard-3d.png?resize=800&classes=left)

**Project Overview**

![Screenshot](Project-View-3d.png?resize=800&classes=left)

**Calendar View**

![Screenshot](Calendar-View-3d.png?resize=800&classes=left)

**Project Information**

![Screenshot](Project-Information-3d.gif?resize=800&classes=left)

**Filament Reference**

![Screenshot](Filament-Reference-3d.png?resize=800&classes=left)

**Filament Information**

![Screenshot](Filament-Information-3d.gif?resize=800&classes=left)

**File Information**

![Screenshot](Files-3d.png?resize=800&classes=left)

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