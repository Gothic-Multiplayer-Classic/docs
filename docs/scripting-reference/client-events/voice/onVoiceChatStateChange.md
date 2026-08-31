---
title: 'onVoiceChatStateChange'
---
# `event` onVoiceChatStateChange <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when the effective voice chat state changes.

## Parameters
```c++
void onVoiceChatStateChange(boolean enabled, number range)
```

* `boolean` **enabled**: True when voice chat is available and enabled locally.
* `number` **range**: Server-configured proximity range in game units.
