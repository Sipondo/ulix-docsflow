---
title: Prefabs
keywords: UPL Ulix Parsed Language Prefabs Prefabrication
tags: [getting_started, upl]
sidebar: guide_sidebar
permalink: upl_prefabs.html
folder: upl
summary: "How to smartly use more complicated UPL."
---

## OpponentEntity example

```ruby
?if(self.memory.defeated){
    exit
}
game: Cinematic()
!self: Say(spot_text)
?self: Move(player.x, player.y)
self: Say(encounter_text)
self: Battle()
game: Cinematic()
self: Say(defeat_text)
self: memory.defeated = True
game: Overworld()
```

The above example shows the UPL action that is */</</<opponent_on_aggro/>/>/>*. This is the action that is automatically generated when you place an OpponentEntity object.
Since this is an action you would want to happen on a lot of different entities, it is saved separately.

## Save location

In order for the game to find these UPL files, they need to be saved in a specific location: **YOUR/GAME/FOLDER***/resources/***YOUR_RESOURCES_NAME***/upl/filename.upl*. The above example can be found in **YOUR/GAME/FOLDER***/resources/base/upl/opponent_on_aggro.upl*. Feel free to add as many of these files as you want (make sure they have the *.upl* extension!).

## More advanced

If you want an example of how to use UPL to get more advanced behaviour, we recommend taking a look at the *lightpuzzle/light_update.upl* file.

```ruby
game: FlushTiles(4)
self: lightsources = GetEntities("lightsource")
self: lightbounces = GetEntities("lightbounce")
self: j = 0
self: b = 0

?while(self.j < Length(self.lightsources)){
  self: current_lightsource = lightsources[j]
  self: light_direction = current_lightsource.light_direction
  self: light_x = current_lightsource.x
  self: light_y = current_lightsource.y
  self: i = 0

  while(self.i <= 50){
    self: b = 0

    self: oldtile = GetTile(4, light_x, light_y)
    if(self.light_direction[0]==0){
        self: tile = (1,0)
        if((self.oldtile[0] == 2)){
            self: tile = (3,0)
        }
        if((self.oldtile[0] == 3)){
            self: tile = (3,0)
        }
    }
    if(self.light_direction[1]==0){
        self: tile = (2, 0)
        if((self.oldtile[0] == 1)){
            self: tile = (3,0)
        }
        if((self.oldtile[0] == 3)){
            self: tile = (3,0)
        }
    }

    while(self.b < Length(self.lightbounces)){
        self: current_lightbounce = lightbounces[b]
        if(self.current_lightbounce.pos == (self.light_x, self.light_y)){
            if(self.current_lightbounce.light_dir_a == (-1*self.light_direction[0], -1*self.light_direction[1])){
                self: light_direction = current_lightbounce.light_dir_b
                self: tile = current_lightbounce.light_tile
            }else{
                if(self.current_lightbounce.light_dir_b == (-1*self.light_direction[0], -1*self.light_direction[1])){
                    self: light_direction = current_lightbounce.light_dir_a
                    self: tile = current_lightbounce.light_tile
                }
            }
        }
        self: b = b + 1
    }

    self: SetTile(4, light_x, light_y, tile)

    self: light_x = light_x + light_direction[0]
    self: light_y = light_y + light_direction[1]

    self: i = i + 1
    if(CheckCollision(self.light_x, self.light_y, 0)){
      self: i = 100
    }
  }

  if(self.light_direction == (-1,0)){
      self: SetTile(4, light_x, light_y, (0, 2))
  }
  if(self.light_direction == (0,-1)){
      self: SetTile(4, light_x, light_y, (1, 2))
  }
  if(self.light_direction == (1,0)){
      self: SetTile(4, light_x, light_y, (2, 2))
  }
  if(self.light_direction == (0,1)){
      self: SetTile(4, light_x, light_y, (3, 2))
  }

  self: j = j + 1
}
?game: UpdateTiles(4)
```

We won't be explaining how this code works here. The result of this code is seen in the basement of the little house in our example world!

{% include links.html %}
