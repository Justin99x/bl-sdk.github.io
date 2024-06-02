---
layout: main

authors: "FromDarkHell" # Authors of the mod
title: Skill Saver # Title of the mod
version: "1.0" # Version of the mod
supported: "BL2 + TPS" # Supported games; currently can only display as "BL2", "BL2 + TPS", or "TPS"

tagline: "Allows for you to save your current skill build and then restore right back to it later!" # A short description of the mod itself.
description: "Allows for you to save your current skill build and then restore right back to it later!" # This is set in order to keep the SEO proper
longDescription: "This mod gives you the ability to save your current skill build, then restore right back to it later.\nWhen in game, hit your `Manage Skill Layouts` bind (Default: F3)\nThen choose whether or not you want to save your current skill build, then type in your skill build's name!\nFrom here, you can then restore back to that build for your current character class" # Description of what the mod can do
categories: ['Utility', 'Gameplay'] # Category of the type of mod

requirements: ['UserFeedback >= 1.5'] # Requirements for the given mod
requirementTitles: ['UserFeedback'] # The link-friendly name of the requirements

issues: ""
download: "https://github.com/FromDarkHell/bl-sdk-mods/blob/main/SkillSaver/SkillSaver.zip?raw=true"
source: "https://github.com/FromDarkHell/bl-sdk-mods" # Link to source code
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