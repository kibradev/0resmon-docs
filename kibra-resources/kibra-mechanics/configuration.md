---
description: Kibra Mechanics Configurations
---

# Configuration

## Adding a New Mechanics Business

```lua
Config.Mechanics = {
    {
        Owner = nil,
        Price = 100000,
        MechanicName = nil,
        DiscountRate = 0,
        JobName = "mechanic", -- If you are using the server's job system, enter the job name.
        VehicleSpawn = vector3(-356.51284790039,-119.94790649414,38.696281433105),
        TownTruckSpawnCoord = vector4(-366.07720947266,-111.69420623779,38.696643829346,110.70636749268),
        Customers = {},
        VehicleRepairAndCleaningLaborPrice = 1000, -- Vehicle Cleaning and Repair Fee || This is the labor price only. The price may increase depending on the damage of the vehicle.
        SalaryPerMod = 40, -- Percentage that employees will receive from their modification wages.
        Money = 0,
        Employees = {},
        CenterCoord = vector3(-339.3092956543,-137.1961517334,38.699272155762),
        BossMenuCoord = vector3(-347.41546630859,-133.4807434082,39.240417480469),
        BlipShow = true,
        Blip = {Id = 446, Scale = 1.0, Color = 2, Display = 4},
        ModifiedAreas = {
            {Coord = vector3(-338.6139831543,-137.64077758789,39.00968170166), Distance = 5.0},
            {Coord = vector3(490.57504272461,5590.2646484375,794.02239990234), Distance = 5.0}
        }
    },
}
```

Copy the code of the Mechanical business in the current table.

```lua
Config.Mechanics = {
    {
        Owner = nil,
        Price = 100000,
        MechanicName = nil,
        DiscountRate = 0,
        JobName = "mechanic", -- If you are using the server's job system, enter the job name.
        VehicleSpawn = vector3(-356.51284790039,-119.94790649414,38.696281433105),
        TownTruckSpawnCoord = vector4(-366.07720947266,-111.69420623779,38.696643829346,110.70636749268),
        Customers = {},
        VehicleRepairAndCleaningLaborPrice = 1000, -- Vehicle Cleaning and Repair Fee || This is the labor price only. The price may increase depending on the damage of the vehicle.
        SalaryPerMod = 40, -- Percentage that employees will receive from their modification wages.
        Money = 0,
        Employees = {},
        CenterCoord = vector3(-339.3092956543,-137.1961517334,38.699272155762),
        BossMenuCoord = vector3(-347.41546630859,-133.4807434082,39.240417480469),
        BlipShow = true,
        Blip = {Id = 446, Scale = 1.0, Color = 2, Display = 4},
        ModifiedAreas = {
            {Coord = vector3(-338.6139831543,-137.64077758789,39.00968170166), Distance = 5.0},
            {Coord = vector3(490.57504272461,5590.2646484375,794.02239990234), Distance = 5.0}
        }
    },

    {
        Owner = nil,
        Price = 100000,
        MechanicName = nil,
        DiscountRate = 0,
        JobName = "mechanic", -- If you are using the server's job system, enter the job name.
        VehicleSpawn = vector3(-356.51284790039,-119.94790649414,38.696281433105),
        TownTruckSpawnCoord = vector4(-366.07720947266,-111.69420623779,38.696643829346,110.70636749268),
        Customers = {},
        VehicleRepairAndCleaningLaborPrice = 1000, -- Vehicle Cleaning and Repair Fee || This is the labor price only. The price may increase depending on the damage of the vehicle.
        SalaryPerMod = 40, -- Percentage that employees will receive from their modification wages.
        Money = 0,
        Employees = {},
        CenterCoord = vector3(-339.3092956543,-137.1961517334,38.699272155762),
        BossMenuCoord = vector3(-347.41546630859,-133.4807434082,39.240417480469),
        BlipShow = true,
        Blip = {Id = 446, Scale = 1.0, Color = 2, Display = 4},
        ModifiedAreas = {
            {Coord = vector3(-338.6139831543,-137.64077758789,39.00968170166), Distance = 5.0},
            {Coord = vector3(490.57504272461,5590.2646484375,794.02239990234), Distance = 5.0}
        }
    },
}
```

Your code should be like above. Then, in the mechanic you copied, <mark style="color:blue;">JobName,</mark> <mark style="color:purple;">VehicleSpawn</mark>, <mark style="color:orange;">TownTruckSpawnCoord</mark>, <mark style="color:yellow;">CenterCoord</mark>, The coordinates in the <mark style="color:red;">BossMenuCoord</mark> and <mark style="color:green;">ModifiedAreas</mark> sections are the places you need to change for your new mechanic.

## Hiding the Border During Modification

{% hint style="info" %}
Please note that these events may vary depending on the hud script you use.
{% endhint %}

```lua
Config.HideHud = function()
    TriggerEvent("mHud:HideHud")
end

Config.OpenHud = function()
    TriggerEvent("mHud:ShowHud")
end
```

Place events, exports or functions that hide and open your border within these functions.

