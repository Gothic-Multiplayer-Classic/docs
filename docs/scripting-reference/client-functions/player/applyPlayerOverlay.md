---
title: 'applyPlayerOverlay'
---
# `function` applyPlayerOverlay <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will apply an animation overlay on player (eg. "HUMANS_MILITIA.MDS").

## Declaration
```cpp
boolean applyPlayerOverlay(number player_id, string overlay)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
* `string` **overlay**: The name of overlay.
  
## Returns `boolean`
True on success.
