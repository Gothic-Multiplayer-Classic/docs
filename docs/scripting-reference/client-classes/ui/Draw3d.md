---
title: 'Draw3d'
---
# `class` Draw3d <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

3D text drawing helper for rendering world-space text on screen.

### Constructor
```cpp
Draw3d.new()
```

**Parameters:**

No parameters.
### Constructor
```cpp
Draw3d.new(number x, number y, number z)
```

**Parameters:**

* `number` **x**: Initial X world position.
* `number` **y**: Initial Y world position.
* `number` **z**: Initial Z world position.
### Constructor
```cpp
Draw3d.new(number x, number y, number z, string text)
```

**Parameters:**

* `number` **x**: Initial X world position.
* `number` **y**: Initial Y world position.
* `number` **z**: Initial Z world position.
* `string` **text**: Initial text line.

## Properties
### `{x, y, z}` worldPosition 

Alias for position.

----
### `table` text 

Represents the displayed text lines.

----
### `string` font 

Represents the font identifier used for rendering.

----
### `{r, g, b, a}` color 

Represents the Draw3d color.

----
### `number` alpha 

Represents the Draw3d alpha.

----
### `boolean` visible 

Represents whether the Draw3d object is rendered.

----
### `number` distance 

Represents the max render distance from the local player.

----

## Methods
### setPosition

Sets the world position used to project this text to screen space.

```cpp
void setPosition(number x, number y, number z)
```

**Parameters:**

* `number` **x**: X world position.
* `number` **y**: Y world position.
* `number` **z**: Z world position.
  

----
### getPosition

Returns the current world position.

```cpp
{x, y, z} getPosition()
```

  
**Returns `{x, y, z}`:**

Table containing x,y,z world position.

----
### insertText

Appends a text line to the Draw3d object.

```cpp
void insertText(string text)
```

**Parameters:**

* `string` **text**: Text line to append.
  

----
### removeText

Removes a text line by zero-based index.

```cpp
void removeText(number index)
```

**Parameters:**

* `number` **index**: Zero-based text line index.
  

----
### updateText

Updates a text line by zero-based index.

```cpp
void updateText(number index, string text)
```

**Parameters:**

* `number` **index**: Zero-based text line index.
* `string` **text**: Replacement text.
  

----
### clearText

Removes all text lines.

```cpp
void clearText()
```

  

----
### getText

Returns all text lines.

```cpp
table getText()
```

  
**Returns `table`:**

Array-like table of text lines.

----
### setText

Replaces all text lines with one text line.

```cpp
void setText(string text)
```

**Parameters:**

* `string` **text**: Text to display.
  

----
### setFont

Sets the font used for rendering.

```cpp
void setFont(string font)
```

**Parameters:**

* `string` **font**: Font file name.
  

----
### getFont

Returns the current font file name.

```cpp
string getFont()
```

  
**Returns `string`:**

Font file name.

----
### setColor

Sets the text color.

```cpp
void setColor(number r, number g, number b)
```

**Parameters:**

* `number` **r**: Red color component.
* `number` **g**: Green color component.
* `number` **b**: Blue color component.
  

----
### getColor

Returns the text color.

```cpp
{r, g, b, a} getColor()
```

  
**Returns `{r, g, b, a}`:**

Table containing color in RGBA model.

----
### setAlpha

Sets the text alpha.

```cpp
void setAlpha(number alpha)
```

**Parameters:**

* `number` **alpha**: Opacity value (0-255).
  

----
### getAlpha

Returns the current alpha.

```cpp
number getAlpha()
```

  
**Returns `number`:**

Opacity value (0-255).

----
### setVisible

Sets whether the Draw3d object should render.

```cpp
void setVisible(boolean visible)
```

**Parameters:**

* `boolean` **visible**: True to render, false to hide.
  

----
### getVisible

Returns whether this Draw3d object is visible.

```cpp
boolean getVisible()
```

  
**Returns `boolean`:**

True if visible.

----
### setDistance

Sets the max render distance from the local player.

```cpp
void setDistance(number distance)
```

**Parameters:**

* `number` **distance**: Max distance in world units. Zero disables distance culling.
  

----
### getDistance

Returns the max render distance.

```cpp
number getDistance()
```

  
**Returns `number`:**

Max distance in world units.

----
### top

Moves the Draw3d view to the top of the screen view stack.

```cpp
void top()
```

  

----
### render

Forces immediate rendering of this Draw3d object.

```cpp
void render()
```

  

----

## Callbacks
No callbacks.

----
