---
title: 'SQLite'
---
```lua
local database, openError = SQLite.open({
  database = "examples/users.sqlite",
  busyTimeout = 5000,
  foreignKeys = true
})

if database then
  local result, queryError = database:execute([[
    CREATE TABLE IF NOT EXISTS users (
      id INTEGER PRIMARY KEY AUTOINCREMENT,
      username TEXT NOT NULL,
      email TEXT NOT NULL
    )
  ]])

  if result then
    print("Users table is ready")
  else
    print(queryError.message)
    print("Error ID: " .. tostring(queryError.code))
  end

  local insertResult, insertError = database:execute(
    "INSERT INTO users (username, email) VALUES (?, ?)",
    "Nameless",
    "nameless@example.com"
  )

  if insertResult then
    print("Inserted ID: " .. tostring(insertResult.lastInsertId))
  else
    print(insertError.message)
    print("Error ID: " .. tostring(insertError.code))
  end

  local selectResult, selectError = database:query(
    "SELECT id, username, email FROM users WHERE id >= ?",
    1
  )

  if selectResult then
    print("Rows: " .. tostring(#selectResult.rows))

    for _, row in ipairs(selectResult.rows) do
      print(tostring(row.id) .. " " .. row.username .. " " .. row.email)
    end
  else
    print(selectError.message)
    print("Error ID: " .. tostring(selectError.code))
  end

  database:close()
else
  print(openError.message)
  print("Error ID: " .. tostring(openError.code))
end
```
