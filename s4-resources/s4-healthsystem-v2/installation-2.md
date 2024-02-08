---
description: Bleeding Adjustment Instructions
---

# Bleeding Adjustment

## Bleeding adjustment <a href="#bleeding-adjustment" id="bleeding-adjustment"></a>

Bleeding setting allows you to set the bleeding feature available in the script.

Adjust this setting to activate or deactivate bleeding.

```lua
Config.EnableBleeding = true -- if true will enable bleeding
```

`Config.BleedingPerMillisecond` This setting determines how many times every second `Config.BleedingHitDamage` will damage the player

Also `Config.BleedingMultiplier` is a multiplier setting that determines how many x damage you will take

```lua
Config.BleedingHitDamage = 1 -- how many times player can bleed 

Config.BleedingPerMillisecond = 2500 -- how many seconds player will bleed

Config.BleedingMultiplier = 1 -- how many times player will bleed
```

When you activate this setting, the player will take damage but will continue to regenerate health. With a balanced setting, you can never get the player killed even if they take damage.

```lua
Config.DisableSetPlayerHealthRecharge = false -- if true will disable recharge player health
```

Self-healing feature This feature allows the player to cure their own bleeding for a certain period of time. Stops bleeding. When you use this item, the player will stop bleeding for a certain number of seconds in `Config.StopBleedingTime`. However, if the player takes damage, the player will need to use this item again to treat the wounds.

```lua
Config.ItemSelfTreatment = "bandageg" -- item name for self treatment

Config.StopBleedingTime = 1 -- minutes
```
