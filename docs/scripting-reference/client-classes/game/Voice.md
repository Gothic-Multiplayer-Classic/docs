---
title: 'Voice'
---
# `class` Voice <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This singleton class controls native proximity voice chat for the local client.


## Properties
No properties.

----

## Methods
### isAvailable

This function checks whether the server offers voice chat.

```cpp
boolean isAvailable()
```

  
**Returns `boolean`:**

True when the server has proximity voice chat enabled.

----
### isEnabled

This function checks whether voice chat is effectively enabled for this client.

```cpp
boolean isEnabled()
```

  
**Returns `boolean`:**

True when server, user, and script settings all allow voice chat.

----
### setEnabled

This function changes the resource-controlled voice chat gate. Enabling it does not override a disabled user setting.

```cpp
boolean setEnabled(boolean enabled)
```

**Parameters:**

* `boolean` **enabled**: Whether this resource permits voice chat.
  
**Returns `boolean`:**

The resulting effective voice chat state.

----
### getRange

This function returns the effective local proximity voice range.

```cpp
number getRange()
```

  
**Returns `number`:**

Voice range in game units, or zero when unavailable.

----
### setRange

This function limits the local client's proximity voice range. The server's
range remains authoritative, so this setting can only reduce the range.

```cpp
boolean setRange(number range)
```

**Parameters:**

* `number` **range**: Maximum local voice range in game units.
  
**Returns `boolean`:**

True when the range was accepted.

----
### getOutputVolume

This function returns the resource output-volume multiplier.

```cpp
number getOutputVolume()
```

  
**Returns `number`:**

Multiplier from 0.0 to 1.0, applied after the user's volume setting.

----
### setOutputVolume

This function changes the resource output-volume multiplier.

```cpp
void setOutputVolume(number volume)
```

**Parameters:**

* `number` **volume**: Multiplier from 0.0 to 1.0, clamped to that range.
  

----
### getPushToTalkKey

This function returns the active push-to-talk key code.

```cpp
number getPushToTalkKey()
```

  
**Returns `number`:**

Key code used for push-to-talk.

----
### setPushToTalkKey

This function sets the local client's push-to-talk key for this resource.

```cpp
boolean setPushToTalkKey(number key)
```

**Parameters:**

* `number` **key**: Keyboard key code in the range 1-255.
  
**Returns `boolean`:**

True when the key was accepted.

----
### getInputDevices

This function returns the available microphone device names.

```cpp
{string...} getInputDevices()
```

  
**Returns `{string...}`:**

Available microphone names.

----
### getInputDevice

This function returns the selected microphone name. An empty string means the system default.

```cpp
string getInputDevice()
```

  
**Returns `string`:**

Selected microphone name.

----
### setInputDevice

This function selects a microphone by name. Pass an empty string to restore the system default.

```cpp
boolean setInputDevice(string device_name)
```

**Parameters:**

* `string` **device_name**: Microphone name returned by getInputDevices, or an empty string.
  
**Returns `boolean`:**

True when the device was selected.

----
### getOutputDevices

This function returns the available playback device names.

```cpp
{string...} getOutputDevices()
```

  
**Returns `{string...}`:**

Available playback device names.

----
### getOutputDevice

This function returns the selected playback device name. An empty string means the system default.

```cpp
string getOutputDevice()
```

  
**Returns `string`:**

Selected playback device name.

----
### setOutputDevice

This function selects a playback device by name. Pass an empty string to restore the system default.

```cpp
boolean setOutputDevice(string device_name)
```

**Parameters:**

* `string` **device_name**: Device name returned by getOutputDevices, or an empty string.
  
**Returns `boolean`:**

True when the device was selected.

----
### getChannel

This function returns the local player's current voice channel.

```cpp
string getChannel()
```

  
**Returns `string`:**

Current channel name.

----
### setChannel

This function changes the local player's voice channel.

```cpp
boolean setChannel(string channel)
```

**Parameters:**

* `string` **channel**: Printable channel name, up to 32 bytes.
  
**Returns `boolean`:**

True when the channel change was accepted locally and sent when connected.

----
### isTransmitting

This function checks whether the local player is currently transmitting voice.

```cpp
boolean isTransmitting()
```

  
**Returns `boolean`:**

True while voice frames are being captured and sent.

----

## Callbacks
No callbacks.

----
