---
description: 2NA Lockpick Installation Document and Basic Concepts
---

# Installation

## How to use ?

```lua
exports["2na_lockpick"]:createGame(Stage Quantity, Maximum Error)
```

## Example

```lua
local success = exports["2na_lockpick"]:createGame(3, 2)
if success then
    print("Lockpick is successful.")
else
    print("Lockpick failed.")
end 
```

