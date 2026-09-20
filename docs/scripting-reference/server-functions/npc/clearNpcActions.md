---
title: 'clearNpcActions'
---
# `function` clearNpcActions <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Cancels the current action and all pending actions.

## Declaration
```cpp
boolean clearNpcActions(number npc_id)
```

## Parameters
* `number` **npc_id**: Server NPC id.
  
## Returns `boolean`
True if cleared, including an empty queue; false for an invalid NPC or failed operation.
