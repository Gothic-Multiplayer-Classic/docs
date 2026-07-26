---
title: 'Draw'
---
# `class` Draw <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

2D text drawing helper for rendering overlay text on screen.

### Constructor
```cpp
Draw.new()
```

**Parameters:**

No parameters.
### Constructor
```cpp
Draw.new(number x, number y, string text)
```

**Parameters:**

* `number` **x**: Initial X position (virtual units).
* `number` **y**: Initial Y position (virtual units).
* `string` **text**: Initial text content.

## Properties
### `{x, y}` position 

Represents the draw position in virtual screen units.

----
### `{x, y}` positionPx 

Represents the draw position in pixel coordinates.

----
### `string` text 

Represents the displayed text.

----
### `string` font 

Represents the font identifier used for rendering.

----
### `number` width 

Represents the rendered text width in virtual screen units.

----
### `number` height 

Represents the rendered text height in virtual screen units.

----
### `{r, g, b, a}` color 

Represents the draw's color.

----
### `number` alpha 

Represents the draw's alpha.

----
### `boolean` visible 

Represents whether the Draw object is rendered.

----

## Methods
### setPosition

This function will set the draw position in virtual screen units.

```cpp
void setPosition(number x, number y)
```

**Parameters:**

* `number` **x**: X position.
* `number` **y**: Y position.
  

----
### getPosition

This function will return the draw position in virtual screen units.

```cpp
{x, y} getPosition()
```

  
**Returns `{x, y}`:**

Table containing x and y numbers.

----
### setPositionPx

This function will set the draw position in pixel coordinates.

```cpp
void setPositionPx(number x, number y)
```

**Parameters:**

* `number` **x**: X position.
* `number` **y**: Y position.
  

----
### getPositionPx

This function will return the draw position in pixel coordinates.

```cpp
{x, y} getPositionPx()
```

  
**Returns `{x, y}`:**

Table containing x and y numbers.

----
### setText

This function will set the text to render.

```cpp
void setText(string text)
```

**Parameters:**

* `string` **text**: Text to display.
  

----
### getText

This function will return the current text.

```cpp
string getText()
```

  
**Returns `string`:**

Current text.

----
### setFont

This function will set the font used for rendering.

```cpp
void setFont(string font)
```

**Parameters:**

* `string` **font**: Font file name.
  

----
### getFont

This function will return the current font file name.

```cpp
string getFont()
```

  
**Returns `string`:**

Font file name.

----
### getWidth

This function returns the rendered text width in virtual screen units.

```cpp
number getWidth()
```

  
**Returns `number`:**

Text width.

----
### getHeight

This function returns the rendered text height in virtual screen units.

```cpp
number getHeight()
```

  
**Returns `number`:**

Text height.

----
### setColor

This function will set the text color.

```cpp
void setColor(number r, number g, number b)
```

**Parameters:**

* `number` **r**: The red color component in RGB model.
* `number` **g**: The green color component in RGB model.
* `number` **b**: The blue color component in RGB model.
  

----
### getColor

This function will return the current text color.

```cpp
{r, g, b, a} getColor()
```

  
**Returns `{r, g, b, a}`:**

Table containing color in RGBA model.

----
### setAlpha

This function will set the text alpha.

```cpp
void setAlpha(number alpha)
```

**Parameters:**

* `number` **alpha**: Opacity value (0-255).
  

----
### getAlpha

This function will return the current alpha

```cpp
number getAlpha()
```

  
**Returns `number`:**

Opacity value (0-255).

----
### setVisible

This function will set whether the Draw object should render.

```cpp
void setVisible(boolean visible)
```

**Parameters:**

* `boolean` **visible**: True to render, false to hide.
  

----
### getVisible

This function will return whether this Draw object is visible.

```cpp
boolean getVisible()
```

  
**Returns `boolean`:**

True if visible.

----

## Callbacks
No callbacks.

----
