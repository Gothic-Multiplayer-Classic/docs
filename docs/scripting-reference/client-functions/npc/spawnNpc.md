---
title: 'spawnNpc'
---
# `function` spawnNpc <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

Spawn a previously created NPC into the world using an optional instance.

## Declaration
```cpp
boolean spawnNpc(number npc_id, string|nil instance_name)
```

## Parameters
* `number` **npc_id**: Internal npc id.
* `string|nil` **instance_name**: Optional instance name (e.g., "PC_HERO").
  
## Returns `boolean`
True if spawn attached to world.
