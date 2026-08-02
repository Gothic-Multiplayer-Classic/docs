---
title: 'Vob'
---
# `class` Vob <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This class represents a 3d object in the world.

### Constructor
```cpp
Vob.new(string model)
```

**Parameters:**

* `string` **model**: Visual model name (e.g. "SPHERE.3DS").

## Properties
### `string` objectName 

Represents the internal engine object name of the Vob.

----
### `Mat4` matrix 

Represents the reference to the Vob matrix.

----
### `Vob|nil` parent 
!!! note
    The Vob hierarchy will be lost after changing the world.

Represents the reference to the parent Vob.

----
### `boolean` cdDynamic 

Represents the state of dynamic collision of the Vob. Enabling this option will prevent other dynamic objects from passing through it.

----
### `boolean` cdStatic 

Represents the state of static collision of the Vob. Enabling this option will prevent static objects (i.e. world mesh) from passing through it.

----
### `number` farClipZScale 

Represents the max distance at which the Vob will still be rendered.

----
### `string` visual 

Represents the model file name used as Vob visual, e.g. "SPHERE.3DS".

----
### `number` visualAlpha 

Represents the transparency of the Vob visual.

----

## Methods
### setPosition

This method will set the position of the Vob in the world.

```cpp
void setPosition(number x, number y, number z)
```

**Parameters:**

* `number` **x**: Position on X axis.
* `number` **y**: Position on Y axis.
* `number` **z**: Position on Z axis.
  

----
### getPosition

This method will return the position of the Vob in the world.

```cpp
{x, y, z} getPosition()
```

  
**Returns `{x, y, z}`:**

Table containing x,y,z position.

----
### setRotation

This method will set the euler rotation of the Vob in the world, in degrees.

```cpp
void setRotation(number x, number y, number z)
```

**Parameters:**

* `number` **x**: Rotation on X axis in degrees.
* `number` **y**: Rotation on Y axis in degrees.
* `number` **z**: Rotation on Z axis in degrees.
  

----
### getRotation

This method will return the euler rotation of the vob in the world, in degrees.

```cpp
{x, y, z} getRotation()
```

  
**Returns `{x, y, z}`:**

Table containing x,y,z rotation.

----
### addToWorld

This method will add the vob to the currently loaded world. If the vob is not added, it won't show up.

```cpp
void addToWorld(Vob|nil parent)
```

**Parameters:**

* `Vob|nil` **parent**: Optional parent vob to attach to.
  

----
### removeFromWorld

This method will remove the vob from the currently loaded world.

```cpp
void removeFromWorld()
```

  

----
### floor

This method will try to put the vob on the floor. If the difference between vob position and the floor y position is <= 1000, the method succeeds.

```cpp
void floor()
```

  

----

## Callbacks
No callbacks.

----
