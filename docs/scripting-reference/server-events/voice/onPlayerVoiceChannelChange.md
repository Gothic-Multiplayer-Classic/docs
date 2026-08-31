---
title: 'onPlayerVoiceChannelChange'
---
# `event` onPlayerVoiceChannelChange <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player changes voice channels.

## Parameters
```c++
void onPlayerVoiceChannelChange(number player_id, string old_channel, string new_channel)
```

* `number` **player_id**: Player id.
* `string` **old_channel**: Previous channel name.
* `string` **new_channel**: New channel name.
