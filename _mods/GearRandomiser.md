---
layout: main

authors: "ZetaDæmon" # Authors of the mod
title: Gear Randomiser # Title of the mod
version: "1.0" # Version of the mod
supported: "BL2 + TPS + AoDK" # Supported games; currently can only display as "BL2", "BL2 + TPS", or "TPS"

tagline: "Randomises all gear in the game." # A short description of the mod itself.
description: "Randomises all gear in the game." # This is set in order to keep the SEO proper
longDescription: "Randomises all gear in the game.\nAdds options to additionally choose which character class mods will be locked to as well as a chaos mode which removes restrictions for weapons as to which parts spawn where on a gun.\nDoes not change how loot is obtained or enemy drops so it is highly suggested to also use a mod like Cold Dead Hands.\nAlso works with mods that add new gear to the game, you will just need to update parts for the randomiser in the mod enable window after running the other mod.\nIf progess is stuck due to weapon randomisation there is a backup button to re-randomise all weapons not belonging to the player." # Description of what the mod can do
categories: ['Gameplay'] # Category of the type of mod

requirements: ['Structs >= 1.0', 'Sanity Saver >= 2.2'] # Requirements for the given mod
requirementTitles: ['Structs', 'SanitySaver'] # The link-friendly name of the requirements

issues: ""
download: "https://github.com/ZetaDaemon/bl-sdk-mods/raw/main/GearRandomiser/GearRandomiser.zip"
source: "https://github.com/ZetaDaemon/bl-sdk-mods/" # Link to source code
license: ['GNU GPLv3', 'https://choosealicense.com/licenses/gpl-3.0'] # License name, link about the license from https://choosealicense.com/

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