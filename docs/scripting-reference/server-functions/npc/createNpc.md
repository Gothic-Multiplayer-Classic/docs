---
title: 'createNpc'
---
# `function` createNpc <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Creates an unspawned, server-owned NPC. Use [spawnPlayer](../player/spawnPlayer.md) to stream it to clients.

## Declaration
```cpp
number|nil, table|nil createNpc(string name, string|nil instance)
```

## Parameters
* `string` **name**: NPC name.
* `string|nil` **instance**: Gothic NPC instance; defaults to PC_HERO.
  
## Returns `number|nil, table|nil`
NPC id and nil on success; nil and {message = string} on failure.
