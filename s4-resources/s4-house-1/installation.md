---
description: S4 Report System V2 Installation Document and Basic Concepts
---

# Installation

This installation guide covers both <mark style="color:red;">ESX</mark> and <mark style="color:blue;">QBCore</mark> frameworks.

## Required Resources

If you do not install all the necessary scripts, the script cannot run.

| Resource    | Download                                                |
| ----------- | ------------------------------------------------------- |
| MugShotBase | [Download](https://github.com/BaziForYou/MugShotBase64) |
| s4-render   | [Download](https://github.com/cokluk/s4-render)         |

## Config.PhotoWebhook

Create a new webhook in Discord. And place the webhook link in the Config.WebHook section in config.lua.

```lua
Config.Webhook = "" -- Discord Webhook
```

## SQL File

```sql
CREATE TABLE `reports` (
    `id` int(11) NOT NULL,
    `owner` text NOT NULL,
    `text` text NOT NULL,
    `pid` int(11) NOT NULL DEFAULT current_timestamp(),
    `datetime` date NOT NULL DEFAULT current_timestamp(),
    `rname` text NOT NULL,
    `identifier` text NOT NULL,
    `rip` int(11) NOT NULL,
    `uniqueid` bigint(20) NOT NULL,
    `img` text NOT NULL,
    `extends` text NOT NULL DEFAULT `{   "status": "#ff004c" }`
  ) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;
  
  CREATE TABLE `reports_banlist` (
    `id` int(11) NOT NULL,
    `identifiers` text NOT NULL
  ) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;
  
  
  CREATE TABLE `reports_players` (
    `id` int(11) NOT NULL,
    `identifier` text NOT NULL,
    `points` int(11) NOT NULL
  ) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;
  
  
  CREATE TABLE `s4-hooks` (
    `pr` varchar(50) NOT NULL,
    `data` longtext DEFAULT NULL
  );
  
  ALTER TABLE `reports`
    ADD PRIMARY KEY (`id`);
  
  ALTER TABLE `reports_banlist`
    ADD PRIMARY KEY (`id`);
  
  ALTER TABLE `reports_players`
    ADD PRIMARY KEY (`id`);
  
  
  ALTER TABLE `reports`
    MODIFY `id` int(11) NOT NULL AUTO_INCREMENT;
  
  ALTER TABLE `reports_banlist`
    MODIFY `id` int(11) NOT NULL AUTO_INCREMENT;
  
  ALTER TABLE `reports_players`
    MODIFY `id` int(11) NOT NULL AUTO_INCREMENT;
  COMMIT;
  
```

## server.cfg

```
--- main core ----
start s4-render
start s4-reportsystemv2
start MugShotBase64
--- other resources ---
```
