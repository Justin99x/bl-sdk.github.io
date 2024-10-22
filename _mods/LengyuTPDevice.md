---
layout: main

authors: "Lengyu" # Authors of the mod
title: Lengyu TP Device # Title of the mod
version: "1.2" # Version of the mod
supported: "BL2 + TPS" # Supported games; currently can only display as "BL2", "BL2 + TPS", or "TPS"

tagline: "Allows you to teleport yourself anywhere you marked." # A short description of the mod itself.
description: "Allows you to teleport yourself anywhere you marked." # This is set in order to keep the SEO proper
longDescription: "Allows you to teleport yourself anywhere you marked. \n1.Press NUM0 to mark the location. \n2.Press NUMdot to teleport.\n3.Press NUM1-3 to switch within 3 slots.\n\nIt doesn't work in the map Digistruct Peak." # Description of what the mod can do
categories: ['Utility'] # Category of the type of mod

requirements: ['UserFeedback >= 1.6'] # Requirements for the given mod
requirementTitles: ['UserFeedback'] # The link-friendly name of the requirements

issues: ""
download: "https://raw.githubusercontent.com/aa3615058/Lengyu-BL2-sdk-Mods/main/LengyuTPDevice/LengyuTPDevice.zip"
source: "https://github.com/aa3615058/Lengyu-BL2-sdk-Mods" # Link to source code
license: ['MIT', 'https://choosealicense.com/licenses/mit'] # License name, link about the license from https://choosealicense.com/

---
**Contents**
* TOC
{:toc}

## {{page.title}}

Mod by: {{page.authors}}
Current Version: {{page.version}}

<p></p>
### Description

{{page.longDescription | markdownify }}

Currently Supports: `{{page.supported}}`

{% if page.categories.size > 0 %}
Categories:
{% for category in page.categories %}
  * [{{category}}](/types/{{category}})
{% endfor %}
<p></p>
{% endif %}

{% if page.requirements.size > 0 %}
### Requirements

{% for requirement in page.requirements %}

{% assign reqName = page.requirementTitles[forloop.index0] %}

{% for mod in site.mods %}

{% assign modName = mod.path | remove_first: '_mods/' %}
{% assign xz = reqName | append: '.md' %}

{% if modName == xz %}
* [{{ requirement }}]( {{ reqName | relative_url | prepend: '/mods'}} ) <sup>[(Direct Download)]({{mod.download}})</sup>
{% endif %}
{% endfor %}

{% endfor %}
<p></p>
{% endif %}

### Links

{% if page.download != "" %}
You can download {{page.title}} here: [Download Link]({{page.download}})
{% endif %}

{% if page.issues != "" %}
Report issues here: [Issue Tracker]({{page.issues}})
{% endif %}

{% if page.source != "" %}
View the source code here: [Source Code]({{page.source}})
{% endif %}

{% if page.license.size > 0 %}
This mod is licensed using {{page.license[0]}} <sup>[?]({{page.license[1]}})</sup>
{% endif %}
