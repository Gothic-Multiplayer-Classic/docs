---
title: 'setNpcHostPlayer'
---
# `function` setNpcHostPlayer <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Assigns an eligible streaming player as host, or releases the host for automatic selection.

## Declaration
```cpp
boolean setNpcHostPlayer(number npc_id, number host_id)
```

## Parameters
* `number` **npc_id**: Server NPC id.
* `number` **host_id**: Eligible player id; -1 releases the current host.
  
## Returns `boolean`
True if the assignment was accepted.
