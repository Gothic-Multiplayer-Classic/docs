---
title: 'onPlayerSummon'
---
# `event` onPlayerSummon <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    The summoned NPC exists when this event is triggered. This event is not triggered when an existing summon streams in.

This event is triggered when a player summons an NPC using a game's spell.

## Parameters
```c++
void onPlayerSummon(number playerId, number spellId, string summonInstance, number npcId)
```

* `number` **playerId**: The id of the player who summoned the NPC.
* `number` **spellId**: The id of the spell used to summon the NPC.
* `string` **summonInstance**: The instance name of the summoned NPC.
* `number` **npcId**: The id of the summoned NPC.
