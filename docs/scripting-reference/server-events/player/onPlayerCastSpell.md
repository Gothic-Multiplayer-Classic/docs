---
title: 'onPlayerCastSpell'
---
# `event` onPlayerCastSpell <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when a player casts a spell.

## Parameters
```c++
void onPlayerCastSpell(number caster_id, number spell_id, number target_id)
```

* `number` **caster_id**: Caster player id.
* `number` **spell_id**: Spell identifier.
* `number` **target_id**: Optional target player id (nil if none).
