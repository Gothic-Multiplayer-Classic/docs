---
title: 'setPlayerVisual'
---
# `function` setPlayerVisual <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the player/npc visual model and textures.

## Declaration
```cpp
void setPlayerVisual(number player_id, string bodyModel, number bodyTexture, string headModel, number headTexture, number teethTexture, number skinColor)
```

## Parameters
* `number` **player_id**: Target player id.
* `string` **bodyModel**: Body model name.
* `number` **bodyTexture**: Body texture index.
* `string` **headModel**: Head model name.
* `number` **headTexture**: Head texture index.
* `number` **teethTexture**: Optional teeth texture file numeric id. Defaults to 0 if omitted.
* `number` **skinColor**: Optional color variant of head & body texture files. Defaults to 0 if omitted.
