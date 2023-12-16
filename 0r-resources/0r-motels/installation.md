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

**This installation guide is for **<mark style="color:green;">**ESX**</mark> **and **<mark style="color:green;">**QBCore.**</mark>

## Required Resources

* 0r\_lib <mark style="color:blue;">(on your keymaster)</mark>
* Motel Map Files&#x20;

{% embed url="https://drive.google.com/file/d/1LpU9HW0qN2l-3KovzFHunm5YNTO44Nho/view?usp=sharing" %}

### Supported Inventories

* ox\_inventory&#x20;
* ps-inventory
* ls-inventory
* qs-inventory
* core-inventory
* lj-inventory
* origen\_inventory
* qb-inventory

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

```
----- your core ----
start [motelmaps]
start 0r_lib
start 0r_motels
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
