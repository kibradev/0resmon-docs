---
description: Kibra Vehicleshops Installation Document and Basic Concepts
---

# Installation

## Depencedies

{% hint style="danger" %}
In order for the script to run properly on your server, you must download the scripts below and install them on your server.
{% endhint %}

<table><thead><tr><th width="365">Resource</th><th>Download</th></tr></thead><tbody><tr><td>kibra-core</td><td><a href="https://github.com/kibradev/kibra-core">https://github.com/kibradev/kibra-core</a></td></tr></tbody></table>

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
start kibra-vehicleshops
```

## Database Setup

{% hint style="info" %}
Check if there is a kibra-mechanics table already established in your database.

If it exists, delete it.
{% endhint %}

And now, enter this SQL code into your mysql database and set up the table.

```sql
CREATE TABLE `kibra-vehicleshops` (
  `id` int(11) NOT NULL,
  `info` text NOT NULL DEFAULT '[]',
  `employees` text NOT NULL DEFAULT '[]',
  `vehicles` text NOT NULL DEFAULT '[]',
  `history` text NOT NULL DEFAULT '[]',
  `requests` text NOT NULL DEFAULT '[]',
  `categories` text NOT NULL DEFAULT '[]',
  `recentsales` text NOT NULL DEFAULT '[]',
  `recentorders` text NOT NULL DEFAULT '[]'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

ALTER TABLE `kibra-vehicleshops`
  ADD PRIMARY KEY (`id`);

ALTER TABLE `kibra-vehicleshops`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=6;
COMMIT;

ALTER TABLE owned_vehicles
ADD COLUMN model VARCHAR(255);
```

## Installation Completed

{% hint style="success" %}
You have successfully completed the **kibra-vehicleshops** installation. Restart your server to make sure everything is working.
{% endhint %}



