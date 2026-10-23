---
title: 'getPlayerOverlays'
---
# `function` getPlayerOverlays <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player/NPC active animation overlays, or nil if unavailable.

## Declaration
```cpp
{...}|nil getPlayerOverlays(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
  
## Returns `{...}|nil`
Array of overlay names or nil.
