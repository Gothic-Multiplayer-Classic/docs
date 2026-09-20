---
title: 'setNpcAnimation'
---
# `function` setNpcAnimation <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Sets an NPC's persistent animation, including looping animations. All current
and future viewers receive this state. Finite queued actions take precedence.

## Declaration
```cpp
boolean setNpcAnimation(number npc_id, string animation)
```

## Parameters
* `number` **npc_id**: Server NPC id.
* `string` **animation**: Gothic animation name; an empty string clears it.
  
## Returns `boolean`
True if the state was accepted; does not validate client assets.
