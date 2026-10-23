---
title: 'getPlayerVisual'
---
# `function` getPlayerVisual <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player/NPC current visual model and textures, or nil if unavailable.

## Declaration
```cpp
{bodyModel, bodyTexture, headModel, headTexture, teethTexture, skinColor}|nil getPlayerVisual(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
  
## Returns `{bodyModel, bodyTexture, headModel, headTexture, teethTexture, skinColor}|nil`
Player visual or nil.
