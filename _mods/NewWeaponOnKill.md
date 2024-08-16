---
layout: main

authors: "RedxYeti" # Authors of the mod
title: New Weapon On Kill # Title of the mod
version: "1.0" # Version of the mod
supported: "BL2" # Supported games; currently can only display as "BL2", "BL2 + TPS", or "TPS"

tagline: "Get a random weapon after getting a kill or kills." # A short description of the mod itself.
description: "Get a random weapon after getting a kill or kills." # This is set in order to keep the SEO proper
longDescription: "After getting in game you'll want to enable the mod and choose your options. Also you can set up a hotkey to change weapons. \n\nOptions include:\nWeapon Type\nLegit, cursed or very cursed weapons\nHow many kills between swaps\nShowing the new weapon name on screen\n\nKnown Issues:\nGaige sometimes gets shotguns with 0 shot mags youll have to reroll manually.\n\nPlaying online:\nIf you have a gunzerker theyll want to host of thier action skill weapons will not swap properly.\nIf the gunzerker cannot host, they just need to press 2 or the dpad every after getting kills for the second gun to show up.\n\nNon hosts pressing the hotkey may get their backpack overflown. just drop all the weapons from your backpack to fix it.\n" # Description of what the mod can do
categories: ['Gameplay'] # Category of the type of mod

requirements: [] # Requirements for the given mod
requirementTitles: [] # The link-friendly name of the requirements

issues: ""
download: "https://github.com/RedxYeti/Yeti-BL2-SDK-Mods/tree/main/NewWeaponOnKill"
source: "https://github.com/RedxYeti/Yeti-BL2-SDK-Mods" # Link to source code
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
