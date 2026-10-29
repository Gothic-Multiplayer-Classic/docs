---
title: 'createNpc'
---
# `function` createNpc <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    By default, the NPC won't be added to the world. It's necessary to call [spawnPlayer](../player/spawnPlayer.md) afterwards.

Creates an unspawned, server-owned NPC.

## Declaration
```cpp
number|nil, table|nil createNpc(string name, string|nil instance)
```

## Parameters
* `string` **name**: NPC name.
* `string|nil` **instance**: Gothic NPC instance; defaults to PC_HERO.
  
## Returns `number|nil, table|nil`
NPC id and nil on success; nil and {message = string} on failure.
