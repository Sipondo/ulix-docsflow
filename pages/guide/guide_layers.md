---
title: Introduction to Layers
keywords: getting started opening ldtk map editor
tags: [getting_started]
sidebar: guide_sidebar
permalink: guide_layers.html
folder: guide
summary: Introduces the concept of layers.
---

## 21-layer Worlds

The game world is built up by stacking many layers on top of eachother. The game will draw the lowest layer first and work its way up to the top layer. This means that the lower layers will contain the ground, flowers etc. while the top layers contain that what is high up in the air.

Let's look at an example. Say we want to this tree to a level.

{% include image.html file="tree_layered_full.png" alt="Picture of a tree" max-width=400 %}

<table>
<colgroup>
<col width="15%" />
<col width="55%" />
<col width="30%" />
</colgroup>
<thead>
<tr class="header">
<th>Layer</th>
<th>Description</th>
<th>Image</th>
</tr>
</thead>
<tbody>
<tr>
<td markdown="span">Ground</td>
<td markdown="span">The ground that the tree is standing on. Notice that the ground uses a variety of tiles, including some flowers. As the layers above </td>
<td markdown="span">{% include image.html file="tree_layered_0.png" alt="Picture of a tree" max-width=200 %}</td>
</tr>
</tbody>
</table>

{% include links.html %}
