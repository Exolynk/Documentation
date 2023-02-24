# Documentation
Welcome to the Exolynk system documentation.

**Important Note:** the [Exolynk Documentation CMS](https://docs.exolynk.com) used some specific tags and syntaxes which are described [here](https://docs.exolynk.com/contribution/docs-syntax) some of them will not be rendered as a proper Markup on GitHub, please use therefore our [Exolynk Documentation CMS](https://docs.exolynk.com).


## Navigation
- __Documentation__
   - [README.md](README.md)
   - [\_config.yml](_config.yml)
   - [chapter.md](chapter.md)
   - __pages__
     - __01.Use\-of\-exolynk__
       - __01.getting\-started__
         - [exolynk.md](pages/01.Use-of-exolynk/01.getting-started/exolynk.md)
       - __02.configuration__
         - [exolynk.md](pages/01.Use-of-exolynk/02.configuration/exolynk.md)
       - [chapter.md](pages/01.Use-of-exolynk/chapter.md)
     - __02.Exolynk\-modeler__
       - __01.layouting\-reference__
       - [exolynk.md](pages/02.Exolynk-modeler/exolynk.md)
     - __03.Rune\-language__
       - __01.introduction__
         - [exolynk.md](pages/03.Rune-language/01.introduction/exolynk.md)
       - __02.getting\-started__
         - [exolynk.md](pages/03.Rune-language/02.getting-started/exolynk.md)
       - __03.concepts__
         - __01.items\-and\-imports__
           - [exolynk.md](pages/03.Rune-language/03.concepts/01.items-and-imports/exolynk.md)
         - __02.functions__
           - [exolynk.md](pages/03.Rune-language/03.concepts/02.functions/exolynk.md)
         - __03.control\-flow__
           - [exolynk.md](pages/03.Rune-language/03.concepts/03.control-flow/exolynk.md)
         - __04.variables\-and\-memory__
           - [exolynk.md](pages/03.Rune-language/03.concepts/04.variables-and-memory/exolynk.md)
         - __05.loops__
           - [exolynk.md](pages/03.Rune-language/03.concepts/05.loops/exolynk.md)
         - __06.pattern\-matching__
           - [exolynk.md](pages/03.Rune-language/03.concepts/06.pattern-matching/exolynk.md)
         - __07.template\-literals__
           - [exolynk.md](pages/03.Rune-language/03.concepts/07.template-literals/exolynk.md)
         - __08.instance\-functions__
           - [exolynk.md](pages/03.Rune-language/03.concepts/08.instance-functions/exolynk.md)
         - [exolynk.md](pages/03.Rune-language/03.concepts/exolynk.md)
       - __04.built\-in\-types__
         - __01.primitives\-and\-references__
           - [exolynk.md](pages/03.Rune-language/04.built-in-types/01.primitives-and-references/exolynk.md)
         - __02.vectors__
           - [exolynk.md](pages/03.Rune-language/04.built-in-types/02.vectors/exolynk.md)
         - __03.objects__
           - [exolynk.md](pages/03.Rune-language/04.built-in-types/03.objects/exolynk.md)
         - __04.tuples__
           - [exolynk.md](pages/03.Rune-language/04.built-in-types/04.tuples/exolynk.md)
         - [exolynk.md](pages/03.Rune-language/04.built-in-types/exolynk.md)
       - __05.dynamic\-types__
         - __01.structs__
           - [exolynk.md](pages/03.Rune-language/05.dynamic-types/01.structs/exolynk.md)
         - __02.enums__
           - [exolynk.md](pages/03.Rune-language/05.dynamic-types/02.enums/exolynk.md)
         - [exolynk.md](pages/03.Rune-language/05.dynamic-types/exolynk.md)
       - __06.try\-operator__
         - [exolynk.md](pages/03.Rune-language/06.try-operator/exolynk.md)
       - __07.generators__
         - [exolynk.md](pages/03.Rune-language/07.generators/exolynk.md)
       - __08.closures__
         - [exolynk.md](pages/03.Rune-language/08.closures/exolynk.md)
       - __09.asynchronous\-programming__
         - __01.streams__
           - [exolynk.md](pages/03.Rune-language/09.asynchronous-programming/01.streams/exolynk.md)
         - [exolynk.md](pages/03.Rune-language/09.asynchronous-programming/exolynk.md)
       - __10.macros__
         - [exolynk.md](pages/03.Rune-language/10.macros/exolynk.md)
       - [exolynk.md](pages/03.Rune-language/exolynk.md)
     - __04.Language\-api__
       - __01.base\-api__
         - [exolynk.md](pages/04.Language-api/01.base-api/exolynk.md)
       - __02.service\-and\-server\-specific\-api__
         - [exolynk.md](pages/04.Language-api/02.service-and-server-specific-api/exolynk.md)
       - __03.workflow\-and\-webapp\-specific\-api__
         - [exolynk.md](pages/04.Language-api/03.workflow-and-webapp-specific-api/exolynk.md)
       - [chapter.md](pages/04.Language-api/chapter.md)
     - __05.contribution__
       - __01.docs\-syntax__
         - [docs\-syntax.md](pages/05.contribution/01.docs-syntax/docs-syntax.md)
       - __02.contribution\-rules__
       - [chapter.md](pages/05.contribution/chapter.md)
     - [chapter.md](pages/chapter.md)
     - __feed__
       - [docs.md](pages/feed/docs.md)

<br>

### Little helper to generate md Navigation
https://github.com/michalbe/md-file-tree

Dependencies: **tree**

Installation under MacOS: ```brew install tree```

<br>


## File Structure for Documentation CSM
```bash
└── pages
    ├── 01.Use-of-exolynk
    │   ├── 01.getting-started
    │   │   └── exolynk.md
    │   ├── 02.configuration
    │   │   └── exolynk.md
    │   └── chapter.md
```

#### Instruction

1. For each document (*.md file) a separate folder is neccesary
2. The folder has to be named as following: ```ORDER#.``` (two digits) ```FILENAME``` (lowercase) Example: ```01.``` ```getting-started```
3. The File name needs to be allways ```exolynk.md``` (twig-template)
4. The file title is specified in the document header as following:
```bash
---
title: 'Getting started'
taxonomy:
    category: docs
process:
    twig: true
---
```