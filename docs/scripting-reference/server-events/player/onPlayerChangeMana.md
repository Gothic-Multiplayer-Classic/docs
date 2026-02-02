---
title: 'onPlayerChangeMana'
---
# `event` onPlayerChangeMana <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when player mana changes.

## Parameters
```c++
void onPlayerChangeMana(number player_id, number previous, number current)
```

* `number` **player_id**: The id of the player whose mana points got changed.
* `number` **previous**: The previous mana points of the player.
* `number` **current**: The current mana points of the player.
