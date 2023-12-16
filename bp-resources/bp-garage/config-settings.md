---
description: BP Garage Configurations
---

# 🪶 Config Settings

## Base Settings

```lua
Config.base = "ESX" --- QBCORE or "ESX"
```

Here you can change the base system to qb or esx.

```lua
Config.notifytype = "esxnotify"    --- esxnotify, costumnotify , qbnotify
```

You can specify 3 different announcement systems. The <mark style="color:blue;">**costumnotify**</mark> part goes to the config side below. You can edit this here according to your needs.

```lua
notifycustom = function (text, time)
    --  print('ss')
end
```

Enter the <mark style="color:orange;">discord webhook</mark> address here for the photo taking system in the Create menu to work.

{% code fullWidth="false" %}
```lua
Config.PhotoWebhook = "https://discord.com/api/webhooks/1097672293221670942/nWxiIpquVFOlVRT-ItXbt-Kk75trcFiqu0_JWyk6wyEcGfqKNIhx8uJGnGmNyPs8_H-A"
```
{% endcode %}

Automatic data extraction system

```lua
Config.getautodata = true  --- get autodata from for esx : owned_vehicles , qb : player_vehicles
```

## Drawtext System

{% hint style="info" %}
if you need use custom drawtext ui set false this settings.
{% endhint %}

```lua
Config.scriptdrawtext = true

customdrawtext = function(types, text)    ------ > This is an alternative to activate and deactivate using a custom drawtext UI.
    if types == "on" then 
    elseif types == "off" then 
    end
end
```

## General Garage Add

```lua
    ["centerpark"] = {   ----- uniqid
        ['label'] = "Center Park",
        ['coords'] = vector3(231.178024, -791.301086, 30.610962),
        ['markers'] = {['markertype'] = 36, ['markerlabel'] = "Center Park [E]" , ['markersize'] = {['x'] = 0.6, ['y'] = 0.6, ['z'] = 0.6}, ['markercolor'] = {['r'] = 247, ['g'] = 245, ['b'] = 255}},
        -- ['interiorsettings'] = {['isinterior'] = false , ['interiortype'] = "lowgarage" },
        ['blips'] = {['bliptype'] = 357, ['blipcolor'] = 3, ['blipscale'] = 0.7},
        ['maxvehicle'] = 25,                               -----------------------------------------------------  !attention if you change this you need to reset the allvehicles.json file.
        ['garagetype'] = {"vehicle", "motorcycle"},
        ['currentjob'] = {"all"}
    },
```

From here you can create a job or public garage.The value \["centerpark"] must be a completely unique name. If it is the same, it may be an error.

:warning: If you have run the script once, the max vehicles in **config.allgarages** will now be recorded. If you want to change this value to <mark style="color:green;">**\['maxvehicle'] = 15**</mark>. You need to reset allvehicles.json file. (you will make the inside like this. **\[]**)

<figure><img src="../../.gitbook/assets/Ekran Alıntısı.JPG" alt=""><figcaption></figcaption></figure>
