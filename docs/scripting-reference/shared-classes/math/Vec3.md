---
title: 'Vec3'
---
# `class` Vec3 <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

3D vector with basic math utilities.

### Constructor
```cpp
Vec3.new(float value)
```

**Parameters:**

* `float` **value**: Value assigned to x, y and z.
### Constructor
```cpp
Vec3.new(float x, float y, float z)
```

**Parameters:**

* `float` **x**: X component.
* `float` **y**: Y component.
* `float` **z**: Z component.

## Properties
### `float` x 

X component.

----
### `float` y 

Y component.

----
### `float` z 

Z component.

----

## Methods
### len

Returns the vector length (magnitude).

```cpp
float len()
```

  
**Returns `float`:**

Vector length.

----
### len2

Returns the squared vector length.

```cpp
float len2()
```

  
**Returns `float`:**

Squared vector length.

----
### lenApprox

Returns an approximate vector length.

```cpp
float lenApprox()
```

  
**Returns `float`:**

Approximate vector length.

----
### distance

Returns the distance to another vector.

```cpp
float distance(Vec3 vec)
```

**Parameters:**

* `Vec3` **vec**: Other vector.
  
**Returns `float`:**

Distance between vectors.

----
### distance2d

Returns the 2D distance to another vector (ignores Z component).

```cpp
float distance2d(Vec3 vec)
```

**Parameters:**

* `Vec3` **vec**: Other vector.
  
**Returns `float`:**

2D distance between vectors.

----
### normalize

Normalizes the vector in-place.

If the vector length is zero, no change is applied.

```cpp
Vec3 normalize()
```

  
**Returns `Vec3`:**

This vector (normalized).

----
### normalizeSafe

Normalizes the vector in-place using an epsilon check.

If the vector length is below a small threshold, no change is applied.

```cpp
Vec3 normalizeSafe()
```

  
**Returns `Vec3`:**

This vector (normalized).

----
### normalizeApprox

Normalizes the vector in-place using an approximate inverse square root.

```cpp
Vec3 normalizeApprox()
```

  
**Returns `Vec3`:**

This vector (normalized).

----
### set

Sets all components of the vector.

```cpp
void set(float x, float y, float z)
```

**Parameters:**

* `float` **x**: X component.
* `float` **y**: Y component.
* `float` **z**: Z component.
  

----
### isEqualEps

Compares this vector with another vector using an epsilon tolerance.

```cpp
boolean isEqualEps(Vec3 vec)
```

**Parameters:**

* `Vec3` **vec**: Other vector.
  
**Returns `boolean`:**

True if all components are equal within epsilon.

----
### abs

Returns a vector with absolute component values.

```cpp
Vec3 abs()
```

  
**Returns `Vec3`:**

Vector with abs(x), abs(y) and abs(z).

----
### reflect

Returns the reflection of this vector around a surface normal.

```cpp
Vec3 reflect(Vec3 normal)
```

**Parameters:**

* `Vec3` **normal**: Surface normal (typically normalized).
  
**Returns `Vec3`:**

Reflected vector.

----
### `static` swap

Swaps two vectors.

```cpp
void swap(Vec3 vec1, Vec3 vec2)
```

**Parameters:**

* `Vec3` **vec1**: First vector.
* `Vec3` **vec2**: Second vector.
  

----
### `static` min

Returns the component-wise minimum of two vectors.

```cpp
Vec3 min(Vec3 vec1, Vec3 vec2)
```

**Parameters:**

* `Vec3` **vec1**: First vector.
* `Vec3` **vec2**: Second vector.
  
**Returns `Vec3`:**

Component-wise minimum.

----
### `static` max

Returns the component-wise maximum of two vectors.

```cpp
Vec3 max(Vec3 vec1, Vec3 vec2)
```

**Parameters:**

* `Vec3` **vec1**: First vector.
* `Vec3` **vec2**: Second vector.
  
**Returns `Vec3`:**

Component-wise maximum.

----
### `static` prod

Returns the component-wise product of two vectors.

```cpp
Vec3 prod(Vec3 vec1, Vec3 vec2)
```

**Parameters:**

* `Vec3` **vec1**: First vector.
* `Vec3` **vec2**: Second vector.
  
**Returns `Vec3`:**

Component-wise product.

----
### `static` dot

Returns the dot product of two vectors.

```cpp
float dot(Vec3 vec1, Vec3 vec2)
```

**Parameters:**

* `Vec3` **vec1**: First vector.
* `Vec3` **vec2**: Second vector.
  
**Returns `float`:**

Dot product.

----
### `static` cross

Returns the cross product of two vectors.

```cpp
Vec3 cross(Vec3 vec1, Vec3 vec2)
```

**Parameters:**

* `Vec3` **vec1**: First vector.
* `Vec3` **vec2**: Second vector.
  
**Returns `Vec3`:**

Cross product.

----
### `static` lerp

Linearly interpolates between two vectors.

```cpp
Vec3 lerp(float t, Vec3 v1, Vec3 v2)
```

**Parameters:**

* `float` **t**: Interpolation factor (typically 0..1).
* `Vec3` **v1**: Start vector.
* `Vec3` **v2**: End vector.
  
**Returns `Vec3`:**

Interpolated vector.

----

## Callbacks
No callbacks.

----
