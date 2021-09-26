---
title: Connecting an Instance
keywords: getting started opening ldtk map editor
tags: [getting_started]
sidebar: guide_sidebar
permalink: guide_connecting_instances.html
folder: guide
summary: Build a functional house.
---

# Connecting an instance to a map
We've made an example map, but how do we connect maps to eachother? This particular page will go over connecting an instance to a map. Recall that instances are "submaps" that are contained within a standalone map. We'll go over connecting a house to the map it's located in.

These are my two maps:

{% include image.html file="instance_teleport_maps.png" alt="Outside and a house" max-width=800 %}

{% include note.html content="As Our House is the first instance contained within Level 7 we call it 'L7_I1_OurHouse'." %}

## Portal regions
Regions are handy little objects that mark zones on the ground. When any entities (such as the player) enter a region or leave a region they fire an action, allowing something to happen.
In our case we want something to happen when the player walks on top of the door and exit tiles. Normally you have to program the action triggered by the region yourself, but as this is a special behaviour that is used a lot you should use the prefabricated "Portal" region instead.



{% include links.html %}
