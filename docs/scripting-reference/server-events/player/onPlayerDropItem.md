---
title: 'onPlayerDropItem'
---
# `event` onPlayerDropItem <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player drops an item.

## Parameters
```c++
void onPlayerDropItem(number player_id, ItemGround item_ground)
```

* `number` **player_id**: Player id who dropped the item.
* `ItemGround` **item_ground**: Ground item object.
