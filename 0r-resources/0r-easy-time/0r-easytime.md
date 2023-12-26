---
description: Config
---

# 0R Easytime

config.lua

```lua
Config = {}

---NOTE NOTE NOTE NOTE NOTE NOTE NOTE NOTE 
---/timer (managment menu)
---/area_tool (area creator)
---NOTE NOTE NOTE NOTE NOTE NOTE NOTE NOTE  

Config.CheckInsideZoneInterval = 15000

Config.ClothingTemperatureEffect = true

Config.TemperatureEffectInterval = 60000

Config.PerClothFeeling = 5

Config.RealTimeAlways = true

Config.ConvertFahrenheitToCelsius = true

Config.DegreeForWarmthBalance = 0  -- Greater than 0 indicates sweating, less than 0 indicates chilling.

Config.MinimumColdStartLevel = -20 

Config.MinimumPerspirationStartLevel = 2

Config.CriticalColdLevel = -50 

Config.CriticalPerspirationLevel = 50

Config.GiveDamage = true

Config.Damage = 5

Config.WarmthEffect = true

Config.WarmthNotifications = true

Config.WarmthEffectInterval = 15000

Config.ChangeTimeFadeEffectOnEnter = true  -- will only work for entrances to the zones. It won't work for exits
 
Config.ColdWeatherConditions = {
    "XMAS","HALLOWEEN","SNOWLIGHT","BLIZZARD","SNOW","THUNDER"
}

Config.PerspirationWeatherConditions = {
    "EXTRASUNNY","CLEAR" 
}

Config.ClothingFeelings = {
    Cold = { -- List of clothes you should not wear in cold weather
    --    [11] = {
    --        7
    --    }
    },
    Perspiration = {--A list of clothes you should not wear in hot weather
        [11] = {
            7
        }
    }
}

Config.ZoneList = {
    -- {
    --     name = "snow",
    --     coords = {
    --         vector2(2727.6, 91.7),
    --         vector2(798.7, 33.2),
    --         vector2(937.7, 6640.8),
    --         vector2(3418.6, 6136.8),
    --     },
    --     opts = {
    --         name="snow",
    --         minZ= 0.0,
    --         maxZ= 500.0,
    --         debugGrid=false,
    --         gridDivisions=25
    --     },
    --     time = {
    --         forceTime = true,
    --         hour = 22,
    --         minute = 22
    --     },
    --     weather = "XMAS"
    -- },
-- 	 {
--         name = "town",
--         coords = {
-- 		    vector2(-164.64788818359, 7524.8403320313),
--             vector2(921.96185302734, 6508.5952148438),
-- 			vector2(928.18237304688, 6465.5419921875),
--             vector2(-169.30432128906, 6468.0703125),
--         },
--         opts = {
--             name="town",
--             minZ= 0.0,
--             maxZ= 500.0,
--             debugGrid=true,
--             gridDivisions=25
--         },
--         time = {
--             forceTime = true,
--             hour = 12,
--             minute = 12
--         },
--         weather = "THUNDER"
--     },
	 
--     {
--        name = "half-map",
--        coords = {
--            vector2(68.472, 7616.768),
--            vector2(104.669, 1621.341),
--            vector2(-3248.069, 1514.634),
--            vector2(-2548.263, 7575.610),
--        },
--        opts = {
--            name="half-map",
--            minZ= 0.0,
--            maxZ= 500.0,
--            debugGrid=true,
--            gridDivisions=25
--        },
--        time = {
--            forceTime = true,
--            hour = 12,
--            minute = 12
--        },
--        weather = "BLIZZARD"
--    },
    
	    
-- {
--     name = "xmas",
--     coords = {
--         vector2(-1631.9451904297, -867.21942138672),
--         vector2(-1620.9650878906, -876.59680175781),
--         vector2(-1632.4249267578, -890.62127685547),
--         vector2(-1646.1198730469, -879.01684570313),
--     },
--     opts = {
--         name="xmas",
--         minZ= 0.0,
--         maxZ= 1500.0,
--         debugGrid=true,
--         gridDivisions=25
--     },
--     time = {
--         forceTime = true,
--         hour = 12,
--         minute = 12
--     },
--     weather = "XMAS"
-- }


{
    name = "thunder",
    coords = {
        vector2(-3359.073, 7325.764),
        vector2(5045.850, 7631.788),
        vector2(5185.811, 2109.306),
        vector2(-5112.210, 2153.691),
    },
    opts = {
        name="thunder",
        minZ= 0,
        maxZ= 700,
        debugGrid=false,
        gridDivisions=25
    },
    time = {
        forceTime = false,
        hour = 12,
        minute = 12
    },
    weather = "THUNDER"
},

{
    name = "extrasunny",
    coords = {
        vector2(5053.089, 1756.492),
        vector2(-4201.255, 1902.338),
        vector2(-4066.120, -3716.653),
        vector2(4498.069, -3683.471),
    },
    opts = {
        name="extrasunny",
        minZ= 0,
        maxZ= 700,
        debugGrid=false,
        gridDivisions=25
    },
    time = {
        forceTime = false,
        hour = 12,
        minute = 12
    },
    weather = "EXTRASUNNY"
}



 

}


Config.Translation = {
     ["sweating"] = "You're getting sweating",
     ["cold"] = "You're getting cold",
     ["hypothermia"] = "You're getting hypothermia",
     ["faint"] = "You'll faint from the heat.",

}
```

## sv\_config.lua

```lua
Config = {}
Config.TimeZoneUrl = "https://worldtimeapi.org/api/timezone/America/Los_Angeles"
Config.RealTimeUpdateInterval = 15000
Config.RealTimeAlways = true
Config.AdminList = {
    'steam:11000011b7c7b7c',
    'license:fd581068d91ab38fe0150add0df96e651c3b6d5c',  --license
	'steam:11000013f947b4e',
    'license:80877aca6164d3df0a469fe3c96f2524127ab052'
}
```
