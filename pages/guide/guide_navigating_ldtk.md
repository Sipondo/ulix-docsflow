---
title: Navigating LDTK
keywords: getting started opening ldtk map editor
tags: [getting_started]
sidebar: guide_sidebar
permalink: guide_navigating_ldtk.html
folder: guide
summary: Introduces the main navigation elements in LDTK.
---

## The Toolbar

One of the main features of the LDTK user interface is the toolbar at the left side of the screen. This toolbar has multiple tabs. Let's go over them:

{% include image.html file="ldtk_toolbar.png" alt="LDTK toolbar" max-width=800 %}

- **World View [W]:** Toggle between world view and level view.
- **Project Settings [F1]:** Change several project-wide settings. You'll mostly just want to make sure that you have enabled `Backup on save`; I recommend setting `Max backup files` to `50`.
- **Current Level [F2]:** Level settings. Allows you to set level name, hardcode level size and specify the level-wide fields.
- **Layers [F3]:** Contains *worldwide* layer settings. You typically will not want to touch this!
- **Entities [F4]:** Contains *worldwide* entity definitions. This is again something to stay away from unless you know what you are doing.
- **Enums [F5]:** Contains *worldwide* enum definitions. Mostly used to define settables and switches for UPL.
- **Tilesets [F6]:** Contains *worldwide* tileset definitions. This is where you add new tilesets, give them collision and other tile-specific behaviours such as hopping and encounters.
- **Cheat Sheet [H]:** Your new best friend! Contains most if not all useful shortcuts.
- **Close Project [CTRL+W]:** The exit button.


{% include warning.html content="The orange tabs contain most of the delicate internals of our project. The tileset tab is generally the only orange tab you'll need to access. Be careful when operating in these tabs." %}



{% include links.html %}
