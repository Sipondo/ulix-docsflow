---
title: Your first level
keywords: getting started opening ldtk map editor
tags: [getting_started]
sidebar: guide_sidebar
permalink: guide_hello_tree.html
folder: guide
summary: Let's build our first level!
---

# Hello tree!
We've had plenty of talk about the editor and layers - let's put this information into action!
We'll build a new level and populate it with a completely functional tree.

## Step 1: Create a level
Either zoom out massively, or press **[W]** (cheat sheet!) to go to the World View.
Right click and click on **[New Level]** to create a level.
Now click on the level to send you straight in!

## Step 2: Giving the level a (legal) name
Your new level will probably have a bit of a dubious name, e.g. "Level_15". This name is not legal in Ulix and will crash the game.
Press the current level tab **[F2]** to go to the level settings and disable **[Use auto identifier]**. This will allow you to rename your level.

There are two kinds of levels: levels and instance levels. The difference is that instance levels are levels within another level (such as a house), whereas levels are standalone. You define your level to be a level or instance level via the naming scheme:

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th>Level</th>
</tr>
</thead>
<tbody>
<tr>
<td markdown="span">{% include image.html file="level_name.png" alt="Level name" max-width=800 %}</td>
</tr>
<tr>
<td markdown="span">-**Tall red rectangle:** unique level ID (Capital L + number from 1 to 999)<br/>
-**Low blue rectangle:** name of the level in Pascal Case, no underscores allowed.</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th>Instance</th>
</tr>
</thead>
<tbody>
<tr>
<td markdown="span">{% include image.html file="instance_name.png" alt="Instance name" max-width=800 %}</td>
</tr>
<tr>
<td markdown="span">-**Tall red rectangle:** containing unique level ID (Capital L + number from 1 to 999)
<br/>
-**Green circle:** unique instance ID (Capital i + number from 1 to 999)
<br/>
-**Low blue rectangle:** name of the level in Pascal Case, no underscores allowed.</td>
</tr>
</tbody>
</table>

In my LDTK world level 7 seems to be available. A good name would thus be "L7_HelloTree".

## Step 3: Shaping the ground
Great! We have a level, but it is quite empty. Let's start with adding some ground for our players to walk on.
Scroll all the way to Ground A and select that layer to start painting the level. I suggest taking one of the above grass tiles to start with.
    
{% include image.html file="instance_name.png" alt="Instance name" max-width=800 %}

{% include links.html %}
