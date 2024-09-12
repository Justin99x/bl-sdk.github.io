---
layout: main

authors: "Deceptix_" # Authors of the mod
title: Cleaning Up Pandora # Title of the mod
version: "1.0" # Version of the mod
supported: "BL2 + TPS" # Supported games; currently can only display as "BL2", "BL2 + TPS", or "TPS"

tagline: "Automatically sell items on the floor or in your backpack by pressing the 'Secondary Use' key." # A short description of the mod itself.
description: "Automatically sell items on the floor or in your backpack by pressing the 'Secondary Use' key." # This is set in order to keep the SEO proper
longDescription: "Adds the ability to sell items that are on the floor or in your backpack by pressing the 'Secondary Use' key.\n\nNOTE:\n<ul><li>Items that are favorited or equipped cannot be sold.</li><li>Controller users need to press 'Start' to sell items from their backpack</li><li>All sold items can be bought back from any vendor.</li></ul>" # Description of what the mod can do
categories: ['Utility'] # Category of the type of mod

requirements: [] # Requirements for the given mod
requirementTitles: [] # The link-friendly name of the requirements

issues: "https://github.com/Decept1x/Borderlands-Cleaning-Up-Pandora/issues"
download: "https://github.com/Decept1x/Borderlands-Cleaning-Up-Pandora/releases/tag/1.0"
source: "https://github.com/Decept1x/Borderlands-Cleaning-Up-Pandora/tree/main" # Link to source code
license: [] # License name, link about the license from https://choosealicense.com/

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
