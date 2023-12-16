---
description: S4 House Installation Document and Basic Concepts
---

# Installation

This installation guide covers both <mark style="color:red;">ESX</mark> and <mark style="color:blue;">QBCore</mark> frameworks.

## Required Resources

If you do not install all the necessary scripts, the script cannot run.

| Resource         | Download                                                  |
| ---------------- | --------------------------------------------------------- |
| screenshot-basic | [Download](https://github.com/citizenfx/screenshot-basic) |
| 0r-core          | [Download](https://github.com/0resmon/0r-core)            |
| qua\_adez\_hotel | It is given to you when you purchase it.                  |
| qua\_houses\_s4  | It is given to you when you purchase it.                  |

## Config.PhotoWebhook

Create a new webhook in Discord. And place the webhook link in the Config.PhotoWebHook section in config.lua.

```lua
Config.PhotoWebhook = "" -- Discord Webhook
```

### Supported Inventories

* qb-inventory
* qs-inventory
* ox\_inventory
* ps-inventory
* lj-inventory
* origen\_inventory
* ls-inventory
* core-inventory

### My Inventory Not in this list

In this case, you must enter the stash code of your own inventory into the <mark style="color:blue;">`Config.StashFunction`</mark> function in <mark style="color:blue;">config.lua.</mark>

#### For Example <mark style="color:red;">(chezza\_inventory)</mark>

```lua
Config.StashFunction = function(id, house)
  local HouseId = 0
  if Config.RealEstateJob then HouseId = house.dataid else HouseId = house.id end
  TriggerEvent('inventory:openInventory', {
    type = "stash",
    id = 'House'..HouseId,
    title 'House'..HouseId,
    weight = 100,  -- set to false for no weight
    delay = 0, -- open delay for the roleplays :)
    save = true -- save to database
})
end 
```

## server.cfg

```
--- main core ----
start screenshot-basic
start 0r-core
start s4-house 
start qua_adez_hotel
start qua_houses_s4
--- other resources ---
```

### Setup Database

And you must install the database sql. Select the sql file suitable for your infrastructure in the sql folder and install it in your database.

## Realestate

If you are going to use the real estate agent system, do not forget to add a profession called <mark style="color:blue;">"realestate".</mark>

## Final

Now you can start the server and use the script. Remember that it is opened with the <mark style="color:blue;">**/studio**</mark> command.

***

<details>

<summary>I cannot download YouTube videos. How do I solve it?</summary>

If YouTube videos are not downloading, you can find a solution by downloading an old version of ytdl-core. It will work more stable, but the videos will download late.

You can solve this problem by using the command below.

`npm i ytdl-core@4.9.1`

If you want to update ytdl-core again, you can use the code below. If a new ytdl-core is released, try it, it may work more stable.&#x20;

`npm i ytdl-core`

</details>



###



###
