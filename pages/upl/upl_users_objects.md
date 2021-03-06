---
title: Users & Objects
keywords: UPL Ulix Parsed Language Users Objects
tags: [documentation, upl]
sidebar: guide_sidebar
permalink: upl_users_objects.html
folder: upl
summary: "The objects you can interact with in-game and how to use them"
---

## Objects

Up until here we have seen that every UPL action requires some "thing" to execute the functions. This is what we call the user.
To discuss what can be a user, we first need to define an object within UPL. An object is in the most basic sense: *anything that can be interacted with in any way*.
What we mean by this is that an object can have attributes that can be accessed and changed, or can be made to execute functions.
A user is also an object. The only difference between a user and other objects is that the user is the *subject* of the line of code.
This means the user is the *ONLY* object that can execute a function call within a line.

## Examples

```ruby
game: Cinematic()
player: Say("Hello!")
game: Overworld()
```

In the syntax example we can see 2 types of objects:
 - player
 - game

```ruby
set: story_chapter = 3
self: Move(e_uid.x, e_uid.y + 1)
```

Here we see another 3 objects: *set*, *self* and *e_uid*. *e_uid* is the *entity_uid* defined when you place an entity in Ldtk. (Green rectangle)

{% include image.html file="entity_uid.png" alt="e uid" max-width=800 %}


## Users as *subjects*
In the first example above, both *player* and *game* are users. That does not mean they cannot also be used in the function following it. Let's say we want to make the player walk 5 tiles to the right. This can be achieved by making the player both the subject and the object of the function:
```ruby
player: Move(player.x + 5, player.y)
```
Notice that we now have the player as a user, but we also access its attributes within the same line! While this works, we have a shorthand for this:
```ruby
player: Move(x + 5, y)
```
This script will achieve the exact same thing. When we don't define the object we want to access, the script will automatically take the user of the line and use their attributes instead.

Let's say that we want to make a different object walk to that tile 5 to the east of the player to take their spot for a battle.
```ruby
e_uid: Move(player.x + 5, player.y)
```
Notice that since the entity is the one moving, it has to be the user! The player is now not the subject of the line, so we have to specify that we need the player's attributes instead of the entity's.

## Special objects

 - **game** <br/>
We have mentioned the *game* object before. This is a special type of object, because it is exactly what it says: the object that controls the entire game. It is mainly used to switch between the overworld, cinematics, shops, storage and other things that would change the way the player interacts with the game. Notice that the Cinematic() and Overworld() functions are executed by the *game*.
 - **player**<br/>
The *player* object is simply a reference to the entity that the player controls. It functions very similarly to other entities.
 - **self**<br/>
When you enter a UPL action, the action is defined within a certain object's trigger. We will explain that further in [Triggers](upl_triggers.html), but for now it is import that *self* is this object that contains the action. In case of an OpponentEntity for example, when you interact with the entity, the *on_interact* action begins, which means that *self* now refers to this OpponentEntity.
 - **target**<br/>
A UPL action is not necessarily player-exclusive. This means that other objects can also trigger the actions. *target* refers to the object that triggered the event. An entity (could be the player) walking onto a Region (see Mapping Tutorial) is then the *target* in the action defined in the Region's *on_enter* attribute.
 - **local**<br/>
Local is a storage that will **NOT** be saved when exiting the current map, or when the game is restarted. It is a temporary place to save attributes that you would want to access while the player is within a small range. This is mostly used for more advanced UPL.
 - **global**<br/>
Global is a storage that will **NOT** be saved when the game is restarted. It is a temporary place to save attributes that you would want to access while the player hasn't restarted their game. This is mostly used for more advanced UPL.
 - **col&map**<br/>
Col and Map are the collision- and map-manager respectively. They are used only in very specific situations, in case you want to replace tiles with others or change the collision of a tile.
 - **switch&set**<br/>
 While we have not mentioned these before, these are the global storages that **WILL** be saved after the game is closed. You can define them in Ldtk (see [Settables&Switches](upl_sets_switches.html)).
 You can access and set the defined switches and settables.

{% include links.html %}
