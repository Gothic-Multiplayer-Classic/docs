---
title: 'Vec2'
---
# `class` Vec2 <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

This class represents a 2d vector.

### Constructor
```cpp
Vec2.new(number value)
```

**Parameters:**

* `number` **value**: Value assigned to x and y.
### Constructor
```cpp
Vec2.new(number x, number y)
```

**Parameters:**

* `number` **x**: X component.
* `number` **y**: Y component.

## Properties
### `number` x 

Represents the X component.

----
### `number` y 

Represents the Y component.

----

## Methods
### len

This method returns the vector length (magnitude).

```cpp
number len()
```

  
**Returns `number`:**

Vector length.

----
### len2

This method returns the squared vector length.

```cpp
number len2()
```

  
**Returns `number`:**

Squared vector length.

----
### lenApprox

This method returns an approximate vector length.

```cpp
number lenApprox()
```

  
**Returns `number`:**

Approximate vector length.

----
### distance

This method returns the distance to another vector.

```cpp
number distance(Vec2 vec)
```

**Parameters:**

* `Vec2` **vec**: Other vector.
  
**Returns `number`:**

Distance between vectors.

----
### normalize

This method normalizes the vector in-place.
If the vector length is zero, no change is applied.

```cpp
Vec2 normalize()
```

  
**Returns `Vec2`:**

This vector (normalized).

----
### normalizeSafe

This method normalizes the vector in-place using an epsilon check.
If the vector length is below a small threshold, no change is applied.

```cpp
Vec2 normalizeSafe()
```

  
**Returns `Vec2`:**

This vector (normalized).

----
### normalizeApprox

This method normalizes the vector in-place using an approximate inverse square root.

```cpp
Vec2 normalizeApprox()
```

  
**Returns `Vec2`:**

This vector (normalized).

----
### set

This method sets both components of the vector.

```cpp
void set(number x, number y)
```

**Parameters:**

* `number` **x**: X component.
* `number` **y**: Y component.
  

----
### isEqualEps

This method compares this vector with another vector using an epsilon tolerance.

```cpp
boolean isEqualEps(Vec2 vec)
```

**Parameters:**

* `Vec2` **vec**: Other vector.
  
**Returns `boolean`:**

True if both components are equal within epsilon.

----
### abs

This method returns a vector with absolute component values.

```cpp
Vec2 abs()
```

  
**Returns `Vec2`:**

Vector with abs(x) and abs(y).

----
### `static` swap

This method swaps two vectors.

```cpp
void swap(Vec2 vec1, Vec2 vec2)
```

**Parameters:**

* `Vec2` **vec1**: First vector.
* `Vec2` **vec2**: Second vector.
  

----
### `static` min

This method returns the component-wise minimum of two vectors.

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

This method returns the component-wise maximum of two vectors.

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

This method returns the component-wise product of two vectors.

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

This method returns the dot product of two vectors.

```cpp
number dot(Vec2 vec1, Vec2 vec2)
```

**Parameters:**

* `Vec2` **vec1**: First vector.
* `Vec2` **vec2**: Second vector.
  
**Returns `number`:**

Dot product.

----
### `static` lerp

This method linearly interpolates between two vectors.

```cpp
Vec2 lerp(number t, Vec2 v1, Vec2 v2)
```

**Parameters:**

* `number` **t**: Interpolation factor (typically 0..1).
* `Vec2` **v1**: Start vector.
* `Vec2` **v2**: End vector.
  
**Returns `Vec2`:**

Interpolated vector.

----

## Callbacks
No callbacks.

----
