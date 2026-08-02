---
title: 'Camera'
---
# `class` Camera <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

Static access to the active engine camera.


## Properties
### `boolean` modeChangeEnabled 

Represents whether scripted camera mode changes are enabled.

----
### `boolean` movementEnabled 

Represents whether the camera is allowed to move.
Setting this to true restores engine camera AI after manual position or rotation changes.

----
### `Vob|nil` targetVob 

Represents the active camera target Vob.

----

## Methods
### setMode

Sets the active camera mode.

```cpp
boolean setMode(string mode)
```

**Parameters:**

* `string` **mode**: Camera mode name.
  
**Returns `boolean`:**

True if an AI camera is available.

----
### getMode

Returns the active camera mode.

```cpp
string getMode()
```

  
**Returns `string`:**

Camera mode name.

----
### setPosition

Sets the active camera world position.
This puts the camera into manual movement mode until movementEnabled is set to true.

```cpp
void setPosition(number x, number y, number z)
```

**Parameters:**

* `number` **x**: X world position.
* `number` **y**: Y world position.
* `number` **z**: Z world position.
  

----
### getPosition

Returns the active camera world position.

```cpp
{x, y, z} getPosition()
```

  
**Returns `{x, y, z}`:**

Table containing x,y,z world position.

----
### setRotation

Sets the active camera Euler rotation in degrees.
This puts the camera into manual movement mode until movementEnabled is set to true.

```cpp
void setRotation(number x, number y, number z)
```

**Parameters:**

* `number` **x**: X rotation in degrees.
* `number` **y**: Y rotation in degrees.
* `number` **z**: Z rotation in degrees.
  

----
### getRotation

Returns the active camera Euler rotation in degrees.

```cpp
{x, y, z} getRotation()
```

  
**Returns `{x, y, z}`:**

Table containing x,y,z rotation.

----
### setTargetVob

Sets a Vob as the active camera target.

```cpp
boolean setTargetVob(Vob vob)
```

**Parameters:**

* `Vob` **vob**: Target Vob.
  
**Returns `boolean`:**

True if the target was applied.

----
### setTargetPlayer

Sets a player or NPC as the active camera target.

```cpp
boolean setTargetPlayer(number playerId)
```

**Parameters:**

* `number` **playerId**: Player id.
  
**Returns `boolean`:**

True if the player or NPC exists.

----
### setFOV

Sets the active render camera field of view.

```cpp
void setFOV(number fov)
```

**Parameters:**

* `number` **fov**: Field of view.
  

----
### getFOV

Returns the active render camera field of view.

```cpp
number getFOV()
```

  
**Returns `number`:**

Field of view.

----

## Callbacks
No callbacks.

----
