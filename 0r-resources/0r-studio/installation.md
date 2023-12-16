---
description: 0Resmon Studio Installation Document and Basic Concepts
---

# Installation

This installation guide covers both <mark style="color:red;">ESX</mark> and <mark style="color:blue;">QBCore</mark> frameworks.

## Setup

**Don't forget to set your Framework in the **<mark style="color:green;">**config.lua**</mark>** file.**

First open cmd in folder part and write "**npm install**" if you dont want this download from here node\_modules folder and put in this folder.

{% embed url="https://github.com/0resmon/res-audio" %}

## Setup Step 1

Open the <mark style="color:blue;">**config.js**</mark> file for video downloads and audio recordings to work.

Type your server's IP address here.

```javascript
Config.Host = "127.0.0.1" // Replace Your IP
```

In order to record voice recordings, you must create TCP and UDP ports inbound and outbound.

The port number must be a number you specify or 48080.

{% embed url="https://www.youtube.com/watch?v=2AcqibSJ8ng" %}

After moving the script to the resources folder, open your **server.cfg** file and position it as follows.

```
--- main core ----
start res-audio
--- other resources ---
```

And now let's create our database tables.

```sql
CREATE TABLE `res-audio` (
  `id` int(11) NOT NULL,
  `owner` text NOT NULL,
  `url` text NOT NULL,
  `name` text NOT NULL,
  `cat` int(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;

CREATE TABLE `res-audio-profile` (
  `id` int(11) NOT NULL,
  `owner` text NOT NULL,
  `name` text NOT NULL,
  `url` text NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;

CREATE TABLE `res-spotify` (
  `id` int(11) NOT NULL,
  `owner` text NOT NULL,
  `name` text NOT NULL,
  `img` text NOT NULL,
  `url` longtext NOT NULL,
  `cur_mahlas` text NOT NULL,
  `cur_avatar` text NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;

ALTER TABLE `res-audio`
  ADD PRIMARY KEY (`id`);

ALTER TABLE `res-audio-profile`
  ADD PRIMARY KEY (`id`);

ALTER TABLE `res-spotify`
  ADD PRIMARY KEY (`id`);

ALTER TABLE `res-audio`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT;

ALTER TABLE `res-audio-profile`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT;
  
ALTER TABLE `res-spotify`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT;
COMMIT;
```

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
