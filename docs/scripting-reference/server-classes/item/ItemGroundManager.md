---
title: 'ItemGroundManager'
---
# `static class` ItemGroundManager <font size="4">(server-side)</font>

Static lookup and creation API for synchronized ground items.


## Properties
No properties.

----

## Methods
### `static` getById
!!! info "Available since version: 0.3.0"

Returns a ground item by id.

```cpp
ItemGround|nil getById(number id)
```

**Parameters:**

* `number` **id**: Ground item id.
  
**Returns `ItemGround|nil`:**

Ground item object or nil if missing.

----
### `static` destroy
!!! info "Available since version: 0.3.0"

Destroys a synchronized ground item.

```cpp
boolean destroy(number|ItemGround itemGround)
```

**Parameters:**

* `number|ItemGround` **itemGround**: Ground item id or object.
  
**Returns `boolean`:**

True if the ground item was destroyed.

----
### `static` create

Creates a synchronized ground item.

```cpp
number|nil, table|nil create(table options)
```

**Parameters:**

* `table` **options**: instance, amount, physicsEnabled, position, rotationDegrees, world and virtualWorld.
  
**Returns `number|nil, table|nil`:**

Ground item id and nil on success; nil and {message = string} on failure.

----

## Callbacks
No callbacks.

----
