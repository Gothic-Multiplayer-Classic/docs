---
title: 'Sound3d'
---
# `class` Sound3d <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This class represents a positional 3D sound attached to an engine Vob.

### Constructor
```cpp
Sound3d.new(string file)
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
### `number` obstruction 

Represents 3D sound obstruction.

----
### `number` radius 

Represents 3D sound radius.

----
### `number` coneAngle 

Represents 3D sound cone angle in degrees.

----
### `number` reverbLevel 

Represents 3D sound reverb level.

----
### `boolean` ambient 

Represents whether the sound uses ambient 3D behavior.

----
### `number` pitchOffset 

Represents 3D sound pitch offset.

----
### `Vob|nil` targetVob 

Represents the target Vob used as sound source.

----

## Methods
### play

Starts 3D sound playback at the current target Vob.

```cpp
void play()
```

  

----
### stop

Stops 3D sound playback.

```cpp
void stop()
```

  

----
### isPlaying

Returns whether the 3D sound is currently playing.

```cpp
boolean isPlaying()
```

  
**Returns `boolean`:**

True if the sound is playing.

----
### update

Updates the active 3D sound parameters in the engine.

```cpp
void update()
```

  

----
### setTargetVob

Sets the Vob used as the 3D sound source.

```cpp
void setTargetVob(Vob vob)
```

**Parameters:**

* `Vob` **vob**: Target Vob.
  

----
### setTargetPlayer

Sets a player NPC as the 3D sound source.

```cpp
boolean setTargetPlayer(number playerId)
```

**Parameters:**

* `number` **playerId**: Player id.
  
**Returns `boolean`:**

True if the player exists and has an NPC.

----

## Callbacks
No callbacks.

----
