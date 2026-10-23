---
title: 'getPlayerVisual'
---
# `function` getPlayerVisual <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player/NPC's visual information as a table, or nil if unavailable.

## Declaration
```cpp
{bodyModel, bodyTexture, headModel, headTexture, teethTexture, skinColor}|nil getPlayerVisual(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id.
  
## Returns `{bodyModel, bodyTexture, headModel, headTexture, teethTexture, skinColor}|nil`
Table with visual data or nil.
