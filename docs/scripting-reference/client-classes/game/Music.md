---
title: 'Music'
---
# `class` Music <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This class represents streamed music playback on the game client. It is unrelated to Zengin's implementation of Sound and Music.

### Constructor
```cpp
Music.new(string file)
```

**Parameters:**

* `string` **file**: Music file path.

## Properties
### `string` file 

Represents the music file path.

----
### `number` volume 

Represents the playback volume before options volume is applied.

----
### `boolean` looping 

Represents whether playback should loop.

----
### `number` position 

Represents the current playback position in seconds.

----
### `number` duration <font size="2">(read-only)</font>

Represents the music duration in seconds.

----
### `boolean` muteGothicMusic 

Represents whether Gothic's original music should be muted while this music plays.

----
### `number` optionsVolume <font size="2">(read-only)</font>

Represents the current Gothic music options volume multiplier.

----
### `boolean` useOptionsVolume 

Represents whether the Gothic music options volume should affect this music.

----

## Methods
### play

This method will start music playback using the current looping state.

```cpp
void play()
```

  

----
### playLooped

This method will enable looping and start music playback.

```cpp
void playLooped()
```

  

----
### pause

This method will pause music playback.

```cpp
void pause()
```

  

----
### resume

This method will resume paused music playback.

```cpp
void resume()
```

  

----
### stop

This method will stop music playback.

```cpp
void stop()
```

  

----
### isPlaying

This method will return whether the music is currently playing.

```cpp
boolean isPlaying()
```

  
**Returns `boolean`:**

True if music is playing.

----
### isPaused

This method will return whether the music is currently paused.

```cpp
boolean isPaused()
```

  
**Returns `boolean`:**

True if music is paused.

----

## Callbacks
No callbacks.

----
