---
title: 'Vec4'
---
# `class` Vec4 <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

This class represents a 4d vector.

### Constructor
```cpp
Vec4.new(number value)
```

**Parameters:**

* `number` **value**: Value assigned to x, y, z and w.
### Constructor
```cpp
Vec4.new(number x, number y, number z, number w)
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
### normalize

This method normalizes the vector in-place.
If the vector length is zero, no change is applied.

```cpp
Vec4 normalize()
```

  
**Returns `Vec4`:**

This vector (normalized).

----
### normalizeSafe

This method normalizes the vector in-place using an epsilon check.
If the vector length is below a small threshold, no change is applied.

```cpp
Vec4 normalizeSafe()
```

  
**Returns `Vec4`:**

This vector (normalized).

----
### normalizeApprox

This method normalizes the vector in-place using an approximate inverse square root.

```cpp
Vec4 normalizeApprox()
```

  
**Returns `Vec4`:**

This vector (normalized).

----
### set

This method sets all components of the vector.

```cpp
void set(number x, number y, number z, number w)
```

**Parameters:**

* `number` **x**: X component.
* `number` **y**: Y component.
* `number` **z**: Z component.
* `number` **w**: W component.
  

----
### isEqualEps

This method compares this vector with another vector using an epsilon tolerance.

```cpp
boolean isEqualEps(Vec4 vec)
```

**Parameters:**

* `Vec4` **vec**: Other vector.
  
**Returns `boolean`:**

True if all components are equal within epsilon.

----
### abs

This method returns a vector with absolute component values.

```cpp
Vec4 abs()
```

  
**Returns `Vec4`:**

Vector with abs(x), abs(y), abs(z) and abs(w).

----
### `static` swap

This method swaps two vectors.

```cpp
void swap(Vec4 vec1, Vec4 vec2)
```

**Parameters:**

* `Vec4` **vec1**: First vector.
* `Vec4` **vec2**: Second vector.
  

----
### `static` min

This method returns the component-wise minimum of two vectors.

```cpp
Vec4 min(Vec4 vec1, Vec4 vec2)
```

**Parameters:**

* `Vec4` **vec1**: First vector.
* `Vec4` **vec2**: Second vector.
  
**Returns `Vec4`:**

Component-wise minimum.

----
### `static` max

This method returns the component-wise maximum of two vectors.

```cpp
Vec4 max(Vec4 vec1, Vec4 vec2)
```

**Parameters:**

* `Vec4` **vec1**: First vector.
* `Vec4` **vec2**: Second vector.
  
**Returns `Vec4`:**

Component-wise maximum.

----
### `static` prod

This method returns the component-wise product of two vectors.

```cpp
Vec4 prod(Vec4 vec1, Vec4 vec2)
```

**Parameters:**

* `Vec4` **vec1**: First vector.
* `Vec4` **vec2**: Second vector.
  
**Returns `Vec4`:**

Component-wise product.

----
### `static` dot

This method returns the dot product of two vectors.

```cpp
number dot(Vec4 vec1, Vec4 vec2)
```

**Parameters:**

* `Vec4` **vec1**: First vector.
* `Vec4` **vec2**: Second vector.
  
**Returns `number`:**

Dot product.

----
### `static` lerp

This method linearly interpolates between two vectors.

```cpp
Vec4 lerp(number t, Vec4 v1, Vec4 v2)
```

**Parameters:**

* `number` **t**: Interpolation factor (typically 0..1).
* `Vec4` **v1**: Start vector.
* `Vec4` **v2**: End vector.
  
**Returns `Vec4`:**

Interpolated vector.

----

## Callbacks
No callbacks.

----
