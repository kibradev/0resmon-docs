---
description: Kibra Mechanics Installation Document and Basic Concepts
---

# Installation

## Depencedies

{% hint style="danger" %}
In order for the script to run properly on your server, you must download the scripts below and install them on your server.
{% endhint %}

<table><thead><tr><th width="365">Resource</th><th>Download</th></tr></thead><tbody><tr><td>oxmysql</td><td><a href="https://github.com/overextended/oxmysql">https://github.com/overextended/oxmysql</a></td></tr></tbody></table>

## Place your scripts

The order on server.cfg should be like this.

```editorconfig
start kibra-core
-- all
```

## And open the config.lua file and specify your infrastructure.

```lua
Shared.Framework = "ESX" -- or "QBCore "
```

## Installation Completed

{% hint style="success" %}
You have successfully completed the **kibra-mechanics** installation. Restart your server to make sure everything is working.
{% endhint %}



