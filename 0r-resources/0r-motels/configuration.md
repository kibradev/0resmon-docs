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

## Config.lua

```lua
Config = {}

Config.Motels = {}

Config.Locale = 'en' -- "tr" "pt" "de" "es" "en", "french"

Config.Corridor = {
    Coord = -- Corridor Coord,
    SecondFloor = -- Second Floor Coord,
    Colors = {
        {name = 'marble', price = 0, default = true},
        {name = 'blue', price = 600, default = false},
        {name = 'orange', price = 1000, default = false},
        {name = 'red', price = 500, default = false},
        {name = 'normal', price = 500, default = false},
    }
}

Config.Apartment = false
-- If you activate this setting, the player will be allocated a hotel room when registering to the server.

-- This information allows the player to be given a motel room when they first enter the server. Here is the motel room information:
Config.RandomMotelRoomData = { 
    mCode = 'ksmOsx',
    Day = 2,
}

Config.Blip = {
    Id = 475,
    Scale = 0.8
}
-- Blip Settings

Config.CustomShowerSystem = false
-- If you want to your shower system, you should open config_functions.lua than you should edit it.

Config.MetaDataSystem = false
-- Metadata System If True, you must have an inventory with metadata. Because the system will work with a unique motel key.

Config.MotelGarages = true 
-- Motel Garages Bool

Config.TargetedRevenueValue = 150000 
-- The maximum income value that can appear in the Boss Menu.

Config.GarageVehiclesLock = true
-- It ensures that the vehicles in the garage are locked.

Config.AutoLock = true 
-- If true, the doors will automatically close.

Config.KeysListCommand = 'mykeys'
-- This feature will only work if Config.MetaDataSystem is turned off. It allows you to give your room keys to other players.

Config.KeyPrices = {
    ChangeKeyPrice = 100, -- Player Motel Key Change Price
    CopyKeyPrice = 100 -- Player Motel Key Copy Price
}

Config.CustomNotify = false -- If you have a Notify that you use, you can place it in the function below.

Config.LockPickSystemOxSkillbar = true
-- If this is checked true you will need to run ox_lib on your server.
-- But if you do not want to use ox_lib, you can integrate a skillbar of your own choice or use into the function below.

Config.ShowerCoords = { -- Locations where players can shower in their rooms.
    -- Shower Coords,
}

Config.GarageCoord = vec3(519.9156, -2639.1565, -38.6916) -- Garage Entrance Coordinate.
Config.GarageElevator = vec3(532.0820, -2637.8948, -38.6916) -- Garage Elevator Coordinate.

Config.GaragePos = { -- Coordinates of vehicles in the garage.
    vec4(0,0,0),
    -- other garageposcoords --
}

Config.MotelCardItem = 'motelcard' 
-- Motel Card Item Name || If Config.MetaDataSystem true

Config.DoorLockPickItem = 'doorlockpick' 
-- This doorlockpick item allows players to enter rooms.

Config.StashInfo = {
    Weight = 40,
    StashWeightPrice = 50, -- 1kg
    StashWeightMaxValue = 100 -- kg
}

Config.RoomTypes = {
    {
        RoomLabel = "Double",
        Image = 'roomplus.png',
        Url = 'Double',

        Coords = {
            Stash = vec3(0,0,0),
            Exit = vec4(0,0,0),
            Wardrobe = vec3(0,0,0)
        },

        EditRoomMenu = vec3(0,0,0),

        Teleport = true,
        Colors = {
            {name = 'marble', price = 0, default = true},
            {name = 'blue', price = 600, default = false},
            {name = 'orange', price = 1000, default = false},
            {name = 'red', price = 500, default = false},
            {name = 'normal', price = 500, default = false},
        },

        Description = 'Big, Double Room, Bedroom and Lux Toilet',
        DetailDescription = 'Modern Comfort: 2-Storey Motel Room Warm welcome and spacious design. Large living area and kitchen on the ground floor. Comfy bed and private bathroom upstairs. We are here for your unforgettable stay!'
    },

    {
        RoomLabel = "Modern",
        Image = 'modern.png',
        Url = 'modern',

        Coords = {
            Stash = vec3(0,0,0),
            Exit = vec4(0,0,0),
            Wardrobe = vec3(0,0,0)
        },

        EditRoomMenu = vec3(0,0,0),

        Teleport = true,

        Colors = {
            {name = 'turuncu', price = 0, default = true},
            {name = 'kirmizi', price = 600, default = false},
            {name = 'mor', price = 1000, default = false},
        },

        Description = 'Big, Modern Room, Bedroom and Lux Toilet',
        DetailDescription = 'Modern Comfort: 2-Storey Motel Room Warm welcome and spacious design. Large living area and kitchen on the ground floor. Comfy bed and private bathroom upstairs. We are here for your unforgettable stay!'
    },

    {
        RoomLabel = "Modern Plus",
        Image = 'modernplus.png',
        Url = 'modernplus',

        Coords = {
            Stash = vec3(0,0,0),
            Exit = vec4(0,0,0),
            Wardrobe = vec3(0,0,0)
        },

        EditRoomMenu = vec3(0,0,0),

        Teleport = true,

        Colors = {
            {name = 'turuncu', price = 0, default = true},
            {name = 'kirmizi', price = 600, default = false},
            {name = 'mor', price = 1000, default = false},
        },

        Description = 'Big, Modern Plus Room, Bedroom and Lux Toilet',
        DetailDescription = 'Modern Comfort Plus: 2-Storey Motel Room Warm welcome and spacious design. Large living area and kitchen on the ground floor. Comfy bed and private bathroom upstairs. We are here for your unforgettable stay!'
    },

    {
        RoomLabel = 'Standard',
        Image = 'roomtype1int4.png',

        Coords = {
            Stash = vec3(0,0,0),
            Exit = vec4(0,0,0),
            Wardrobe = vec3(0,0,0)
        },
        
        Teleport = true,
        Colors = false,

        EditRoomMenu = vector3(1,1,1),

        Description = 'Standard Room',
        DetailDescription = 'Comfortable and Simple: Standard Motel Room Welcome! A comfortable bed and basic furniture await you in our simple and comfortable standard room. The modern bathroom offers freshness and comfort.'
    },

    {
        RoomLabel = 'Simple',
        Image = 'roomtype1int6.png',
        Teleport = true,
        Colors = false,

        EditRoomMenu = vector3(1,1,1),
        Coords = {
            Stash = vec3(0,0,0),
            Exit = vec4(0,0,0),
            Wardrobe = vec3(0,0,0)
        },

        Description = 'Simple Room',
        DetailDescription = "Welcome to our cozy, simple room. It's designed for your comfort and convenience. You'll find a comfortable bed, a clean, functional bathroom, and a small sitting area. While it's not extravagant, it has everything you need for a peaceful and relaxing stay."
    },
    
    -- for pinkcage motel 

    -- {
    --     RoomLabel = 'Classic',
    --     Image = 'roomtype1int.png',
    --     Teleport = false,
    --     Colors = false,
    --     EditRoomMenu = false,
    --     Description = 'Classic Room',
    --     DetailDescription = 'Comfortable and Simple: Classic Motel Room Welcome! A comfortable bed and basic furniture await you in our simple and comfortable standard room. The modern bathroom offers freshness and comfort.'
    -- },

    {
        RoomLabel = 'Rustic',
        Image = 'roomtype1int5.png',
        Teleport = false,
        Colors = false,
        EditRoomMenu = false,
        Description = 'Rustic Room',
        DetailDescription = 'Rustic Motel Room: Comfort & Simplicity Experience simplicity and comfort in our rustic motel room. Enjoy a cozy bed, basic furniture, and a modern bathroom for your stay.'
    },

    {
        RoomLabel = 'Economy',
        Image = 'roomtype1int7.png',
        Teleport = false,
        Colors = false,
        EditRoomMenu = false,
        Description = 'Economy Room',
        DetailDescription = "Our economy room offers a budget-friendly stay with essential amenities. It's a comfortable and practical choice for travelers looking to save without sacrificing comfort."
    },

    {
        RoomLabel = 'Normal',
        Image = 'roomtype1int9.png',
        Teleport = false,
        Colors = false,
        EditRoomMenu = false,
        Description = 'Normal Room',
        DetailDescription = "Our normal room room offers a budget-friendly stay with essential amenities. It's a comfortable and practical choice for travelers looking to save without sacrificing comfort."
    },

    {
        RoomLabel = 'Modest',
        Image = 'roomtype1int10.png',
        Teleport = false,
        Colors = false,
        EditRoomMenu = false,
        Description = 'Modest Room',
        DetailDescription = "In a modest motel room, warm-colored walls and simple, comfortable furnishings offer a tranquil and unpretentious lodging experience. Equipped with all necessary amenities, it provides an ideal space to relax and enjoy the journey."
    },

    {
        RoomLabel = 'Modest VIP',
        Image = 'roomtype1int11.png',
        Teleport = false,
        Colors = false,
        EditRoomMenu = false,
        Description = 'Modest VIP Room',
        DetailDescription = "In a modest motel room, warm-colored walls and simple, comfortable furnishings offer a tranquil and unpretentious lodging experience. Equipped with all necessary amenities, it provides an ideal space to relax and enjoy the journey."
    }
}

Config.DueDate = 3
-- The number of days entered into this variable ensures that the player's room will be canceled if he does not pay the room rent within the specified day.

Config.MotelAdminMenuAccessible = { -- Enter the license IDs of the players you want to be able to access the /moteladmin menu here.
    "license:0Resmon",
}

Config.Keys = {
    ["reception"] = {"E", 38, "Reception"}
}

Config.CreateMotelEditorKeys = {
    ["reception"] = {"E", 38, "Reception"},
    ["room"] = {"E", 38}
}

Config.MotelAdminMenuCommand = 'moteladmin' -- Motel Admin Menu Open Command
```

## Config Functions

```lua
Config.CustomStash = function(id)
    -- You can add the stash function of the inventory you are using here.
end

Config.OpenWardrobe = function()
    -- TriggerEvent('illenium-appearance:client:openOutfitMenu') -- for illenium-appearance
    --TriggerEvent('qb-clothing:client:openOutfitMenu') -- for qb-clothing
    TriggerEvent('ox_appearance:wardrobe') -- for ox_appearance
    -- TriggerEvent('ex_clothingstore:wardrobe') -- for bp_clothing v3
end

Config.CustomLockPickSystem = function() -- if Config.LockPickSystem is work for false 
    return exports["2na_lockpick"]:createGame(3, 1)
end

Config.TakeAShower = function()
    -- Custom Functions
end

Config.CustomNotifyFunc = function(title, text, type)
    exports['okokNotify']:Alert(title, text, 3000, type)
end
```
