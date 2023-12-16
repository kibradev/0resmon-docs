---
description: BP Garage Installation Document and Basic Concepts
---

# 🧠 Installation

## Depencedies

{% hint style="danger" %}
In order for the script to run properly on your server, you must download the scripts below and install them on your server.
{% endhint %}



<table><thead><tr><th width="365">Resource</th><th>Download</th></tr></thead><tbody><tr><td>garage-map</td><td><a href="https://drive.google.com/file/d/1zM8Sj4P0fHkYOhy9KtMcMJNvyqYCbrX2/view?usp=sharing">https://drive.google.com/file/d/1zM8Sj4P0fHkYOhy9KtMcMJNvyqYCbrX2/view?usp=sharing</a></td></tr><tr><td>bp-garage-sql</td><td><a href="https://drive.google.com/file/d/1XO-M3dvf0qvgVyI-6W5vDqXUNwT0VIeH/view?usp=drive_link">https://drive.google.com/file/d/1XO-M3dvf0qvgVyI-6W5vDqXUNwT0VIeH/view?usp=drive_link</a></td></tr><tr><td>Bob74_ipl</td><td><a href="https://github.com/Bob74/bob74_ipl">https://github.com/Bob74/bob74_ipl</a></td></tr></tbody></table>

## Place your scripts

The order on server.cfg should be like this.

```
start bob74_ipl
start qua_houses_s4
start bp_garage
```

## Database Setup

{% hint style="info" %}
Check if there is a kibra-mechanics table already established in your database.

If it exists, delete it.
{% endhint %}

And now, enter this SQL code into your mysql database and set up the table.

```sql

CREATE TABLE IF NOT EXISTS `bp_garages` (
  `garageid` int(11) NOT NULL AUTO_INCREMENT,
  `garagetype` longtext DEFAULT NULL,
  `garageowner` longtext DEFAULT NULL,
  `garagemeta` longtext DEFAULT NULL,
  `garageimg` longtext DEFAULT NULL,
  `garagename` longtext DEFAULT NULL,
  `garageownername` longtext DEFAULT NULL,
  PRIMARY KEY (`garageid`)
) ENGINE=InnoDB AUTO_INCREMENT=131 DEFAULT CHARSET=utf8mb4;

```

## Installation Completed

{% hint style="success" %}
You have successfully completed the **bp-garage** installation. Restart your server to make sure everything is working.
{% endhint %}



