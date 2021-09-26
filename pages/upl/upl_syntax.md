---
title: UPL Syntax
keywords: UPL Ulix Parsed Language Syntax
tags: [getting_started, upl]
sidebar: guide_sidebar
permalink: upl_syntax.html
folder: upl
summary: "Introduces the syntax of UPL"
---

## Say("Hello!") in 4 parts

```Ruby
game: Cinematic()
player: Say("Hello!")
game: Overworld()
```

As we saw in the introduction, this script will make your character say "Hello!" when triggered. More about how to trigger this script later!
This script can be broken down into 4 parts:
 - **Script user**
 - **Function**
 - **Arguments**
 - **Cinematic & Overworld**

## Script user
Every UPL script requires you to define a user. This can be many things, we will go over all of them in [Script users](upl_script_users.html).
In the script the user is defined in the part before (and including) the colon (:). This is the object that will execute the code.
```Ruby
game:
player:
game:
```
By making the "player" object the user, we make the player execute the function for us. In this case, the player will say "Hello!".

## Function
UPL works using functions. These functions are the hidden mechanics that do things such as saying text, starting a battle or opening a shop.
In the script the function is defined directly after the colon. The UPL Documentation tab contains all the existing functions currently in UPL.
```Ruby
Cinematic()
Say()
Overworld()
```
Each of these functions must be called using the parentheses. Do note that we left out the "Hello!" from Say(). In the next section we will explain more.

## Arguments
Some functions in UPL take (optional) arguments. These arguments specify further what the function should be doing.
```Ruby
"Hello!"
```
In the example, "Hello!" was the argument given to the Say() function. This is the text that is shown on screen when Say() is called, and is a *required* argument for the Say() function. For an overview of required and optional arguments for a function, go the the UPL Documentation.

## Cinematic & Overworld
```Ruby
game: Cinematic()
game: Overworld()
```
We've already seen that these are functions executed by the "game" as a user. Cinematic and Overworld are special, because they are what allow you to pause the game and play a cinematic, whether it's just a bit of dialogue or an entire sequence of actions, such as forced walking. Cinematic is the function that starts such a sequence, which will unfold itself with the player having little to no control. Overworld is the function that ends the sequence, thus giving control back to the player.

