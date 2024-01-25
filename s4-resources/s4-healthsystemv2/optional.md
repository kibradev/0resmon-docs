# Optional settings

## Revive 
If you have a custom ambulance job, you will need to change here.
```lua
Revive = function(playerId)
    if Config.Framework == "ESX" then 
        TriggerServerEvent('esx_ambulancejob:revive', playerId) -- change this for your ambulance revive event
    else 
        TriggerServerEvent('hospital:server:RevivePlayer', playerId)
    end
end
```

## Enable targeting 
```lua
Config.UseTarget = true -- if true will use target else will use closest player
```

## Open menu key
```lua
Config.Key = 'o' -- key to open menu
```

## Open hud key
```lua
Config.AlwaysOpenHudKey = 'u' -- key to open hud
```

