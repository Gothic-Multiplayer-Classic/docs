---
title: 'isNpc'
---
# `function` isNpc <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Checks whether an id identifies an existing server-owned NPC.

## Declaration
```cpp
boolean isNpc(number npc_id)
```

## Parameters
* `number` **npc_id**: Character id.
  
## Returns `boolean`
True for an existing server NPC, including unspawned NPCs.
