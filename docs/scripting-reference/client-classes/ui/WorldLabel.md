---
title: 'WorldLabel'
---
# `class` WorldLabel <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

3D text drawing helper for rendering world-space text on screen.

### Constructor
```cpp
WorldLabel.new()
```

**Parameters:**

No parameters.
### Constructor
```cpp
WorldLabel.new(number x, number y, number z)
```

**Parameters:**

* `number` **x**: Initial X world position.
* `number` **y**: Initial Y world position.
* `number` **z**: Initial Z world position.
### Constructor
```cpp
WorldLabel.new(number x, number y, number z, string text)
```

**Parameters:**

* `number` **x**: Initial X world position.
* `number` **y**: Initial Y world position.
* `number` **z**: Initial Z world position.
* `string` **text**: Initial text line.

## Properties
### `{x, y, z}` position 

World position {x, y, z}, projected onto the screen while rendering.

----
### `table` lines 

Dense one-based array of text lines. See `getLines` and `setLines`.

----
### `string` font 

Represents the font identifier used for rendering.

----
### `{r, g, b, a}` color 

Represents the WorldLabel color.

----
### `number` alpha 

Opacity from 0 (transparent) to 255 (opaque).

----
### `boolean` visible 

Represents whether the WorldLabel object is rendered.

----
### `number` maxRenderDistance 

Maximum distance from the local hero in world units; this is independent of the camera.

----
### `string` text 

Complete text as a newline-separated string. Reading and writing use the same representation.

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
### appendLine

Appends a text line to the WorldLabel object.

```cpp
void appendLine(string text)
```

**Parameters:**

* `string` **text**: Text line to append.
  

----
### clearLines

Removes all text lines.

```cpp
void clearLines()
```

  

----
### getLines

Returns all text lines.

```cpp
table getLines()
```

  
**Returns `table`:**

Array-like table of text lines.

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

Sets whether the WorldLabel object should `render`.

```cpp
void setVisible(boolean visible)
```

**Parameters:**

* `boolean` **visible**: True to render, false to hide.
  

----
### getVisible

Returns whether this WorldLabel object is visible.

```cpp
boolean getVisible()
```

  
**Returns `boolean`:**

True if visible.

----
### setMaxRenderDistance

Sets the max render distance from the local player.

```cpp
void setMaxRenderDistance(number distance)
```

**Parameters:**

* `number` **distance**: Max distance in world units. Zero disables distance culling.
  

----
### getMaxRenderDistance

Returns the max render distance.

```cpp
number getMaxRenderDistance()
```

  
**Returns `number`:**

Max distance in world units.

----
### bringToFront

Moves the WorldLabel view to the front of the screen view stack.

```cpp
void bringToFront()
```

  

----
### render

Forces immediate rendering of this WorldLabel object.

```cpp
void render()
```

  

----
### setLines

Atomically replaces the label lines. The input must be a dense one-based string array.

```cpp
void setLines(table lines)
```

**Parameters:**

* `table` **lines**: Array of text lines.
  

----
### getText

Returns all lines joined by newline characters.

```cpp
string getText()
```

  
**Returns `string`:**

Complete label text.

----
### setText

Replaces all lines by splitting text on newline characters.

```cpp
void setText(string text)
```

**Parameters:**

* `string` **text**: Complete label text.
  

----
### removeLine

Removes one line by its one-based index.

```cpp
boolean removeLine(number index)
```

**Parameters:**

* `number` **index**: Line index starting at 1.
  
**Returns `boolean`:**

False if out of range.

----
### setLine

Replaces one existing line by its one-based index.

```cpp
boolean setLine(number index, string text)
```

**Parameters:**

* `number` **index**: Line index starting at 1.
* `string` **text**: Replacement text.
  
**Returns `boolean`:**

False if out of range.

----
### getLine

Returns one line by its one-based index.

```cpp
string|nil getLine(number index)
```

**Parameters:**

* `number` **index**: Line index starting at 1.
  
**Returns `string|nil`:**

Text or nil if out of range.

----

## Callbacks
No callbacks.

----
