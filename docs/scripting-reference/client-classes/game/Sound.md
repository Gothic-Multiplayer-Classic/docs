---
title: 'Sound'
---
# `class` Sound <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This class represents an internal sound method.

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
### `number` playingTime <font size="2">(read-only)</font>

Represents the current playback time.

----
### `number` volume 

Represents the playback volume.

----
### `boolean` looping 

Represents whether the sound should loop.

----
### `number` balance 

Represents the stereo balance (pan).

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
