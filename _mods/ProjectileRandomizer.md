---
layout: main

authors: "RedxYeti" # Authors of the mod
title: Projectile Randomizer # Title of the mod
version: "1.0" # Version of the mod
supported: "BL2 + TPS" # Supported games; currently can only display as "BL2", "BL2 + TPS", or "TPS"

tagline: "Randomizes Projectiles on weapons and grenades." # A short description of the mod itself.
description: "Randomizes Projectiles on weapons and grenades." # This is set in order to keep the SEO proper
longDescription: "****WARNING: THIS MOD CAN HAVE LOTS OF FLASHING LIGHTS AND OFTEN IS VERY LOUD****\n****RECOMMNDED YOU HAVE YOUR VOLUME LOW****\n\nVideo Startup Guide Here: https://www.youtube.com/watch?v=liQ26DvCO3w \nThis mod will randomize projectiles all over your game. There's 2 types of things it randomizes. One is Firing Modes and the other is Projectiles.\n\nFiring modes are mostly used on weapons. Guns and vehicles use them.\n\nProjectiles are mostly used on grenades, however firing modes can have projectiles tied to them. \nYou'll find most weapons with different projectiles than thier firing modes, the projectile will come out of the weapon.\nProjectiles and Firing Modes will show on the item card.\n\nWeapons also have a 50/50 chance of projectiles being changed or even added to their firing mode.\n\nYou'll see on the item card what each has been randomized to. \n\nRequirements:\nHD Texture pack UNINSTALLED, your game will crash with the HD Pack on.\n\nSuggested:\nDXVK: https://github.com/doitsujin/dxvk/releases/tag/v2.4\nPlace d3d9.dll from the x32 folder in the same folder as bl2/tps exe\n\n4gb patch: https://ntcore.com/4gb-patch/\nrun it, and select your bl2/tps exe\n\n\nPrepping the randomizer:\nI HIGHLY recommend you use the prep projectile randomizer option in the main menu.\nIt will load multiple levels until it's found the set amount of firing modes and projectiles.\n\nIt only takes 2-3 minutes (depending on your PC) and you'll be set for your entire session.\n\nIf you find your game crashing while trying to use the randomizer prep, id recommend lowering projectiles first, then firing modes.\n\nYou can also use the 4gb patch on the exe, which may help a bit. \n\n\nSaving Items:\nItems will get saved to a json file in 'saves' in the projectile randomizer. The save number will be the same as your character save number.\n\nYou can edit these saves by replacing the parts that you want.\nYoull just have to find the barrel, Firing mode, and/or projectile you want to replace in the json." # Description of what the mod can do
categories: ['Gameplay'] # Category of the type of mod

requirements: [] # Requirements for the given mod
requirementTitles: [] # The link-friendly name of the requirements

issues: ""
download: "https://github.com/RedxYeti/Yeti-BL2-SDK-Mods/blob/main/ProjectileRandomizer"
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
