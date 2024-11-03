---
layout: main

authors: "Siggles" # Authors of the mod
title: Ambient Spawns # Title of the mod
version: "1.0.0" # Version of the mod
supported: "BL2" # Supported games; currently can only display as "BL2", "BL2 + TPS", or "TPS"

tagline: "Periodically spawns random groups of enemies, optionally from other maps." # A short description of the mod itself.
description: "Periodically spawns random groups of enemies, optionally from other maps." # This is set in order to keep the SEO proper
longDescription: "Periodically spawns random groups of enemies.\nThe intention is to make the game more unpredictable.\n\nIt matches spawn points to enemies with spawn animations, so it doesn't look too janky.\nOptions for spawn frequency and distance to the player, and which enemies to use:\nDen		- Only spawns enemies that usually spawn from a chosen point.\nLevel	- Only spawns enemies loaded in the current level.\nDLC*	- May spawn any custom enemy groups from the current DLC (or base game).\nGame*	- May spawn any custom enemy groups from the entire game.\n*These options require all available enemies to be loaded upon reaching the start menu.\n*This causes some visual texture bugs, and possibly crashes." # Description of what the mod can do
categories: ['Gameplay'] # Category of the type of mod

requirements: ['UserFeedback >= 1.6'] # Requirements for the given mod
requirementTitles: ['UserFeedback'] # The link-friendly name of the requirements

issues: "https://github.com/Siggless/bl-sdk-mods/issues"
download: "https://github.com/Siggless/bl-sdk-mods/raw/main/AmbientSpawns/AmbientSpawns.zip"
source: "https://github.com/Siggless/bl-sdk-mods/tree/main/AmbientSpawns" # Link to source code
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
