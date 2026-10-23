---
title: 'Sprite'
---
# `class` Sprite <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This class represents a 2d Sprite on screen.

### Constructor
```cpp
Sprite.new(number x, number y, number width, number height, string file)
```

**Parameters:**

* `number` **x**: X position (virtual units).
* `number` **y**: Y position (virtual units).
* `number` **width**: Width (virtual units).
* `number` **height**: Height (virtual units).
* `string` **file**: Texture file path displayed by the sprite.

## Properties
### `{x, y}` position 

Represents the Sprite position in virtual screen units.

----
### `{x, y}` positionPx 

Represents the Sprite position in pixel coordinates.

----
### `{width, height}` size 

Represents the Sprite size in virtual screen units.

----
### `{width, height}` sizePx 

Represents the Sprite size in pixel coordinates.

----
### `{r, g, b, a}` color 

Represents the Sprite color.

----
### `number` alpha 

Opacity from 0 (transparent) to 255 (opaque).

----
### `string` file 

Represents the texture file path.

----
### `boolean` visible 

Represents whether the texture is rendered.

----
### `table` uvRect 

Normalized texture rectangle {x, y, width, height}, independent of screen position and size.

----

## Methods
### setPosition

This method will set the Sprite position in virtual screen units.

```cpp
void setPosition(number x, number y)
```

**Parameters:**

* `number` **x**: X position (virtual units).
* `number` **y**: Y position (virtual units).
  

----
### getPosition

This method will return the Sprite position in virtual screen units.

```cpp
{x, y} getPosition()
```

  
**Returns `{x, y}`:**

Table containing x and y (virtual units).

----
### setPositionPx

This method will set the Sprite position in pixel coordinates.

```cpp
void setPositionPx(number x, number y)
```

**Parameters:**

* `number` **x**: X position (pixels).
* `number` **y**: Y position (pixels).
  

----
### getPositionPx

This method will return the Sprite position in pixel coordinates.

```cpp
{x, y} getPositionPx()
```

  
**Returns `{x, y}`:**

Table containing x and y (pixels).

----
### setSize

This method will set the Sprite size in virtual screen units.

```cpp
void setSize(number width, number height)
```

**Parameters:**

* `number` **width**: Width (virtual units).
* `number` **height**: Height (virtual units).
  

----
### getSize

This method will return the Sprite size in virtual screen units.

```cpp
{width, height} getSize()
```

  
**Returns `{width, height}`:**

Table containing width and height (virtual units).

----
### setSizePx

This method will set the Sprite size in pixel coordinates.

```cpp
void setSizePx(number width, number height)
```

**Parameters:**

* `number` **width**: Width (pixels).
* `number` **height**: Height (pixels).
  

----
### getSizePx

This method will return the Sprite size in pixel coordinates.

```cpp
{width, height} getSizePx()
```

  
**Returns `{width, height}`:**

Table containing width and height (pixels).

----
### setColor

This method will set the Sprite color.

```cpp
void setColor(number r, number g, number b)
```

**Parameters:**

* `number` **r**: The red color component in RGB model.
* `number` **g**: The green color component in RGB model.
* `number` **b**: The blue color component in RGB model.
  

----
### getColor

This method will return the Sprite color.

```cpp
{r, g, b, a} getColor()
```

  
**Returns `{r, g, b, a}`:**

Table containing color in RGBA model.

----
### setAlpha

This method will set the Sprite alpha.

```cpp
void setAlpha(number alpha)
```

**Parameters:**

* `number` **alpha**: Opacity value (0-255).
  

----
### getAlpha

This method will return the current Sprite alpha (opacity).

```cpp
number getAlpha()
```

  
**Returns `number`:**

Opacity value (0-255).

----
### setFile

This method will set the Texture file name.

```cpp
void setFile(string file)
```

**Parameters:**

* `string` **file**: Texture file name.
  

----
### getFile

This method will return the Texture file name.

```cpp
string getFile()
```

  
**Returns `string`:**

Texture file name.

----
### setVisible

This method will set whether the Sprite should be rendered.

```cpp
void setVisible(boolean visible)
```

**Parameters:**

* `boolean` **visible**: True to render, false to hide.
  

----
### getVisible

This method will return whether the Sprite is visible.

```cpp
boolean getVisible()
```

  
**Returns `boolean`:**

True if visible.

----
### bringToFront

This method will move the Sprite to the front of the render order.

```cpp
void bringToFront()
```

  

----
### getUVRect

Returns the normalized texture rectangle; screen position and size are independent.

```cpp
table getUVRect()
```

  
**Returns `table`:**

{x, y, width, height} in normalized UV coordinates.

----
### setUVRect

Sets the normalized texture rectangle. Coordinates must be finite; values outside 0..1 follow renderer addressing behavior.

```cpp
void setUVRect(number u, number v, number width, number height)
```

**Parameters:**

* `number` **u**: Left texture coordinate.
* `number` **v**: Top texture coordinate.
* `number` **width**: Texture rectangle width.
* `number` **height**: Texture rectangle height.
  

----

## Callbacks
No callbacks.

----
