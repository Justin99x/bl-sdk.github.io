---
layout: main

authors: "LaryIsland" # Authors of the mod
title: Melee Enhancement # Title of the mod
version: "1.0" # Version of the mod
supported: "BL2" # Supported games; currently can only display as "BL2", "BL2 + TPS", or "TPS"

tagline: "A few tweaks to Zer0 and Krieg to enhance their melee gameplay." # A short description of the mod itself.
description: "A few tweaks to Zer0 and Krieg to enhance their melee gameplay." # This is set in order to keep the SEO proper
longDescription: "A few tweaks to Zer0 and Krieg to enhance their melee gameplay\n\nZer0\nFearless increases shield recharge delay, and Kunai no longer inflict self damage\nKrieg\nSilence the Voices self-hit chance scales down, and Buzz Axe Bombadier causes slag explosions" # Description of what the mod can do
categories: ['Gameplay'] # Category of the type of mod

requirements: ['Structs >= 1.1'] # Requirements for the given mod
requirementTitles: ['Structs'] # The link-friendly name of the requirements

issues: "https://github.com/LaryIsland/bl-sdk-mods/issues"
download: "https://github.com/LaryIsland/bl-sdk-mods/raw/main/MeleeEnhancement/MeleeEnhancement.zip"
source: "https://github.com/LaryIsland/bl-sdk-mods/tree/main/MeleeEnhancement" # Link to source code
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
