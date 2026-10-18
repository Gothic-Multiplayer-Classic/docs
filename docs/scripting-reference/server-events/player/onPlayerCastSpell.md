---
title: 'onPlayerCastSpell'
---
# `event` onPlayerCastSpell <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    This event can be cancelled.

This event is triggered when the player/npc attempts to cast a spell.

## Parameters
```c++
void onPlayerCastSpell(number caster_id, number spell_id, number|nil target_id)
```

* `number` **caster_id**: Caster player or server NPC id.
* `number` **spell_id**: Spell identifier.
* `number|nil` **target_id**: Optional target player or server NPC id (nil if none).
