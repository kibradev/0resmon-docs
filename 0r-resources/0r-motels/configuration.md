---
description: 0R Motels Configurations
---

# Configuration

## Custom Stash

If you use an inventory other than **ox**, **qbcore,** **qs inventories**, you can integrate the Stash Opening function suitable for your own inventory into this function.

```lua
Config.CustomStash = function(id)
    local other = {}
    other.maxweight = 10000 -- Custom weight stash.
    other.slots = 50 -- Custom slots spaces.
    TriggerServerEvent("inventory:server:OpenInventory", "stash", "Stash_"..id)
    TriggerEvent("inventory:client:SetCurrentStash", "Stash_"..id).
end
```

## Wardrobe Setting

You can use your own clothing system by integrating it into this function. Below is an example.

```lua
Config.OpenWardrobe = function()
    TriggerEvent('illenium-appearance:client:changeOutfit') -- for illenium-appearance
    --TriggerEvent('qb-clothing:client:openOutfitMenu') -- for qb-clothing
    -- TriggerEvent('ox_appearance:wardrobe') -- for ox_appearance
    -- TriggerEvent('ex_clothingstore:wardrobe') -- for bp_clothing v3
endPlace events, exports or functions that hide and open your border within these functions.
```

