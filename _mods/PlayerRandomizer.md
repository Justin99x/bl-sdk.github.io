---
layout: main

authors: "Milo" # Authors of the mod
title: Player Randomizer # Title of the mod
version: "0.2" # Version of the mod
supported: "BL2 + TPS + AoDK" # Supported games; currently can only display as "BL2", "BL2 + TPS", or "TPS"

tagline: "Play with randomized skills and class mods." # A short description of the mod itself.
description: "Play with randomized skills and class mods." # This is set in order to keep the SEO proper
longDescription: "Fills a player's trees with random skills, and\nupdates class mods to boost skills from the new set.\n\nIdea stolen from Abahbob's Cross Class Skill Randomizer.\n\n# Usage:\nFrom the main menu, under Mods, enable 'Player\nRandomizer (New Seed)'.  Bring up Options-&gt;Mods-&gt;Player\nRandomizer to control how you want to randomize your\ncharacter.\n  - **Skill Sources** sets which characters to pull skills\nfrom.\n  - **Additional Skills** lets you include skills that\nshould work despite referencing the wrong Action Skill,\nas well as skills that may be nonfunctional or badly\nbroken.\n  - **Action Skill** determines which character's action\nskill to assign to yours; note that graphics may be\nwrong for some character/skill combinations, but the\neffects should still work correctly.\n  - **Skill Density** selects how much to fill in the skill\ntree - for reference, BL2 character trees are about 60%\nfull, while TPS trees average 65% full.\n  - **Randomizing Tier Points** changes how many skill\npoints it takes to unlock the next skill tier.\n  - **Randomize COMs** enables modifying the player's\nclassmods to contain skills from the new random tree.\n\nOnce you've made your choices, load your character and\nstart the session as usual.  The next time you launch\nthe game, the Mods menu will show a new enabled entry,\n'Effect Randomizer (#)', where the number is the\nnewly-generated effect seed.  Remember that seed - if\nthe game crashes, you'll need to re-enable that entry." # Description of what the mod can do
categories: ['Gameplay'] # Category of the type of mod

requirements: [] # Requirements for the given mod
requirementTitles: [] # The link-friendly name of the requirements

issues: ""
download: "https://github.com/ncalvin1/Milo-BL2-SDK-Mods/raw/refs/heads/main/PlayerRandomizer/PlayerRandomizer_v0.2.zip"
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
