---
title: 'createNpc'
---
# `function` createNpc <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    By default, the NPC won't be added to the world. It's necessary to call [`spawnNpc`](./spawnNpc.md) afterwards.

This function will create a client-side NPC entry and return an internal npc id (<0).

## Declaration
```cpp
number createNpc(string name)
```

## Parameters
* `string` **name**: Name for the created NPC.
  
## Returns `number`
NPC id (starting from -1) or 0 on failure.
