---
title: 'Texture'
---
# `class` Texture <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"



### Constructor
```cpp
Texture.new(number x, number y, number width, number height, string file)
```

**Parameters:**

* `number` **x**: X position (virtual units).
* `number` **y**: Y position (virtual units).
* `number` **width**: Width (virtual units).
* `number` **height**: Height (virtual units).
* `string` **file**: Texture file path.

## Properties
### `{x, y}` position 

Gets or sets the texture position in virtual screen units.

----
### `{x, y}` positionPx 

Gets or sets the texture position in pixel coordinates.

----
### `{width, height}` size 

Gets or sets the texture size in virtual screen units.

----
### `{width, height}` sizePx 

Gets or sets the texture size in pixel coordinates.

----
### `{x, y, width, height}` rect 

Gets or sets the texture rectangle in virtual screen units.

----
### `{x, y, width, height}` rectPx 

Gets or sets the texture rectangle in pixel coordinates.

----
### `{r, g, b}` color 

Gets or sets the texture color.

----
### `number` alpha 

Gets or sets the texture alpha (opacity).

----
### `boolean` visible 

Gets or sets whether the texture is rendered.

----
### `string` file 

Gets or sets the texture file path.

----

## Methods
### setPosition

Sets the texture position in virtual screen units.

```cpp
void setPosition(number x, number y)
```

**Parameters:**

* `number` **x**: X position (virtual units).
* `number` **y**: Y position (virtual units).
  

----
### getPosition

Returns the texture position in virtual screen units.

```cpp
{x, y} getPosition()
```

  
**Returns `{x, y}`:**

Table containing x and y (virtual units).

----
### setPositionPx

Sets the texture position in pixel coordinates.

```cpp
void setPositionPx(number x, number y)
```

**Parameters:**

* `number` **x**: X position (pixels).
* `number` **y**: Y position (pixels).
  

----
### getPositionPx

Returns the texture position in pixel coordinates.

```cpp
{x, y} getPositionPx()
```

  
**Returns `{x, y}`:**

Table containing x and y (pixels).

----
### setSize

Sets the texture size in virtual screen units.

```cpp
void setSize(number width, number height)
```

**Parameters:**

* `number` **width**: Width (virtual units).
* `number` **height**: Height (virtual units).
  

----
### getSize

Returns the texture size in virtual screen units.

```cpp
{width, height} getSize()
```

  
**Returns `{width, height}`:**

Table containing width and height (virtual units).

----
### setSizePx

Sets the texture size in pixel coordinates.

```cpp
void setSizePx(number width, number height)
```

**Parameters:**

* `number` **width**: Width (pixels).
* `number` **height**: Height (pixels).
  

----
### getSizePx

Returns the texture size in pixel coordinates.

```cpp
{width, height} getSizePx()
```

  
**Returns `{width, height}`:**

Table containing width and height (pixels).

----
### setRect

Sets the texture rectangle in virtual screen units.

```cpp
void setRect(number x, number y, number width, number height)
```

**Parameters:**

* `number` **x**: X position (virtual units).
* `number` **y**: Y position (virtual units).
* `number` **width**: Width (virtual units).
* `number` **height**: Height (virtual units).
  

----
### getRect

Returns the texture rectangle in virtual screen units.

```cpp
{x, y, width, height} getRect()
```

  
**Returns `{x, y, width, height}`:**

Table containing x,y,width,height (virtual units).

----
### setRectPx

Sets the texture rectangle in pixel coordinates.

```cpp
void setRectPx(number x, number y, number width, number height)
```

**Parameters:**

* `number` **x**: X position (pixels).
* `number` **y**: Y position (pixels).
* `number` **width**: Width (pixels).
* `number` **height**: Height (pixels).
  

----
### getRectPx

Returns the texture rectangle in pixel coordinates.

```cpp
{x, y, width, height} getRectPx()
```

  
**Returns `{x, y, width, height}`:**

Table containing x,y,width,height (pixels).

----
### setColor

Sets the texture color.

```cpp
void setColor(number r, number g, number b)
```

**Parameters:**

* `number` **r**: Red component (0-255).
* `number` **g**: Green component (0-255).
* `number` **b**: Blue component (0-255).
  

----
### getColor

Returns the texture color.

```cpp
{r, g, b} getColor()
```

  
**Returns `{r, g, b}`:**

Table containing r,g,b (0-255).

----
### setAlpha

Sets the texture alpha (opacity).

```cpp
void setAlpha(number alpha)
```

**Parameters:**

* `number` **alpha**: Opacity value (0-255).
  

----
### getAlpha

Returns the texture alpha (opacity).

```cpp
number getAlpha()
```

  
**Returns `number`:**

Opacity value (0-255).

----
### setFile

Sets the texture file name.

```cpp
void setFile(string file)
```

**Parameters:**

* `string` **file**: Texture file name.
  

----
### getFile

Returns the texture file name.

```cpp
string getFile()
```

  
**Returns `string`:**

Texture file name.

----
### setVisible

Sets whether the texture should be rendered.

```cpp
void setVisible(boolean visible)
```

**Parameters:**

* `boolean` **visible**: True to render, false to hide.
  

----
### getVisible

Returns whether the texture is visible.

```cpp
boolean getVisible()
```

  
**Returns `boolean`:**

True if visible.

----
### top

Moves the texture to the top of the render order.

```cpp
void top()
```

  

----

## Callbacks
No callbacks.

----
