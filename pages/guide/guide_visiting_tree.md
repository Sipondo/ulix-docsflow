---
title: Visiting our tree
keywords: getting started opening ldtk map editor
tags: [getting_started]
sidebar: guide_sidebar
permalink: guide_visiting_tree.html
folder: guide
summary: Let's view our first level in-game!
---

## Viewing our tree in-game
Let's pay a visit to our new level. There are two files in your game folder that allow you to run your game:
- `game.exe` opens the game normally.
- `develop.bat` compiles the world before opening the game.

You will always have to compile the world before you see any changes made in LDTK come into effect. Run `develop.bat` to compile the world and open your game.

### Getting to our tree
If your game is like me, you'll be dropped in the middle of one of the example maps. We haven't yet connected our new map to the game world and thus are not able to normally get to that area. As we are developing the game, however, we can use the developer console in order to teleport to the new area directly.

Pressing **[T]** while in-game opens up the developer console. This is a powerful feature for testing stuff out to bring your world to life, but currently we are only interested in teleporting to our new map.
Teleporting is done simply by entering the level number and pressing **[enter]**. As my tree level is called "L7_HelloTree" I can travel to that location by entering "7" and pressing **[enter]**.

{% include note.html content="Pressing **[H]** while playing the game will toggle collisions, allowing you to get out of any trees you might warp into!" %}

{% include image.html file="tree_behind.png" alt="Behind a tree" max-width=350 %}

Hooray! Our level works. Make sure to test out the collision and the level depth by moving behind the trees.

Feel free to experiment with your map. You can for example alter it's size and add paths, water and flowers. The rest of the mapping section will expect you to be able to work with layers and go over other concepts.

{% include links.html %}
