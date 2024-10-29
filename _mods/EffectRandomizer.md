---
layout: main

authors: "Milo" # Authors of the mod
title: Effect Randomizer # Title of the mod
version: "0.1" # Version of the mod
supported: "BL2 + TPS + AoDK" # Supported games; currently can only display as "BL2", "BL2 + TPS", or "TPS"

tagline: "Lose your knowledge of what does what." # A short description of the mod itself.
description: "Lose your knowledge of what does what." # This is set in order to keep the SEO proper
longDescription: "Changes subtle aspects of most game items, so they no\nlonger behave completely as expected.\n\n# Alterations:\n\n  - Projectiles may borrow each other's behaviors.  They\ncan make unexpected noises, follow odd paths, or even\nhome.\n  - Firing modes can lase, split, ricochet, or change\nspeeds.\n  - Parts have different effects on shield behavior.\nA common Absorb shield with lucky parts may beat a Sham.\n  - The same applies to classmods.  With good parts,\na high-level mod could potentially boost a skill more\nthan +6.\n  - Lastly, relics now boost random attributes.  Really\nwant an artifact that improves corrosion damage and \nmovement speed?  It might be out there...\n*Note: relics are not supported on TPS.  Oz kits have\nenough quirks already.*\n# Usage:\nFrom the main menu, under Mods, enable 'Effect\nRandomizer (New Seed)'.  Bring up Options-&gt;Mods-&gt;Effect\nRandomizer to enable the effects you want to change,\nthen load your character and start the session as usual.\nThe next time you launch the game, the Mods menu will\nshow a new enabled entry, 'Effect Randomizer (#)',\nwhere the number is the newly-generated effect seed.\nRemember that seed - if the game crashes, you'll need\nto re-enable that entry.\n" # Description of what the mod can do
categories: ['Gameplay'] # Category of the type of mod

requirements: ['Change Util >= 0.1'] # Requirements for the given mod
requirementTitles: ['ChangeUtil'] # The link-friendly name of the requirements

issues: ""
download: "https://github.com/ncalvin1/Milo-BL2-SDK-Mods/raw/refs/heads/main/EffectRandomizer/EffectRandomizer_v0.1.zip"
source: "https://github.com/ncalvin1/Milo-BL2-SDK-Mods" # Link to source code
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
