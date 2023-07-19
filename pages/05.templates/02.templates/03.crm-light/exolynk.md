---
title: 'CRM Light'
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


<p class="ui5-icon" style="font-size: 4em;" name="wrench">&#xe114;</p>

<br><br><br><br>

## Customer Relationship Management

[downloads route="/downloads/model-templates/crm-light" layout="list-files" width="300" /]

<br>


[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Description"]

In tempor sed sapien eu porttitor. Aliquam cursus facilisis ante. Etiam neque nunc, blandit vel lacus et, faucibus accumsan lacus. Proin posuere varius purus quis faucibus. Quisque et enim vitae orci [placerat tincidunt](#) id ac eros. Fusce et gravida libero. 

Phasellus cursus odio ex, in **mattis lorem tincidunt** vel. Donec nibh odio, dapibus non ligula a, semper ornare massa. Nulla consectetur eu nunc sed ultrices. Integer at turpis dolor.

[ui-tabs position="top-left" active="0" theme="lite"]

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
    <highlight-button title="Opportunities" text="CRM Opportinities" icon="crm-sales" link="#/search?lang=en&query=&model=opportunities&status=&view=List&print=false&tab=" />
    <highlight-button title="All Leads" text="CRM Opportinities" icon="group-2" link="#/search?lang=en&query=&model=opportunities&status=&view=Table&print=false&tab=&cols=name+status+crm_prio_select+assigned_user_1+" />
    <!-- Line Break -->
    <new-line />    
    <highlight-button title="1/6 Prospecting" text="CRM Opportinities" icon="sys-find" link="#/search?lang=en&query=&model=opportunities&status=prospecting%2C+&view=Table&print=false&tab=&cols=name+status+crm_prio_select+assigned_user_1+" />
    <highlight-button title="2/6 Qualification" text="CRM Opportinities" icon="sys-find" link="#/search?lang=en&query=&model=opportunities&status=qualification%2C+&view=Table&print=false&tab=&cols=name+status+crm_prio_select+assigned_user_1+" />
    <highlight-button title="3/6 Needs Analysis" text="CRM Opportinities" icon="tools-opportunity" link="#/search?lang=en&query=&model=opportunities&status=needs_analysis%2C+&view=Table&print=false&tab=&cols=name+status+crm_prio_select+assigned_user_1+" />
    <highlight-button title="4/6 Proposal" text="CRM Opportinities" icon="sales-document" link="#/search?lang=en&query=&model=opportunities&status=proposal%2C+&view=Table&print=false&tab=&cols=name+status+crm_prio_select+assigned_user_1+" />
    <highlight-button title="5/6 Negotiation" text="CRM Opportinities" icon="discussion-2" link="#/search?lang=en&query=&model=opportunities&status=negotiation%2C+&view=Table&print=false&tab=&cols=name+status+crm_prio_select+assigned_user_1+" />
    <highlight-button title="6/6 Closed Won" text="CRM Opportinities" icon="competitor" link="#/search?lang=en&query=&model=opportunities&status=won_closed%2C+&view=Table&print=false&tab=&cols=name+status+crm_prio_select+assigned_user_1+" />
    <highlight-button title="6/6 Closed Los" text="CRM Opportinities" icon="sys-cancel" link="#/search?lang=en&query=&model=opportunities&status=lost_closed%2C+&view=Table&print=false&tab=&cols=name+status+crm_prio_select+assigned_user_1+" />

    <!-- Line Break -->
    <new-line />   
    <!-- Pipline Chart -->
    <chart typ="bar" name="Pipline Opportunity by Stage">
        <chart-data model="opportunities" action="count" variable="status" group_by="ident" name="New">
            <data-filter variable="status" operator="equal" value="new" />
        </chart-data>
        <chart-data model="opportunities" action="count" variable="status" group_by="ident" name="1/6 Prospecting">
            <data-filter variable="status" operator="equal" value="prospecting" />
        </chart-data>
        <chart-data model="opportunities" action="count" variable="status" group_by="ident" name="2/6 Qualification">
            <data-filter variable="status" operator="equal" value="qualification" />
        </chart-data>
        <chart-data model="opportunities" action="count" variable="status" group_by="ident" name="3/6 Needs Analysis">
            <data-filter variable="status" operator="equal" value="needs_analysis" />
        </chart-data>
        <chart-data model="opportunities" action="count" variable="status" group_by="ident" name="4/6 Proposal">
            <data-filter variable="status" operator="equal" value="proposal" />
        </chart-data>
        <chart-data model="opportunities" action="count" variable="status" group_by="ident" name="5/6 Negotiation">
            <data-filter variable="status" operator="equal" value="negotiation" />
        </chart-data>
        <chart-data model="opportunities" action="count" variable="status" group_by="ident" name="6/6 Closed Won">
            <data-filter variable="status" operator="equal" value="won_closed" />
        </chart-data>
        <chart-data model="opportunities" action="count" variable="status" group_by="ident" name="6/6 Closed Lost">
            <data-filter variable="status" operator="equal" value="lost_closed" />
        </chart-data>
    </chart>
</home>
```
[/ui-tab]

[ui-tab title="Screenshots"]

#### CRM Usage
![CRM Usage](crm_capture.gif?resize=600&classes=left)

#### Dashboard
![Dashboard](crm_dashboard.png?resize=600&classes=left)

#### Record Overview with Filter
![Record Overview](crm_overview.png?resize=600&classes=left)

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