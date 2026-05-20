---
title: 'onPlayerTakeItem'
---
# `event` onPlayerTakeItem <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player picks up an item.

## Parameters
```c++
void onPlayerTakeItem(number player_id, ItemGround item_ground)
```

* `number` **player_id**: Player id who took the item.
* `ItemGround` **item_ground**: Ground item object.
