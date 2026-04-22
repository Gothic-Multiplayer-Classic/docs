---
title: 'Quat'
---
# `class` Quat <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

This class represents a Quaternion.

Provides conversion to/from matrices, Euler angles and axis-angle, as well as
common quaternion operations and interpolation utilities.

### Constructor
```cpp
Quat.new()
```

**Parameters:**

No parameters.
### Constructor
```cpp
Quat.new(number w)
```

**Parameters:**

* `number` **w**: W component.
### Constructor
```cpp
Quat.new(number x, number y, number z, number w)
```

**Parameters:**

* `number` **x**: X component.
* `number` **y**: Y component.
* `number` **z**: Z component.
* `number` **w**: W component.

## Properties
### `number` x 

Represents X component.

----
### `number` y 

Represents Y component.

----
### `number` z 

Represents Z component.

----
### `number` w 

Represents W component.

----

## Methods
### toMat3

This method converts this quaternion to a 3x3 rotation matrix.

```cpp
Mat3 toMat3()
```

  
**Returns `Mat3`:**

Rotation matrix.

----
### fromMat3

This method sets this quaternion from a 3x3 rotation matrix.

```cpp
void fromMat3(Mat3 mat)
```

**Parameters:**

* `Mat3` **mat**: Rotation matrix.
  

----
### toMat4

This method converts this quaternion to a 4x4 rotation matrix.

```cpp
Mat4 toMat4()
```

  
**Returns `Mat4`:**

Rotation matrix.

----
### fromMat4

This method sets this quaternion from a 4x4 transform matrix (rotation part).

```cpp
void fromMat4(Mat4 mat)
```

**Parameters:**

* `Mat4` **mat**: Transform matrix.
  

----
### toEuler

This method converts this quaternion to Euler angles.

```cpp
Vec3 toEuler()
```

  
**Returns `Vec3`:**

Euler angles as a 3D vector.

----
### fromEuler

This method sets this quaternion from Euler angles.

```cpp
void fromEuler(Vec3 vec)
```

**Parameters:**

* `Vec3` **vec**: Euler angles as a 3D vector.
  

----
### toAxisAngle

This method converts this quaternion to axis-angle representation.
The returned Vec4 contains (axis.x, axis.y, axis.z, angle).

```cpp
Vec4 toAxisAngle()
```

  
**Returns `Vec4`:**

Axis-angle as (x, y, z, angle).

----
### fromAxisAngle

This method sets this quaternion from an axis and angle.

```cpp
void fromAxisAngle(Vec3 axis, number angle)
```

**Parameters:**

* `Vec3` **axis**: Rotation axis (typically normalized).
* `number` **angle**: Rotation angle.
  

----
### makeIdentity

This method sets this quaternion to identity (no rotation).

```cpp
void makeIdentity()
```

  

----
### isIdentity

This method returns true if this quaternion is identity (within epsilon tolerance).

```cpp
boolean isIdentity()
```

  
**Returns `boolean`:**

True if identity.

----
### len

This method returns the quaternion length.

```cpp
number len()
```

  
**Returns `number`:**

Quaternion length.

----
### len2

This method returns the squared quaternion length.

```cpp
number len2()
```

  
**Returns `number`:**

Squared quaternion length.

----
### lenApprox

This method returns an approximate quaternion length.

```cpp
number lenApprox()
```

  
**Returns `number`:**

Approximate length.

----
### normalize

This method normalizes the quaternion in-place.
If the quaternion length is zero, no change is applied.

```cpp
Quat normalize()
```

  
**Returns `Quat`:**

This quaternion (normalized).

----
### normalizeSafe

This method normalizes the quaternion in-place using an epsilon check.
If the quaternion length is below a small threshold, no change is applied.

```cpp
Quat normalizeSafe()
```

  
**Returns `Quat`:**

This quaternion (normalized).

----
### normalizeApprox

This method normalizes the quaternion in-place using an approximate inverse square root.

```cpp
Quat normalizeApprox()
```

  
**Returns `Quat`:**

This quaternion (normalized).

----
### set

This method sets quaternion components.

```cpp
void set(number x, number y, number z, number w)
```

**Parameters:**

* `number` **x**: X component.
* `number` **y**: Y component.
* `number` **z**: Z component.
* `number` **w**: W component.
  

----
### inverse

This method returns the inverse quaternion.
For unit quaternions, this is equivalent to conjugate().

```cpp
Quat inverse()
```

  
**Returns `Quat`:**

Inverse quaternion.

----
### conjugate

This method returns the conjugate quaternion.

```cpp
Quat conjugate()
```

  
**Returns `Quat`:**

Conjugated quaternion.

----
### `static` dot

This method returns the dot product of two quaternions.

```cpp
number dot(Quat quat1, Quat quat2)
```

**Parameters:**

* `Quat` **quat1**: First quaternion.
* `Quat` **quat2**: Second quaternion.
  
**Returns `number`:**

Dot product.

----
### `static` lerp

This method linearly interpolates between two quaternions.

```cpp
Quat lerp(number t, Quat q1, Quat q2)
```

**Parameters:**

* `number` **t**: Interpolation factor (typically 0..1).
* `Quat` **q1**: Start quaternion.
* `Quat` **q2**: End quaternion.
  
**Returns `Quat`:**

Interpolated quaternion.

----
### `static` slerp

This method spherically interpolates between two quaternions.

```cpp
Quat slerp(number t, Quat q1, Quat q2)
```

**Parameters:**

* `number` **t**: Interpolation factor (typically 0..1).
* `Quat` **q1**: Start quaternion.
* `Quat` **q2**: End quaternion.
  
**Returns `Quat`:**

Spherically interpolated quaternion.

----
### `static` squad

This method performs a squad-style interpolation using three quaternions.

```cpp
Quat squad(number t, Quat q1, Quat q2, Quat q3)
```

**Parameters:**

* `number` **t**: Interpolation factor (typically 0..1).
* `Quat` **q1**: First quaternion.
* `Quat` **q2**: Second quaternion.
* `Quat` **q3**: Third quaternion.
  
**Returns `Quat`:**

Interpolated quaternion.

----
### `static` lookRotation

This method creates a quaternion that looks in the given forward direction with the given up direction.

```cpp
Quat lookRotation(Vec3 forward, Vec3 up)
```

**Parameters:**

* `Vec3` **forward**: Forward direction.
* `Vec3` **up**: Up direction.
  
**Returns `Quat`:**

Resulting rotation quaternion.

----

## Callbacks
No callbacks.

----
