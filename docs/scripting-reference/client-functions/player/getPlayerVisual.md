---
title: 'getPlayerVisual'
---
# `function` getPlayerVisual <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player/npc current visual model and textures, or nil if unavailable.

## Declaration
```cpp
{body_model, body_texture, head_model, head_texture}|nil getPlayerVisual(number player_id)
```

## Parameters
* `number` **player_id**: Target player id.
  
## Returns `{body_model, body_texture, head_model, head_texture}|nil`
Player visual or nil.
