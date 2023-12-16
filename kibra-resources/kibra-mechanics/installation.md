---
description: Kibra Mechanics Installation Document and Basic Concepts
---

# Installation

## Depencedies

{% hint style="danger" %}
In order for the script to run properly on your server, you must download the scripts below and install them on your server.
{% endhint %}

<table><thead><tr><th width="365">Resource</th><th>Download</th></tr></thead><tbody><tr><td>kibra-core</td><td><a href="https://github.com/kibradev/kibra-core">https://github.com/kibradev/kibra-core</a></td></tr><tr><td>kibra-mechanics-flatbed</td><td><a href="https://github.com/kibradev/kibra-mechanics-flatbed3">https://github.com/kibradev/kibra-mechanics-flatbed3</a></td></tr></tbody></table>

{% hint style="warning" %}
Before continuing with the instructions, you should also read and follow the instructions in the kibra-core documentation.
{% endhint %}

{% content-ref url="../kibra-core/" %}
[kibra-core](../kibra-core/)
{% endcontent-ref %}

## Place your scripts

The order on server.cfg should be like this.

```
start kibra-core
start kibra-mechanics
start kibra-mechanics-flatbed3
```

## Database Setup

{% hint style="info" %}
Check if there is a kibra-mechanics table already established in your database.

If it exists, delete it.
{% endhint %}

And now, enter this SQL code into your mysql database and set up the table.

```sql
CREATE TABLE IF NOT EXISTS `kibra-mechanics` (
  `id` int(11) NOT NULL,
  `name` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL,
  `owner` varchar(46) DEFAULT NULL,
  `employees` text CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT '[]',
  `money` float NOT NULL,
  `wage` float NOT NULL,
  `discountrate` float NOT NULL,
  `customers` text NOT NULL DEFAULT '[]',
  `repairfee` float NOT NULL DEFAULT 0,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM DEFAULT CHARSET=utf8mb4;
```

## Installation Completed

{% hint style="success" %}
You have successfully completed the **kibra-mechanics** installation. Restart your server to make sure everything is working.
{% endhint %}



