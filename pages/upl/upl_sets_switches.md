---
title: Prefabs
keywords: UPL Ulix Parsed Language Set Switch Settables Switches
tags: [getting_started, upl]
sidebar: guide_sidebar
permalink: upl_sets_switches.html
folder: upl
summary: "How to save global variables with UPL."
---

## Settables & Switches

Settables and switches are the way to save your global data in your save file. They are defined in the Enums tab (F5) in Ldtk. <br/>
{% include image.html file="settables.png" alt="settables" max-width=800 %}
{% include image.html file="switches.png" alt="switches" max-width=800 %}

## Settables

Settables are variables that you can store *anything* in. In the example above, we have defined a *story_chapter* settable, which we can now access in UPL. It is an attribute of the *set* object (see [Users & Objects](upl_users_objects.html)). This means we can now access it to see how far the player has progressed or set it in UPL when the player progresses through the game!

```ruby
set: story_chapter = 3
```
```ruby
if(story_chapter > 2){
	exit
}
```

It can also contain other types of variables like names, percentages and whatever else could be useful saving. Keep in mind that you need to define them in the Ldtk Enums tab first!

```ruby
set: rival_name = Prompt("What is the name of your rival?")
```

## Switches

Switches are similar to settables, but they can only be on or off, or rather: *True* or *False*. They can be very useful when checking whether a certain character has been talked to, a puzzle has been completed or similar events. Technically you could use settables for anything you do with switches, but sometimes settables might be more difficult to keep track of. Switches have the advantage that they are **ONLY** *True* or *False*. This also means that we can do a little shorthand writing in our conditional actions (see [conditional actions](upl_syntax.html#conditional-actions)):
```ruby
if(switch.obtained_coat){
	exit
}
```
Notice that we do not use '==' to compare its value to *True*. Because it is either *True* or *False* we can simply leave out the part we compare it to these values.

{% include links.html %}
