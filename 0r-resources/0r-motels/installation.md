---
description: 0Resmon Motels Installation Document and Basic Concepts
---

# Installation

This installation guide covers both <mark style="color:red;">ESX</mark> and <mark style="color:blue;">QBCore</mark> frameworks.

## What is required for installation

* **0r\_lib** <mark style="color:blue;">(You can find it on your Keymaster.)</mark>
* **Map Files**

### Supported Inventories

* qb-inventory
* qs-inventory
* ox\_inventory
* ps-inventory
* lj-inventory
* origen\_inventory
* ls-inventory
* core-inventory

{% embed url="https://drive.google.com/file/d/1LpU9HW0qN2l-3KovzFHunm5YNTO44Nho/view?usp=sharing" %}

## Apartment System Installation

Apartment system, when players register to the server, they automatically start the server in the hotel room. To achieve this, we need to make a few changes.

First, change **Config.Apartment = true** in the config.lua file.

```lua
Config.Apartment = true
```

### esx\_multicharacter Setup

Open the <mark style="color:blue;">**esx\_multicharacter/client/main.lua**</mark> file and then, as you see in the photo, you should leave a space after line <mark style="color:blue;">**271**</mark> and place the triggerevent that allows giving a Random Room.

The code sample is available below the photo.

```lua
TriggerEvent('0R:Motels:Client:SetPlayerRandomRoom')
```

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

## qb-multicharacter Setup

{% hint style="danger" %}
First you must disable **qb-apartments.**
{% endhint %}

What you need to do here is; Open the <mark style="color:blue;">**qb-multicharacter/client/main.lua**</mark> file and find the <mark style="color:blue;">**qb-multicharacter:client:closeNUIdefault**</mark> event starting at <mark style="color:blue;">**line 100**</mark>. And update as below.&#x20;

**Code You Need to Add:**

```lua
if not exports["0r_motels"]:GetApartment() then
    SetEntityCoords(PlayerPedId(), Config.DefaultSpawn.x, Config.DefaultSpawn.y, Config.DefaultSpawn.z)
end
```

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

What we need to do in the same way here is; Open the <mark style="color:blue;">**qb-multicharacter/server/main.lua**</mark> file and find the <mark style="color:blue;">**qb-multicharacter:server:createCharacter**</mark> event starting at <mark style="color:blue;">**line 116**</mark> and add the following code with a space after <mark style="color:blue;">**line 124.**</mark>

```lua
if exports["0r_motels"]:GetApartment() then
    TriggerClientEvent('0R:Motels:Client:SetPlayerRandomRoom', src)
end
```

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

### Using a different multi-character?

If you are using a different multi-character, you need to place the event in the server or client event where the player is registered to integrate it. I leave a small explanation.

You must add this code to the new section of the player's character. Each multicharacter has a default spawn point. You must cancel these spawn points.&#x20;

```lua
if exports["0r_motels"]:GetApartment() then
    TriggerClientEvent('0R:Motels:Client:SetPlayerRandomRoom', src)
end
```

We have an export for this, `exports["0r_motels"]:GetApartment()`. Thanks to this export, you can check whether the Apartment system is active or not. If `Config.Apartment` is true, you must cancel the default spawn points of your multicharacter.

## Setup for Ox Inventory

Open the <mark style="color:blue;">**ox\_inventory/data/items.lua**</mark> file. And place the following code.

```lua
['motelcard'] = {
	label = 'Motel Card',
	weight = 200,
	stack = false
},

['doorlockpick'] = {
	label = 'Lockpick',
	weight = 200,
	stack = false
},
```

and now open the <mark style="color:blue;">**ox\_inventory/modules/items/client.lua**</mark> file and place the following code.

```lua
Item('motelcard', function(data, slot)
    TriggerEvent('0R:Motels:Client:OpenDoorNotTeleport', slot)
end)
```

## Setup for QS, LJ, Origen, PS, QB Inventories

The best thing about these inventories is that their infrastructure is qb-inventory. That's why the installations are the same.

Place these items in items.lua in your inventories. (qb-inventory to qb-core/shared/items.lua)

```lua
['motelcard'] = {['name'] = 'motelcard', ['label'] = 'Motel Card', ['weight'] = 500, ['type'] = 'item', ['image'] = 'motelcard.png', ['unique'] = true, ['useable'] = true, ['shouldClose'] = true, ['combinable'] = nil, ['description'] = 'Motel Card'},
```

Open your inventory javascript file. And search for the <mark style="color:blue;">**FormatItemInfo**</mark> function and place this code in the if loop within that function. There should be a <mark style="color:blue;">**metadata.js**</mark> file in <mark style="color:blue;">**qs-inventory**</mark>, do the same process there.

```javascript
} else if (itemData.name == "motelcard") {
    $(".item-info-title").html("<p>" + itemData.label + "</p>");
    $(".item-info-description").html(
        "<p><strong>Motel: </strong><span>" +
        itemData.info.motelname +
        "</span></p><p><strong>Room Id: </strong><span>" +
        itemData.info.roomid
);
```

## server.cfg

The server.cfg initialization order should be as follows.

{% hint style="danger" %}
If you are going to use an apartment system, pay attention to the server.cfg sequence. The motel system must be initialized before your multicharacter script.
{% endhint %}

### ESX

```
start es_extended
start 0r_lib
start 0r_motels
--- esx resources --
```

### QBCore

```
start qb-core
start 0r_lib
start 0r_motels
--- qbcore resources --
```

## What You Need to Know

***

<details>

<summary>Where is the sql  file ?</summary>

**There is no SQL File. The system automatically installs SQL into your database.**

</details>

<details>

<summary>How to add a motel room?</summary>

You can get information about this by watching this video.

[https://youtu.be/Wx-91KYJmvQ](https://youtu.be/Wx-91KYJmvQ)

</details>

<details>

<summary>How to create a motel?</summary>

You can get information about this by watching this video.

[https://youtu.be/\_bO\_Velqtpw](https://youtu.be/\_bO\_Velqtpw)

</details>



###



###
