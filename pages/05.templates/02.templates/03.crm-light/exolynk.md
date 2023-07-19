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

A lightweight and customizable CRM Tool to track Sales Opportunities in the following pipeline stages (status):
- 1/6 Prospecting
- 2/6 Qualification
- 3/6 Needs Analysis
- 4/6 Proposal
- 5/6 Negotiation
- 6/6 Closed Won
- 6/6 Closed Lost

**Supported features:**
- Opportunitiy Information
    - Priority (A-List / B-List / C-List)
    - Opportunity value
    - Forecast completion
    - Company information (number of employees, industry, address, contact details,..)
    - Assigning User with automated workflow to add new assigned leads to the selected sales user
    - Tracking of activities and correspondences
    - attachement (files, like Offer PDF`s, Pictures, etc.)
    - Chart for Opportunities by Stage
    - Record log for all user interactions
    - User access management with roles and rights (can be configured per variable and layout)
[/ui-tab]

[ui-tab title="Predefined Model Variables"]
> | Variable ident     | data type                       | Description
> |--------------------|---------------------------------|-----------------------------------------------------------------------|
> | contact_firstname          | String                          | Contact Firstname
> | contact_lastname           | String                          | Contact Lastname
> | client_phone               | String                          | Company Phone
> | client_email               | String                          | Company Email Address
> | client_start_date          | DateTime                        | Client Start Date
> | client_address             | Location                        | Location with Map-View, Street, Nr., ZIP, Country
> | contact_title              | String                          | Contact Title
> | contact_phone              | String                          | Contact Phone
> | contact_mobile             | String                          | Contact Mobile
> | contact_email              | String                          | Contact Email Address
> | client_website             | String                          | Company Website
> | contact_linkedin           | String                          | Contact LinkedIn Profile
> | crm_prio_select            | Selection                       | Options: A-List, B-List, C-List
> | client_info                | String (Multiline)              | Longtext field for general information to the client/lead
> | crm_activities             | Table                           | A Table with 3 columns: Date, Channel, Activity (Longtext Field)
> | assigned_user_1            | Reference -> Filter: User       | A reference to the assigned responsible user
> | opportunity_value_revenue  | Float                           | The value of the opportunity in CHF
> | opportunity_value_licenses | Integer                         | The value of the opportunity in amount of licenses
> | employees                  | Integer                         | The amount of emloyees at the prospect company
> | industry                   | String                          | The industry where the prospect company is in
> | exl_product_select         | Selection                       | Product Selection; Options: Starter, SME, Corporate
> | forecast_completion        | DateTime                        | The date of the forecasted deal completion
> | files                      | List Reference -> Filter: Files | A list of file attachements
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

**CRM Usage**

![CRM Usage](crm_capture.gif?resize=600&classes=left)

**Dashboard**

![Dashboard](crm_dashboard.png?resize=600&classes=left)

**Record Overview with Filter**

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