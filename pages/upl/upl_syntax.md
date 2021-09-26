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

```ruby
game: Cinematic()
player: Say("Hello!")
game: Overworld()
```

As we saw in the introduction, this action will make your character say "Hello!" when triggered. More about how to trigger this action later!
This action can be broken down into 4 parts:
 - **User**
 - **Function**
 - **Arguments**
 - **Cinematic & Overworld**

### User
Every UPL line requires you to define a user. This can be many things, we will go over types of users in [Users & Objects](upl_users_objects.html).
In the line the user is defined in the part before (and including) the colon (:). This is the object that will execute the code.
```ruby
game:
player:
game:
```
By making the "player" object the user, we make the player execute the function for us. In this case, the player will say "Hello!".

### Function
UPL works using functions. These functions are the hidden mechanics that do things such as saying text, starting a battle or opening a shop.
In the action the function is defined directly after the colon. The UPL Documentation tab contains all the existing functions currently in UPL.
```ruby
Cinematic()
Say()
Overworld()
```
Each of these functions must be called using the parentheses. Do note that we left out the "Hello!" from Say(). In the next section we will explain more.

### Arguments
Some functions in UPL take (optional) arguments. These arguments specify further what the function should be doing.
```ruby
"Hello!"
```
In the example, "Hello!" was the argument given to the Say() function. This is the text that is shown on screen when Say() is called, and is a *required* argument for the Say() function. For an overview of required and optional arguments for a function, go the the UPL Documentation.

### Cinematic & Overworld
```ruby
game: Cinematic()
game: Overworld()
```
We've already seen that these are functions executed by the *game* as a user. Cinematic and Overworld are special, because they are what allow you to pause the game and play a cinematic, whether it's just a bit of dialogue or an entire sequence of functions, including things like forced walking. Cinematic is the function that starts such a sequence, which will unfold itself with the player having little to no control. Overworld is the function that ends the sequence, thus giving control back to the player.

## Attributes

Sometimes you would want to know where an object is (For more info on objects, see [Users and Objects](upl_users_objects.html)). Or maybe you would want to set an entity as *defeated* after a battle. We've seen before that we define a *user* whenever we execute a line of UPL code.

```ruby
entity: Move(player.x + 1, player.y)
```
Notice that we use *.attribute_name* to access the current x- and y-coordinates of the player. This code will make the *entity* that is the user walk to a position 1 to the right of the player.
```ruby
entity: defeated = True
```
To set an attribute, we first name the attribute we want to assign a value to: *defeated*. To assign a value, use a single *=* followed by the value you want to assign. 
*True* and *False* are the simplest, simply saving whether something is true or false. You can also assign numbers and other things:
```ruby
set: story_chapter = 3
```
These can be very useful to progress through the game without repeating events!

## Conditional actions

Let's say the player has already had a battle with a certain entity. The next time we want to pass by this entity, we do not want to start another battle, so we need some way to stop the script before it executes again! In OpponentEntity, this is done by default, but we can manually check this as well:
```ruby
if(self.defeated == True){
    exit
}
# do other stuff
```
For now, ignore the *self*. We will talk more about that in Triggers and [Users and Objects](upl_users_objects.html). Notice that we are now using a double equals sign *==*. This is used for comparing values to see if they are equal. In this case, we check if the entity has an attribute that says it has already been defeated, and *exit* if that's the case. *exit* immediately ends the script. Make sure that you are not in a Cinematic when you use *exit* or the player will not be able to move!
The *{}* is for when you would want to execute multiple lines conditionally. Everything within the brackets will **ONLY** execute if the condition within the parentheses is met!

```ruby
if(set.story_chapter > 3){
    exit
}
```
You can also use comparison to check if something is greater than *>* or smaller than *<* a value. In this case, we check if we have progressed past this point in the story yet. If that's the case, we no longer need to do this action.

{% include links.html %}
