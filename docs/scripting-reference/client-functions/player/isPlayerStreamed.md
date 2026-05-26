---
title: 'isPlayerStreamed'
---
# `function` isPlayerStreamed <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will check whether a player or client NPC is spawned into the world.

## Declaration
```cpp
boolean|nil isPlayerStreamed(number player_id)
```

## Parameters
* `number` **player_id**: Target player or client NPC id.
  
## Returns `boolean|nil`
True when spawned, false when known but not spawned, nil if unknown.
