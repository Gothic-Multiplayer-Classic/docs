---
title: 'MySQL'
---
```lua
local database, openError = MySQL.open({
  host = "127.0.0.1",
  port = 3306,
  database = "gmp",
  username = "root",
  password = "",
  charset = "utf8mb4"
})

if database then
  local result, queryError = database:query(
    "SELECT id, username, email FROM users WHERE id >= ?",
    1
  )

  if result then
    print("Rows: " .. tostring(#result.rows))
    print("Columns: " .. tostring(#result.columns))

    for _, row in ipairs(result.rows) do
      print(tostring(row.id) .. " " .. row.username .. " " .. row.email)
    end
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
    print("Affected rows: " .. tostring(insertResult.affectedRows))
  else
    print(insertError.message)
    print("Error ID: " .. tostring(insertError.code))
  end

  database:close()
else
  print(openError.message)
  print("Error ID: " .. tostring(openError.code))
end
```
