---
title: Running Dexflow
keywords: getting started begin running dexflow game
tags: [getting_started, begin, install, running, dexflow, game]
sidebar: guide_sidebar
permalink: guide_running_dexflow.html
folder: guide
summary: This page will walk you through all the files and your first time running the game.
---

## Running Dexflow
Your folder will now look something like this:
{% include image.html file="filesystem.png" alt="Filesystem screenshot" max-width=350 %}


Let's briefly go over the files and folders:

 - `game`: Folder that houses the framework code. You won't have to interact with this unless you want to do crazy stuff.
 - `lib`: Irrelevant.
 - `resources`: Folder that houses all the resources of the game: art, sound, animations etc.
 - `world`: Folder that houses information specific to LDTK.
 - `autotile_reformat.bat`: Tool that allows you to translate Essentials Autotiles into Ulix Autotiles.
 - `compile_world.bat`: Tool that compiles any new changes you made to the world in LDTK to Ulix.
 - `develop.bat`: Shortcut for first compiling the world and afterwards playing the game.
 - `game.exe`: Your game!
 - `python3.dll`: Irrelevant.
 - `python38.dll`: Irrelevant
 - `streamingsave.usave`: The current savegame. Delete if you want to start the playthrough over.
 - `world.ldtkc`: Compiled version of the LDTK world (generated via `compile_world.bat`).


## Playing your game for the first time
Before you can run your game, you need to compile the game world (ldtk world).
You can do this by running `compile_world.bat`.
Afterwards, play your game by running `game.exe`.

{% include note.html content="If you are doing rapid iterations on your game world, you might want to use `develop.bat` instead. This is a shortcut for first compiling the world and afterwards playing the game." %}


{% include links.html %}

