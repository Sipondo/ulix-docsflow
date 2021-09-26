---
title: Introduction to UPL
keywords: UPL Ulix Parsed Language Scripting Actions
tags: [getting_started, upl]
sidebar: guide_sidebar
permalink: upl_introduction.html
folder: upl
summary: "Introduces the actions language of Ulix Dexflow: UPL"
---

## Ulix Parsed Language

Ulix Parsed Language (UPL) is the way of defining actions in Ulix Dexflow. The language was designed to be as simple as possible,
making it easy to read, write and use. This guide will introduce you to everything from how to say "Hello!" to creating entire 
sequences of actions depending on player choices throughout the game!

## Say("Hello!")

The following code would start a cinematic, make your character say "Hello!", and then giving control back to the player upon trigger (we will get to triggers later).

```ruby
game: Cinematic()
player: Say("Hello!")
game: Overworld()
```

In the [UPL Syntax](upl_syntax.html) we will break down this piece of code into its basic parts, explaining what each part does along the way.


{% include links.html %}
