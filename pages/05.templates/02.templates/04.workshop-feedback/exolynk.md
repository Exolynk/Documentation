---
title: 'Workshop Feedback'
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


<p class="ui5-icon" style="font-size: 4em;" name="wrench">&#xe149;</p>

<br><br><br><br>

## Workshop Feedback Tool

[downloads route="/downloads/model-templates/workshop-feedback" layout="list-files" width="300" /]

<br>


[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Description"]

A workshop feedback tool as it was used at the Zürioberland Forum 2023 to collect workshop feedback over 5 workshops and totally 40 questions. Each Model represents one workshop with different questions.

Here you will find a summary about this workshop: <a href="Zuerioberland-Forum-2023-Stationaere-Arbeit.pdf" target="_blank">Zuerioberland Forum 2023 Stationäre Arbeit</a>

**Supported features:**
- Participant Information
- Workshop Feedback collection (Multiple Choise)
- Complex User Workflow and Service
    - Bulk user login generator
    - Bulk permission granting
    - Autocreate feedback records for each user 
- Evaluation chart for Feedbacks
- Record log for all user interactions
- User access management with roles and rights (can be configured per variable and layout)

![Slide 1](ZOB_Slide_1.png?resize=600&classes=left)

![Slide 2](ZOB_Slide_2.png?resize=600&classes=left)

![Slide 3](ZOB_Slide_3.png?resize=600&classes=left)

[/ui-tab]

[ui-tab title="Predefined Model Variables"]
> | Variable ident             | data type                       | Description
> |----------------------------|---------------------------------|-----------------------------------------------------------------------|
> | branche                    | Selection                       | A selection with different industries
> | andere_branche             | String                          | If nothing fits a freetext field for industry
> | mitarbeitende              | Selection                       | Options: 1-5, 6-10, 11-20, 21-50, 50+
> | feedback_1                 | Bool                            | Yes/No Question
> | feedback_2                 | Bool                            | Yes/No Question
> | feedback_3                 | Bool                            | Yes/No Question
> | feedback_4                 | Bool                            | Yes/No Question
> | feedback_5                 | Bool                            | Yes/No Question
> | feedback_6                 | Bool                            | Yes/No Question
> | feedback_7                 | Bool                            | Yes/No Question
> | feedback_8                 | Bool                            | Yes/No Question
[/ui-tab]

[ui-tab title="Dashboard Layout"]
```html
<home>
    <highlight-button title="All Workshops" text="Workshop Feedback" icon="meeting-room" link="#/search" />
    <highlight-button title="Workshop 1" text="Workshop Feedback" icon="meeting-room" link="#/search?lang=en&query=&model=feedback_workshop_1&status=&view=List&print=false&tab=" />
    <highlight-button title="Workshop 2" text="Workshop Feedback" icon="meeting-room" link="#/search?lang=en&query=&model=feedback_workshop_2&status=&view=List&print=false&tab=" />
    <highlight-button title="Workshops 3" text="Workshop Feedback" icon="meeting-room" link="#/search?lang=en&query=&model=feedback_workshop_3&status=&view=List&print=false&tab=" />
    <highlight-button title="Workshops 4" text="Workshop Feedback" icon="meeting-room" link="#/search?lang=en&query=&model=feedback_workshop_4&status=&view=List&print=false&tab=" />
    <highlight-button title="Workshops 5" text="Workshop Feedback" icon="meeting-room" link="#/search?lang=en&query=&model=feedback_workshop_5&status=&view=List&print=false&tab=" />
    <highlight-button title="Workshops 6" text="Workshop Feedback" icon="meeting-room" link="#/search?lang=en&query=&model=feedback_workshop_6&status=&view=List&print=false&tab=" />
</home>
```
[/ui-tab]

[ui-tab title="Screenshots"]

**Usage**

![Usage](screenshot-1.png?resize=600&classes=left)

**Evaluation**

![Evaluation](screenshot-2.png?resize=600&classes=left)

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