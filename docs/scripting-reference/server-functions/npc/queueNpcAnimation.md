---
title: 'queueNpcAnimation'
---
# `function` queueNpcAnimation <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Queues a finite animation. Completion is reported by [onNpcActionFinished](../../server-events/npc/onNpcActionFinished.md).

## Declaration
```cpp
number|nil, table|nil queueNpcAnimation(number npc_id, string animation, number|nil timeout_ms)
```

## Parameters
* `number` **npc_id**: Server NPC id.
* `string` **animation**: Gothic animation name.
* `number|nil` **timeout_ms**: Execution timeout, 1-30000 ms; defaults to 10000.
  
## Returns `number|nil, table|nil`
Action id and nil on success; nil and {message = string} when rejected.
