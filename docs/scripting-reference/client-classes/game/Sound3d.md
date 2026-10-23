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
### `number` obstruction 

Represents 3D sound obstruction.

----
### `number` radius 

3D sound radius in world units.

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

Attached Vob. Set to nil to detach the sound from its target.

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

Sets a streamed player or server NPC as the 3D sound source.

```cpp
boolean setTargetPlayer(number playerId)
```

**Parameters:**

* `number` **playerId**: Streamed player or server NPC id; client-local NPC ids are not supported.
  
**Returns `boolean`:**

True if the target exists in the game world.

----

## Callbacks
No callbacks.

----
