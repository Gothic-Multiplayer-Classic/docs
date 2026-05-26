---
title: 'MusicTheme'
---
# `class` MusicTheme <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

Static access to the engine music theme system.


## Properties
### `string` fileName 

Represents the loaded theme file name.

----
### `number` volume 

Represents the theme volume.

----
### `boolean` loop 

Represents whether the theme should loop.

----
### `boolean` disabled 

Represents whether the engine music system is disabled.

----
### `string|nil` activeTheme 

Represents the active engine music theme name or file name.

----
### `number` reverbMix 

Represents the theme reverb mix.

----
### `number` reverbTime 

Represents the theme reverb time.

----
### `number` transType 

Represents the theme transition type.

----
### `number` transSubType 

Represents the theme transition subtype.

----
### `string` name 

Represents the theme script name.

----

## Methods
### loadTheme

Loads a music theme by script name, falling back to a raw file name.

```cpp
boolean loadTheme(string fileName)
```

**Parameters:**

* `string` **fileName**: Theme script name or file name.
  
**Returns `boolean`:**

True if the theme was loaded.

----
### playTheme

Plays the currently loaded theme.

```cpp
boolean playTheme()
```

  
**Returns `boolean`:**

True if playback was started.

----
### stopTheme

Stops music theme playback.

```cpp
void stopTheme()
```

  

----

## Callbacks
No callbacks.

----
