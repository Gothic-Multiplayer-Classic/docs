---
title: 'ItemGroundManager'
---
# `class` ItemGroundManager <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

Provides client-side lookup for synchronized ground items visible in the current world.


## Properties
No properties.

----

## Methods
### getById

Returns a synchronized ground item by id.

```cpp
ItemGround|nil getById(number id)
```

**Parameters:**

* `number` **id**: Ground item id.
  
**Returns `ItemGround|nil`:**

Ground item object or nil if missing.

----
### getByItem

Returns the first synchronized ground item with the given item instance.

```cpp
ItemGround|nil getByItem(string instance)
```

**Parameters:**

* `string` **instance**: Gothic item instance name.
  
**Returns `ItemGround|nil`:**

Ground item object or nil if missing.

----

## Callbacks
No callbacks.

----
