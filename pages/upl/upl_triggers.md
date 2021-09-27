---
title: Triggers
keywords: UPL Ulix Parsed Language Triggers
tags: [getting_started, upl]
sidebar: guide_sidebar
permalink: upl_triggers.html
folder: upl
summary: "How to make your UPL code happen in game!"
---

## Triggers

With a good basis on how to write some UPL actions, it would be nice if you could actually see them happen in game!
The way to make the code happen is based on **Triggers**. These triggers are things that can fire in predefined conditions.

{% include image.html file="triggers_oppo_entity.png" alt="triggers opponent" max-width=800 %}
{% include image.html file="triggers_region.png" alt="triggers region" max-width=800 %}

There are 5 mainly used triggers:
- **on_enter**: fires when an entity steps onto a certain Region. (Purple rectangle)
- **on_exit**: fires when an entity steps out of a certain Region. (Green rectangle)
- **on_interact**: fires when the player interacts with another entity. (Red rectangle)
- **on_create**: fires when the entity is created. This happens when the map the entity is in is loaded. (Yellow rectangle)
- **on_aggro**: *Specific to OpponentEntity at the moment*. fires when the player enters an entity's aggro range. (Light blue rectangle)

All of these triggers are defined within the entities and Regions you place in Ldtk. Some of these are prefabricated (prefab for short) when you place the entity, such as *\<\<\<opponent_on_aggro\>\>\>* (see [prefabs](upl_prefabs.html)). Be careful when changing these, because they are usually integral to the functionality of the entity. Note however, that you could also battle a Civilian entity if you would so desire. They do not have an aggro range or *on_aggro* trigger, but there is no problem with defining a battle within the civilian's *on_interact* trigger for example.

### *self*

As we've seen in [Users and Objects](upl_users_objects.html), you can refer to a *self* in UPL. This is always the object that contains the triggers that we just mentioned. Keep in mind that you can still refer to this *self* with their *entity_uid*, but this is less flexible.
```ruby
self: Say("Hello!")
```
Whereever we place this line of code, the user will **always** be the entity containing the trigger. It does not matter if we later decide to rename this entity, or if we place this same line in another entity. In the same way we can access the attributes of the *self* object:
```ruby
self: memory.defeated = True
```
Remember that because we do not mention the object that contains *memory*, it is seen as an attribute of the user. It is thus equivalent to:
```ruby
self: self.memory.defeated = True
```
This is an easy way to make opponents remember when they have been defeated, without having to create a specific line of UPL for each opponent you place. We use this in our OpponentEntity [prefab](upl_prefabs.html).

{% include links.html %}
