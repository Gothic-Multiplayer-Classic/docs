---
title: 'createNpc'
---
# `function` createNpc <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Creates an unspawned, server-owned NPC. Use spawnPlayer to stream it to clients.

## Declaration
```cpp
number createNpc(string name, string|nil instance)
```

## Parameters
* `string` **name**: Character name.
* `string|nil` **instance**: Gothic NPC instance; defaults to PC_HERO.
  
## Returns `number`
NPC id, or -1 on failure.
