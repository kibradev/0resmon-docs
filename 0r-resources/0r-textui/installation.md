---
description: 0R Text UI Installation Document
---

# Installation

## How to use ?


## Creating Normal Zone (Only Client)
```lua
Put this on top of your client side and you don't need to do anything else. This is for classic cordinates

CreateThread(function()
    exports['0r-textui']:AddClassic(vector3(x, y, z), 'Key (E)', 'Text (Talk with Trevor)', distance: 2.5)
end)

Also you can add for peds on cfg.lua, but you should know this script is creating peds by own!
```
