---
title: 'Sound'
---
# `class` Sound <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"



### Constructor
```cpp
Sound.new(string file)
```

**Parameters:**

* `string` **file**: Sound file path.

## Properties
### `string` file 

Get or set the sound file path.

----
### `number` playingTime <font size="2">(read-only)</font>

Return the current playback time.

----
### `number` volume 

Get or set the playback volume.

----
### `boolean` looping 

Get or set whether the sound should loop.

----
### `number` balance 

Get or set the stereo balance (pan).

----

## Methods
### play

Start sound playback.

```cpp
void play()
```

  

----
### stop

Stop sound playback.

```cpp
void stop()
```

  

----
### isPlaying

Return whether the sound is currently playing.

```cpp
boolean isPlaying()
```

  
**Returns `boolean`:**

True if the sound is playing.

----

## Callbacks
No callbacks.

----
