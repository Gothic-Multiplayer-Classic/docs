---
title: 'setPlayerNameColor'
---
# `function` setPlayerNameColor <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    Accepts player and server NPC ids; negative client-local NPC ids are not supported.

This function will change the player/NPC name color.

## Declaration
```cpp
boolean setPlayerNameColor(number player_id, number r, number g, number b)
```

## Parameters
* `number` **player_id**: Target player or server NPC id; client-local NPC ids are not supported.
* `number` **r**: The red color component in RGB model.
* `number` **g**: The green color component in RGB model.
* `number` **b**: The blue color component in RGB model.
  
## Returns `boolean`
True on success.
