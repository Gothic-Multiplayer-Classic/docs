---
title: 'TOML'
---
```lua
local file = TOML.open("examples/settings.toml")

if file then
  print("Server: " .. file:get("server.name"))
  print("Slots: " .. tostring(file:getOr("server.slots", 32)))
  print("Public: " .. tostring(file:getOr("server.public", true)))
  print("Has password: " .. tostring(file:has("server.password")))

  local admins = file:get("server.admins")
  if admins then
    for _, name in ipairs(admins:entries()) do
      print("Admin: " .. name)
    end
  end

  local spawns = file:get("spawns")
  if spawns then
    for _, spawn in ipairs(spawns:entries()) do
      print(spawn:get("name") .. ": " .. spawn:get("world"))
    end
  end
else
  print("Could not open TOML file")
end
```
