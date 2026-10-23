---
title: 'getPlayerWorld'
---
# `function` getPlayerWorld <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

Returns the online player's world, independently of native streaming.

## Declaration
```cpp
string|nil getPlayerWorld(number player_id)
```

## Parameters
* `number` **player_id**: Target player id; NPC ids are not supported.
  
## Returns `string|nil`
World filename or nil.
