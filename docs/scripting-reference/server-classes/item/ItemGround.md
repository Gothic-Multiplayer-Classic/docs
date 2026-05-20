---
title: 'ItemGround'
---
# `class` ItemGround <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Represents a synchronized item placed in the world.


## Properties
### `number` id 

Represents the unique ground item id.

----
### `string` instance 

Represents the Gothic item instance name.

----
### `number` amount 

Represents the item amount.

----
### `boolean` physicsEnabled 

Enables or disables client-side physics for this ground item.

----
### `string` world 

Represents the world name where this ground item exists.

----
### `number` virtualWorld 

Represents the virtual world id where this ground item exists.

----

## Methods
### getPosition

Returns the ground item world position.

```cpp
{x, y, z} getPosition()
```

  
**Returns `{x, y, z}`:**

Position table.

----
### setPosition

Sets the ground item world position and synchronizes it to relevant players.

```cpp
void setPosition(number x, number y, number z)
```

**Parameters:**

* `number` **x**: X coordinate.
* `number` **y**: Y coordinate.
* `number` **z**: Z coordinate.
  

----
### getRotation

Returns the ground item Euler rotation.

```cpp
{x, y, z} getRotation()
```

  
**Returns `{x, y, z}`:**

Rotation table.

----
### setRotation

Sets the ground item Euler rotation and synchronizes it to relevant players.

```cpp
void setRotation(number x, number y, number z)
```

**Parameters:**

* `number` **x**: X rotation.
* `number` **y**: Y rotation.
* `number` **z**: Z rotation.
  

----

## Callbacks
No callbacks.

----
