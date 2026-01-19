---
title: 'onPlayerChangeMana'
---
# `event` onPlayerChangeMana <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when player mana changes.

## Parameters
```c++
void onPlayerChangeMana(int player_id, int previous, int current)
```

* `int` **player_id**: The id of the player whose mana points got changed.
* `int` **previous**: The previous mana points of the player.
* `int` **current**: The current mana points of the player.
