---
description: Kibra Vehicleshops Configurations
---

# Configuration

## Adding a New Vehicleshops

```lua
{
    Type = "car",
    Owner = "",
    VehicleShopName = "",
    Money = 0,
    History = {},
    Employees = {},
    Vehicles = {},
    StockRequestFeeRate = 0,
    Discount = 0,
    RecentSales = {},
    RecentOrders = {},
    IncreasedSalesRate = 0,
    ShareofCarDeliverer = 0,
    Categories = {},
    Requests = {},
    -- Do not play with the above variables. You can make changes to the following variables. 
    Price = 5000000, -- VehicleShop purchase price.
    BlipShow = true,
    Blip = {Id = 227, Scale = 0.5, Color = 3, Display = 4}, 
    ExitVehicleSpawn = vector4(-33.62, -1080.69, 27.04, 70.3), -- After the vehicle is purchased, where it will spawn.
    CarSpawn = vector4(-47.6053, -1093.84, 26.422, 255.01), -- Coordinate where the vehicle that appears in the gallery was created.w
    Spawn = vector3(-42.4820, -1091.92, 26.422), -- Coordinate where the vehicle that appears in the gallery was created.
    PlayerSpawn = vector3(-47.6053, -1093.84, 26.422), -- Coordinate where the vehicle that appears in the gallery was created.
    ShopOpenCoord = vector3(-57.118858337402,-1097.2447509766,26.422357559204), -- Coordinate of the menu where the players can see the vehicles.
    BossMenuCoord = vector3(-32.083930969238,-1114.3852539063,26.422359466553), -- Location where the player can access the boss menu.
    VehicleDeliveryCoord = vector3(-18.44, -1103.87, 26.93), -- Coordinate where the player will deliver the car during a vehicle delivery.
    CardealerVehicles = {
        Spawn = vector3(-11.417442321777,-1102.2602539063,26.672048568726),
    }
},
```

Your code should be like above. Then, in the vehicleshop you copied, <mark style="color:blue;">ExitVehicleSpawn,</mark> <mark style="color:purple;">CarSpawn</mark>, <mark style="color:orange;">Spawn</mark>, The coordinates in the <mark style="color:red;">BossMenuCoord</mark> and <mark style="color:green;">CardealerVehicles</mark> sections are the places you need to change for your new vehicleshops

## Hide Hud

{% hint style="info" %}
Please note that these events may vary depending on the hud script you use.
{% endhint %}

```lua
Shared.CloseHud = function() -- When Vehicleshop opens, it hides your hud.
    TriggerEvent('wais:hudHide', true)
end

Shared.OpenHud = function() -- When Vehicleshop opens, it makes your hud visible.   
    TriggerEvent('wais:hudHide', false)
end
```

Place events, exports or functions that hide and open your border within these functions.

## Addon add a car

First, find the image of your addon tool in png format. And then drag this image to **kibra-vehicleshops/web/img.**

Next, open **kibra-vehicleshops/shared/main.lua**&#x20;

```lua
Shared.CustomCars = { -- Write the models of the vehicles you add as addon here.
    "redeye"
}
```

Next, write the model of the vehicle in this table.

<mark style="color:green;">**Remember:**</mark> The model name of the vehicle and the image extension name of the vehicle must be the same.
