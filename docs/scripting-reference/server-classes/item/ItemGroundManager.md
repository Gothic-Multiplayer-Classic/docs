---
title: 'ItemGroundManager'
---
# `class` ItemGroundManager <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Provides server-side access to synchronized ground items.


## Properties
No properties.

----

## Methods
### getById

Returns a ground item by id.

```cpp
ItemGround|nil getById(number id)
```

**Parameters:**

* `number` **id**: Ground item id.
  
**Returns `ItemGround|nil`:**

Ground item object or nil if missing.

----
### create

Creates a synchronized ground item.

```cpp
number create({...} options, string options.instance, number options.amount, boolean options.physicsEnabled, {x, y, z} options.position, {x, y, z} options.rotation, string options.world, number options.virtualWorld)
```

**Parameters:**

* `{...}` **options**: Creation options.
* `string` **options.instance**: Gothic item instance name.
* `number` **options.amount**: Optional amount. Defaults to 1.
* `boolean` **options.physicsEnabled**: Optional physics flag. Defaults to false.
* `{x, y, z}` **options.position**: Optional world position. Defaults to 0,0,0.
* `{x, y, z}` **options.rotation**: Optional Euler rotation. Defaults to 0,0,0.
* `string` **options.world**: Optional world name. Defaults to the server world.
* `number` **options.virtualWorld**: Optional virtual world id. Defaults to 0.
  
**Returns `number`:**

Ground item id, or 0 on failure.

----
### destroy

Destroys a synchronized ground item.

```cpp
boolean destroy(number|ItemGround itemGround)
```

**Parameters:**

* `number|ItemGround` **itemGround**: Ground item id or object.
  
**Returns `boolean`:**

True if the ground item was destroyed.

----

## Callbacks
No callbacks.

----
