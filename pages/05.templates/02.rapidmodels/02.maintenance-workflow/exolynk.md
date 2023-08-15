---
title: 'Maintenance Workflow'
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


<p class="ui5-icon" style="font-size: 4em;" name="wrench">&#xe002</p>

<br><br><br><br>

## Maintenance Management Workflow

[downloads route="/downloads/model-templates/maintenance-workflow" layout="list-files" width="300" /]

<br>


[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Description"]

In tempor sed sapien eu porttitor. Aliquam cursus facilisis ante. Etiam neque nunc, blandit vel lacus et, faucibus accumsan lacus. Proin posuere varius purus quis faucibus. Quisque et enim vitae orci [placerat tincidunt](#) id ac eros. Fusce et gravida libero. 

Phasellus cursus odio ex, in **mattis lorem tincidunt** vel. Donec nibh odio, dapibus non ligula a, semper ornare massa. Nulla consectetur eu nunc sed ultrices. Integer at turpis dolor.

[/ui-tab]

[ui-tab title="Predefined Variables"]
> | Variable ident     | data type                       | Description
> |--------------------|---------------------------------|-----------------------------------------------------------------------|
> | client_reference   | Reference -> Filter: Client     | Client  |
> | goods_reference    | Reference -> Filter: Goods      | Goods |
> | assigned_user_1    | Reference -> Filter: User       | Responsible service engineer 
> | time_tracking      | Table                           | Time tracking
> | service_report     | Table                           | Service Report
> | client_accept      | Bool                            | Accepted by client
> | service_date       | DateTime format                 | Date and Time

[/ui-tab]

[ui-tab title="Dashboard Layout"]
```html
<home>
    <highlight-button title="Kunden" text="Alle Kunden" icon="customer" link="#/search?lang=en&query=&offset=0&model=client" />
    <highlight-button title="Bestellungen" text="Alle Bestellungen" icon="shipping-status" link="#/search?lang=en&query=&offset=0&model=order" />
    <highlight-button title="Equipment" text="Alle Investitionsgüter" icon="bed" link="#/search?lang=en&query=&offset=0&model=equipment" />
    <highlight-button title="Service Aufträge" text="Alle Service Aufträge" icon="wrench" link="#/search?lang=en&query=&offset=0&model=maintenance_request" />
    <highlight-button title="Neue Aufträge" text="Neue Service Aufträge" icon="add-equipment" link="#/search?lang=en&query=&offset=0&model=maintenance_request&status=new" />
    <highlight-button title="Hakuna" text="Hakuna Zeiterfassung" icon="chain-link" link="https://app.hakuna.ch/login" target="_blank" />
    
    <!-- Line Break -->
    <new-line />    
    <highlight-button title="Hinzufügen" text="Record hinzufügen" icon="add" link="#/search/add" />
    <highlight-button title="Dateien" text="Alle Anhänge" icon="attachment-photo" link="#/search?lang=en&query=&offset=0&model=file" />
    <highlight-button title="All User" text="List of all User" icon="person-placeholder" link="#/search?lang=en&query=&offset=0&model=user" />

    <!-- Line Break -->
    <new-line />
    
    <!-- Service Chart -->
    <chart typ="bar" name="Service Requests by status">
        <chart-data model="maintenance_request" action="count" variable="status" group_by="ident" name="New">
            <data-filter variable="status" operator="equal" value="new" />
        </chart-data>
        <chart-data model="maintenance_request" action="count" variable="status" group_by="ident" name="Scheduled">
            <data-filter variable="status" operator="equal" value="scheduled" />
        </chart-data>
        <chart-data model="maintenance_request" action="count" variable="status" group_by="ident" name="In process">
            <data-filter variable="status" operator="equal" value="in_process" />
        </chart-data>
        <chart-data model="maintenance_request" action="count" variable="status" group_by="ident" name="Done">
            <data-filter variable="status" operator="equal" value="done" />
        </chart-data>
    </chart>
    
    <!-- Order Chart -->
    <chart typ="doughnut" name="Orders by status">
        <chart-data model="order" action="count" variable="status" group_by="ident" name="New">
            <data-filter variable="status" operator="equal" value="new" />
        </chart-data>
        <chart-data model="order" action="count" variable="status" group_by="ident" name="Delivered">
            <data-filter variable="status" operator="equal" value="delivered" />
        </chart-data>
        <chart-data model="order" action="count" variable="status" group_by="ident" name="Pending">
            <data-filter variable="status" operator="equal" value="pending" />
        </chart-data>
    </chart>
</home>
```

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