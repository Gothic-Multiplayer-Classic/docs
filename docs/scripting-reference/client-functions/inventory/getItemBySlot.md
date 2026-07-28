---
title: 'getItemBySlot'
---
# `function` getItemBySlot <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the item instance from the local player's inventory slot.

## Declaration
```cpp
string|nil getItemBySlot(number slot)
```

## Parameters
* `number` **slot**: Inventory slot, starting from 0.
  
## Returns `string|nil`
Item instance, or nil if the slot is empty.
