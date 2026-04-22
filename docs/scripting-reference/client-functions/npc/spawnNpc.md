---
title: 'spawnNpc'
---
# `function` spawnNpc <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will spawn a previously created NPC into the world.

## Declaration
```cpp
boolean spawnNpc(number npc_id, string|nil instance_name)
```

## Parameters
* `number` **npc_id**: NPC id.
* `string|nil` **instance_name**: Optional instance name (defaults to "PC_HERO").
  
## Returns `boolean`
True if spawn attached to world.
