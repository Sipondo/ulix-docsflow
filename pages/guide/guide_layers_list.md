---
title: Types of Layers
keywords: getting started opening ldtk map editor
tags: [getting_started]
sidebar: guide_sidebar
permalink: guide_layers_list.html
folder: guide
summary: Goes over all the different types of layers.
---

## 21 layers to choose from
We need to split our level up in many layers, building the game world from the ground up. Let's take a look at what layers we have to our disposal.

{% include image.html file="layergif.gif" alt="Gif scrolling over layers" max-width=300 %}

{% include important.html content="The layers are a tool for you to use. Decide on what kind of information you want to put on what layer and stick to your system. It's a good system as long as it works for you and makes sense to you!" %}
{% include note.html content="Tile layers in succession are labelled A, B, C etc.. There is no functional difference between these layers. Try to utilise earlier layers more than later ones." %}


<table>
<colgroup>
<col width="20%" />
<col width="80%" />
</colgroup>
<thead>
<tr class="header">
<th>Layer</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td markdown="span">Boundaries</td>
<td markdown="span">A 'fake' layer that is not drawn in-game, but is used as a guide to visualise the map boundaries. Clicking on rules and toggling the eye icon {% include inline_image.html file="eye.png" alt="Eye icon" %} toggles this map boundary view, showing a red outline where players are able to view the edge of the map.</td>
</tr>
<tr>
<td markdown="span">Regions</td>
<td markdown="span">A layer that contains marked areas which can be used for making things happen in your game (actions). These regions are not visible in-game.</td>
</tr>
<tr>
<td markdown="span">Sky A, B, C</td>
<td markdown="span">The top-most tile layers that are normally included in Dexflow. These tiles are drawn on top of anything else in the game and will never contribute collision.</td>
</tr>
<tr>
<td markdown="span">Entities B</td>
<td markdown="span">The 'high' entities layer. Used in situations where visible elevation is required, e.g. bridges. This layer receives collision information from any layers inbetween Entities A and B (Rooftops A, B, C and Collision B).</td>
</tr>
<tr>
<td markdown="span">Collision B</td>
<td markdown="span">Collision override layer for Entities B. Any collision information in here overwrites the collision that the tile normally would have for those in Entities B. The tiles themselves are not visible in-game.</td>
</tr>
<tr>
<td markdown="span">Rooftops A, B, C</td>
<td markdown="span">Tile layers that are below Entities B but above Entities A. Contain tiles that normally are above the player but are not sky-high, such as building rooftops and treetops. Additionally, this is where you'd put bridge tiles if you want to make a working bridge for Entities B and these layers are the main contributors to collision for Entities B.</td>
</tr>
<tr>
<td markdown="span">Entities A</td>
<td markdown="span">The primary entities layer which will house the player and all other npcs most of the time. Receives collision information from everything below it (as this is the bottom entities layer).</td>
</tr>
<tr>
<td markdown="span">Collision A</td>
<td markdown="span">Collision override layer for Entities A. Any collision information in here overwrites the collision that the tile normally would have for those in Entities A. The tiles themselves are not visible in-game.</td>
</tr>
<tr>
<td markdown="span">Structures A, B, C</td>
<td markdown="span">Tile layers that are just below Entities A. Typically you'll put walls, tree trunks and other structural things that collide with the player on these layers. The only technical difference between these layers and the Ground layers is that these draw on top of the Auto Layers.</td>
</tr>
<tr>
<td markdown="span">Auto Road A, B</td>
<td markdown="span">Automatic layer that is used for drawing roads.</td>
</tr>
<tr>
<td markdown="span">Auto Cliff A</td>
<td markdown="span">Automatic layer that is used for drawing cliffs. Cliffs that go up multiple levels should be drawn in a normal tile layer instead.</td>
</tr>
<tr>
<td markdown="span">Auto Water A</td>
<td markdown="span">Automatic layer that is used for drawing water.</td>
</tr>
<tr>
<td markdown="span">Ground A, B, C</td>
<td markdown="span">The last tile layers. Best used for anything that is below the feet of those on Entities A. Beware that these still contribute collision information to Entities A.</td>
</tr>
</tbody>
</table>

{% include note.html content="Not enough layers? While 21 layers should be plenty for nearly all use cases, advanced users can always add more layers to the world. Keep in mind that layers are worldwide and thus all levels will feature these extra layers. Removing layers is possible as well." %}

{% include links.html %}
