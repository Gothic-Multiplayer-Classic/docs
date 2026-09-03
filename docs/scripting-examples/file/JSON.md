---
title: 'JSON'
---
```lua
local file = JSON.open("examples/settings.json")

if file then
  file:setItem("server", {
    name = "Gothic Multiplayer Server",
    public = true,
    slots = 100
  })

  file:setItem("admins", {
    "Player One",
    "Player Two"
  })

  print("Entries: " .. tostring(file:len()))

  local server = file:getItem("server")
  if server then
    print("Server: " .. server.name)
    print("Slots: " .. tostring(server.slots))
  end

  local admins = file:getItem("admins")
  if admins then
    for _, name in ipairs(admins) do
      print("Admin: " .. name)
    end
  end

  for index = 0, file:len() - 1 do
    print("Key: " .. file:key(index))
  end

  file:removeItem("admins")
else
  print("Could not open JSON file")
end
```
