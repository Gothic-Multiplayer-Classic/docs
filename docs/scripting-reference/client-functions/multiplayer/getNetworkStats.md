---
title: 'getNetworkStats'
---
# `function` getNetworkStats <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    Packet loss fields are ratios from 0.0 to 1.0.
!!! note
    Send buffer fields aggregate low, medium, and high priority packets.

This function will return client network statistics.

## Declaration
```cpp
{packetReceived, packetlossTotal, packetlossLastSecond, messagesInResendBuffer, messageInSendBuffer, bytesInResendBuffer, bytesInSendBuffer} getNetworkStats()
```

## Parameters
No parameters.
  
## Returns `{packetReceived, packetlossTotal, packetlossLastSecond, messagesInResendBuffer, messageInSendBuffer, bytesInResendBuffer, bytesInSendBuffer}`
Table containing current network statistics.
