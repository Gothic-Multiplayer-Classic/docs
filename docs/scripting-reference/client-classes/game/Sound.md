---
title: 'Sound'
---
# `class` Sound <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This class controls playback of a non-positional sound.

### Constructor
```cpp
Sound.new(string file)
```

**Parameters:**

* `string` **file**: Sound file path.

## Properties
### `string` file 

Represents the sound file path.

----
### `number` duration <font size="2">(read-only)</font>

Represents the total sound duration in seconds.

----
### `number` volume 

Playback volume from 0.0 to 1.0.

----
### `boolean` looping 

Represents whether the sound should loop.

----
### `number` balance 

Stereo balance from -1 (left) through 0 (center) to 1 (right).

----

## Methods
### play

This method will start Sound playback.

```cpp
void play()
```

  

----
### stop

This method will stop Sound playback.

```cpp
void stop()
```

  

----
### isPlaying

This method will return whether the Sound is currently playing.

```cpp
boolean isPlaying()
```

  
**Returns `boolean`:**

True if the sound is playing.

----

## Callbacks
No callbacks.

----
