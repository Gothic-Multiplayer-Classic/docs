---
title: 'onTakeItem'
---
# `event` onTakeItem <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when the hero takes an item from the ground.

## Parameters
```c++
void onTakeItem(string item, boolean synchronized, number amount, number|nil itemGroundId)
```

* `string` **item**: Item instance.
* `boolean` **synchronized**: True when pickup is synchronized with the server.
* `number` **amount**: Item amount.
* `number|nil` **itemGroundId**: Ground item id, or nil for non-server items.
