# Lua Resource System
This document explains how Lua resources behave from the resource author's point of view. It focuses on the structure and lifecycle you can rely on, the guarantees the engine provides, and the mental model that makes resources predictable and easy to maintain - without requiring engine internals.

---

## What a Resource Is
A **resource** is a **versioned, self-contained Lua package** that lives on the server and is distributed to clients automatically. From the client's perspective, resources arrive as part of the connection flow: they are downloaded during the server handshake, verified for integrity, placed into an isolated Lua environment, and only then started explicitly by the engine.

The practical takeaway is simple: you never "install" or "load" resources manually on the client. You write code that assumes the resource will begin executing only when the engine starts it.

---

## Mandatory Structure
Every resource is a directory that contains a `resource.toml`. That file is what makes the directory recognizable as a resource.

!!! note
    If `resource.toml` is missing, the resource is not recognized and no script is executed.

A minimal valid layout looks like this:
```yaml
my_resource/
  resource.toml
  client/
    main.lua

my_resource_two/
  resource.toml
  server/
    main.lua
```

---

## `resource.toml`
`resource.toml` stores the resource metadata used for identification and validation. It describes the resource (version, author, description) and whether it should be active.

```toml
version = "1.0.0"
author = "YourName"
description = "Example resource"
active = true
```

---

## Folder Roles
A resource can contain client-only code, server-only code, and optionally shared modules used by both sides. A typical layout looks like this:
```yaml
my_resource/
  resource.toml
  client/
    main.lua
    ui.lua
    events.lua
  shared/
    init.lua
  server/
    main.lua
```

Conceptually, `client/` holds code that will only ever run on clients, `server/` holds code that will only ever run on the server, and `shared/` holds modules that are safe and useful on both sides. On the client, the engine loads only from `client/` and `shared/`, so server-only files are never part of the client execution surface.

---

## What the Client guarantees before Lua runs
When client-side Lua begins executing, it does so under strong guarantees. The client will not start running Lua until all resources are fully downloaded, all declared files exist, and integrity checks have passed. By the time Lua runs, the Lua environment is initialized and the engine bindings are already registered.

This is important because it eliminates partial or "half-loaded" states. If your client Lua is running, you can assume the resource is complete and the files it depends on are present. If something is missing or corrupted, the resource won't start in the first place.

---

## Single Client Entrypoint
Each client-side resource has exactly one automatic entrypoint: `client/main.lua`. Everything else is opt-in and must be loaded explicitly.

!!! note
    If code is not reachable from `client/main.lua`, it will never be executed.

In other words, the engine does not execute files based on file order or by scanning the directory. Only `client/main.lua` is started automatically, and any additional modules run only if `client/main.lua` requires them.

---

## The role of `client/main.lua`
Think of client/main.lua as a bootstrap rather than "the whole resource." Its job is to establish the resource's wiring: load modules, register event handlers, and set up lifecycle hooks. The heavy lifting typically lives in separate modules.

A common pattern looks like this:
```lua
require("shared.init")
require("client.events")
require("client.ui")

function onResourceStart()
end

function onResourceStop()
end
```

As a rule of thumb, avoid doing significant work at file top-level in `client/main.lua`. Treat top-level code as setup, and keep actual side effects and gameplay behavior inside lifecycle hooks and event handlers.

---

## Lifecycle Hooks
Resources can define lifecycle callbacks that the engine calls when the resource becomes active or stops:
```lua
function onResourceStart() end
function onResourceStop() end
```

!!! note
    Side effects belong in lifecycle hooks, not at file top level.

### onResourceStart
onResourceStart is called after the resource has been loaded and `client/main.lua` has executed. This is the point where the resource is considered live. This is where you typically register events, initialize UI, start timers, and create runtime state.

### onResourceStop
onResourceStop runs when the resource is being unloaded, replaced, or the client is disconnecting. Its purpose is cleanup. If you registered handlers, created UI, or started timers, this is where you should remove/destroy/stop them so the resource shuts down cleanly.

---

## `require()` Behavior
`require()` resolves modules from inside the resource package rather than the OS filesystem. For example:
```lua
require("client.ui")
```

This typically resolves to `client/ui.lua`, and may also resolve to shared modules depending on how paths are configured. The key behaviors to rely on are that modules load once per resource (they are cached), and a missing module prevents the resource from starting successfully.

---

## Lua Environment Isolation
Each resource runs in its own Lua environment. This prevents accidental cross-resource interference and makes resources behave like isolated packages.

!!! note
    Engine-provided globals remain accessible, but avoid globals as a cross-resource communication mechanism.

In practice, this means globals you define belong to that resource only, they persist for the lifetime of the resource, and they do not leak into other resources.

---

## Exports
Resources can optionally expose an explicit API surface through exports:
```lua
exports = {
  showUI = function() end
}
```

Exports are discovered after the resource starts. They are opt-in, they are not injected into global scope, and they represent the intentional interface other resources are allowed to depend on.

---

## Event-Driven Design
Client-side Lua should be designed as an event-driven system. Even though the resource starts in a well-defined way, the game world and gameplay state are not guaranteed to be "ready" at that exact moment. Player state may not exist yet, the world may initialize later, and visuals or UI systems may become available asynchronously.

A reliable client resource registers handlers and reacts to engine events. An unreliable one performs gameplay actions at file load or assumes the world is immediately available.

---

## Assets and Files
A resource only starts if all required files and assets are present. Missing assets are packaging errors rather than runtime concerns.

!!! note
    Assets are referenced by name and managed by the engine. Lua does not manually load assets.

Lua scripts are not expected to open files, load assets from disk, or access arbitrary paths. Instead, treat the resource as a sealed package: scripts reference known assets, and the engine handles the loading lifecycle.