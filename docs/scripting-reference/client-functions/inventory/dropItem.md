---
title: 'dropItem'
---
# `function` dropItem <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will drop an item from the local player's inventory.

## Declaration
```cpp
boolean dropItem(string instance, number|nil amount)
```

## Parameters
* `string` **instance**: Item instance name.
* `number|nil` **amount**: Optional amount to drop. Defaults to the whole stack.
  
## Returns `boolean`
True on success.
