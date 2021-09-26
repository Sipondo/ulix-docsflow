---
title: Introduction to Layers
keywords: getting started opening ldtk map editor
tags: [getting_started]
sidebar: guide_sidebar
permalink: guide_layers.html
folder: guide
summary: Introduces the concept of layers.
---

## A world of many layers

The game world is built up by stacking many layers on top of eachother. The game will draw the lowest layer first and work its way up to the top layer. This means that the lower layers will contain the ground, flowers etc. while the top layers contain that what is high up in the air.

Let's look at an example. Say we want to this tree to a level.

{% include image.html file="tree_layered_full.png" alt="Picture of a tree" max-width=400 %}

Even though intuitively the tree is one solid object, we actually have to split it over multiple layers. This is because not every part of the tree interacts with our game world in the same way. We want to overlap the ground with the tree trunk and we want to be able to walk behind the top of the tree. Generally you will divide the tree over three layers in the following way:

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
<td markdown="span">Rooftops</td>
<td markdown="span">The upper branches of the tree. These tiles don't contribute collision as they are high up in the air. We want to be able to walk behind these tiles without hindrance which is why we split them from the base of the tree.</td>
<td markdown="span">{% include image.html file="tree_layered_2.png" alt="Picture of a tree" max-width=160 %}</td>
</tr>
<tr>
<td markdown="span">Structures</td>
<td markdown="span">The base of the tree that collides with the player. The tile that we are using here has non-transparent green shadow, but in Ulix a transparent shadow would be preferred.</td>
<td markdown="span">{% include image.html file="tree_layered_1.png" alt="Picture of a tree" max-width=160 %}</td>
</tr>
<tr>
<td markdown="span">Ground</td>
<td markdown="span">The ground that the tree is standing on. Notice that the ground uses a variety of tiles, including some flowers. As the layers above </td>
<td markdown="span">{% include image.html file="tree_layered_0.png" alt="Picture of a tree" max-width=160 %}</td>
</tr>
</tbody>
</table>

{% include links.html %}
