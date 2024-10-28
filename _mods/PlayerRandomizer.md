---
layout: main

authors: "Milo" # Authors of the mod
title: Player Randomizer # Title of the mod
version: "0.1" # Version of the mod
supported: "BL2 + TPS + AoDK" # Supported games; currently can only display as "BL2", "BL2 + TPS", or "TPS"

tagline: "Play with randomized skills and class mods." # A short description of the mod itself.
description: "Play with randomized skills and class mods." # This is set in order to keep the SEO proper
longDescription: "Fills a player's trees with random skills, and<br>updates class mods to boost skills from the new set.<br><br>Idea stolen from Abahbob's Cross Class Skill Randomizer.<br><br><h3>Usage:</h3><br>From the main menu, under Mods, enable 'Player<br>Randomizer (New Seed)'.  Bring up Options-&gt;Mods-&gt;Player<br>Randomizer to control how you want to randomize your<br>character.<ul><li>Skill Sources sets which characters to pull skills<br>from.</li><li>Additional Skills lets you include skills that<br>should work despite referencing the wrong Action Skill,<br>as well as skills that may be nonfunctional or badly<br>broken.</li><li>Action Skill determines which character's action<br>skill to assign to yours; note that graphics may be<br>wrong for some character/skill combinations, but the<br>effects should still work correctly.</li><li>Skill Density selects how much to fill in the skill<br>tree - for reference, BL2 character trees are about 60%<br>full, while TPS trees average 65% full.</li><li>Randomizing Tier Points changes how many skill<br>points it takes to unlock the next skill tier.</li><li>Randomize COMs enables modifying the player's<br>classmods to contain skills from the new random tree.</li></ul><br>Once you've made your choices, load your character and<br>start the session as usual.  The next time you launch<br>the game, the Mods menu will show a new enabled entry,<br>'Effect Randomizer (#)', where the number is the<br>newly-generated effect seed.  Remember that seed - if<br>the game crashes, you'll need to re-enable that entry." # Description of what the mod can do
categories: ['Gameplay'] # Category of the type of mod

requirements: [] # Requirements for the given mod
requirementTitles: [] # The link-friendly name of the requirements

issues: ""
download: "https://github.com/ncalvin1/Milo-BL2-SDK-Mods/raw/refs/heads/main/PlayerRandomizer/PlayerRandomizer_v0.1.zip"
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
