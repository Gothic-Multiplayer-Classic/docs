---
title: 'Vec2'
---
# `class` Vec2 <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

2D vector with basic math utilities.

### Constructor
```cpp
Vec2.new(float value)
```

**Parameters:**

* `float` **value**: Value assigned to x and y.
### Constructor
```cpp
Vec2.new(float x, float y)
```

**Parameters:**

* `float` **x**: X component.
* `float` **y**: Y component.

## Properties
### `float` x 

X component.

----
### `float` y 

Y component.

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
float distance(Vec2 vec)
```

**Parameters:**

* `Vec2` **vec**: Other vector.
  
**Returns `float`:**

Distance between vectors.

----
### normalize

Normalizes the vector in-place.

If the vector length is zero, no change is applied.

```cpp
Vec2 normalize()
```

  
**Returns `Vec2`:**

This vector (normalized).

----
### normalizeSafe

Normalizes the vector in-place using an epsilon check.

If the vector length is below a small threshold, no change is applied.

```cpp
Vec2 normalizeSafe()
```

  
**Returns `Vec2`:**

This vector (normalized).

----
### normalizeApprox

Normalizes the vector in-place using an approximate inverse square root.

```cpp
Vec2 normalizeApprox()
```

  
**Returns `Vec2`:**

This vector (normalized).

----
### set

Sets both components of the vector.

```cpp
void set(float x, float y)
```

**Parameters:**

* `float` **x**: X component.
* `float` **y**: Y component.
  

----
### isEqualEps

Compares this vector with another vector using an epsilon tolerance.

```cpp
boolean isEqualEps(Vec2 vec)
```

**Parameters:**

* `Vec2` **vec**: Other vector.
  
**Returns `boolean`:**

True if both components are equal within epsilon.

----
### abs

Returns a vector with absolute component values.

```cpp
Vec2 abs()
```

  
**Returns `Vec2`:**

Vector with abs(x) and abs(y).

----
### `static` swap

Swaps two vectors.

```cpp
void swap(Vec2 vec1, Vec2 vec2)
```

**Parameters:**

* `Vec2` **vec1**: First vector.
* `Vec2` **vec2**: Second vector.
  

----
### `static` min

Returns the component-wise minimum of two vectors.

```cpp
Vec2 min(Vec2 vec1, Vec2 vec2)
```

**Parameters:**

* `Vec2` **vec1**: First vector.
* `Vec2` **vec2**: Second vector.
  
**Returns `Vec2`:**

Component-wise minimum.

----
### `static` max

Returns the component-wise maximum of two vectors.

```cpp
Vec2 max(Vec2 vec1, Vec2 vec2)
```

**Parameters:**

* `Vec2` **vec1**: First vector.
* `Vec2` **vec2**: Second vector.
  
**Returns `Vec2`:**

Component-wise maximum.

----
### `static` prod

Returns the component-wise product of two vectors.

```cpp
Vec2 prod(Vec2 vec1, Vec2 vec2)
```

**Parameters:**

* `Vec2` **vec1**: First vector.
* `Vec2` **vec2**: Second vector.
  
**Returns `Vec2`:**

Component-wise product.

----
### `static` dot

Returns the dot product of two vectors.

```cpp
float dot(Vec2 vec1, Vec2 vec2)
```

**Parameters:**

* `Vec2` **vec1**: First vector.
* `Vec2` **vec2**: Second vector.
  
**Returns `float`:**

Dot product.

----
### `static` lerp

Linearly interpolates between two vectors.

```cpp
Vec2 lerp(float t, Vec2 v1, Vec2 v2)
```

**Parameters:**

* `float` **t**: Interpolation factor (typically 0..1).
* `Vec2` **v1**: Start vector.
* `Vec2` **v2**: End vector.
  
**Returns `Vec2`:**

Interpolated vector.

----

## Callbacks
No callbacks.

----
