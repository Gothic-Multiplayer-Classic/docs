---
title: 'Texture'
---
# `class` Texture <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This class represents a 2d Texture on screen.

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

Represents the Texture position in virtual screen units.

----
### `{x, y}` positionPx 

Represents the Texture position in pixel coordinates.

----
### `{width, height}` size 

Represents the Texture size in virtual screen units.

----
### `{width, height}` sizePx 

Represents the Texture size in pixel coordinates.

----
### `{x, y, width, height}` rect 

Represents the Texture rectangle in virtual screen units.

----
### `{x, y, width, height}` rectPx 

Represents the Texture rectangle in pixel coordinates.

----
### `{r, g, b}` color 

Represents the Texture color.

----
### `number` alpha 

Represents the Texture alpha .

----
### `boolean` visible 

Represents whether the texture is rendered.

----
### `string` file 

Represents the texture file path.

----

## Methods
### setPosition

This method will set the Texture position in virtual screen units.

```cpp
void setPosition(number x, number y)
```

**Parameters:**

* `number` **x**: X position (virtual units).
* `number` **y**: Y position (virtual units).
  

----
### getPosition

This method will return the Texture position in virtual screen units.

```cpp
{x, y} getPosition()
```

  
**Returns `{x, y}`:**

Table containing x and y (virtual units).

----
### setPositionPx

This method will set the Texture position in pixel coordinates.

```cpp
void setPositionPx(number x, number y)
```

**Parameters:**

* `number` **x**: X position (pixels).
* `number` **y**: Y position (pixels).
  

----
### getPositionPx

This method will return the Texture position in pixel coordinates.

```cpp
{x, y} getPositionPx()
```

  
**Returns `{x, y}`:**

Table containing x and y (pixels).

----
### setSize

This method will set the Texture size in virtual screen units.

```cpp
void setSize(number width, number height)
```

**Parameters:**

* `number` **width**: Width (virtual units).
* `number` **height**: Height (virtual units).
  

----
### getSize

This method will return the Texture size in virtual screen units.

```cpp
{width, height} getSize()
```

  
**Returns `{width, height}`:**

Table containing width and height (virtual units).

----
### setSizePx

This method will set the Texture size in pixel coordinates.

```cpp
void setSizePx(number width, number height)
```

**Parameters:**

* `number` **width**: Width (pixels).
* `number` **height**: Height (pixels).
  

----
### getSizePx

This method will return the Texture size in pixel coordinates.

```cpp
{width, height} getSizePx()
```

  
**Returns `{width, height}`:**

Table containing width and height (pixels).

----
### setRect

This method will set the Texture rectangle in virtual screen units.

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

This method will return the Texture rectangle in virtual screen units.

```cpp
{x, y, width, height} getRect()
```

  
**Returns `{x, y, width, height}`:**

Table containing x,y,width,height (virtual units).

----
### setRectPx

This method will set the Texture rectangle in pixel coordinates.

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

This method will return the Texture rectangle in pixel coordinates.

```cpp
{x, y, width, height} getRectPx()
```

  
**Returns `{x, y, width, height}`:**

Table containing x,y,width,height (pixels).

----
### setColor

This method will set the Texture color.

```cpp
void setColor(number r, number g, number b)
```

**Parameters:**

* `number` **r**: The red color component in RGB model.
* `number` **g**: The green color component in RGB model.
* `number` **b**: The blue color component in RGB model.
  

----
### getColor

This method will return the Texture color.

```cpp
{r, g, b} getColor()
```

  
**Returns `{r, g, b}`:**

Table containing color in RGB model.

----
### setAlpha

This method will set the Texture alpha.

```cpp
void setAlpha(number alpha)
```

**Parameters:**

* `number` **alpha**: Opacity value (0-255).
  

----
### getAlpha

This method will return the current Texture alpha (opacity).

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

This method will set whether the Texture should be rendered.

```cpp
void setVisible(boolean visible)
```

**Parameters:**

* `boolean` **visible**: True to render, false to hide.
  

----
### getVisible

This method will return whether the Texture is visible.

```cpp
boolean getVisible()
```

  
**Returns `boolean`:**

True if visible.

----
### top

This method will move the Texture to the top of the render order.

```cpp
void top()
```

  

----

## Callbacks
No callbacks.

----
