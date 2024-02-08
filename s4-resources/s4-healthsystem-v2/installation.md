---
description: S4 Health System V2 Installation Document and Basic Concepts
---

# Installation

## How To Install <a href="#how-to-install" id="how-to-install"></a>

First of all, leave the name of the script as it is, do not change it at all. Because this may cause the script not to work.

Script name should be: "s4-realisticdisease".

### Framework selection <a href="#framework-selection" id="framework-selection"></a>

Set the framework as the framework you use

```
Config.Framework = "ESX" -- ESX or QBCore
```

### Adding items <a href="#adding-items" id="adding-items"></a>

There are a total of 10 items in our script, 1 of which is usable.

Since we cannot adapt the items to every inventory and framework, you will need to add them.

But we have ready-made inventory item lists and sample sql file that we have provided you. If these are not suitable for your server, you will have to introduce the items to your server yourself.

* [For ox\_inventory item list (credit: boltzy)](https://docs.0resmon.com/HealthSystemV2/ox\_inventory/)
* [For qb\_inventory item list](https://docs.0resmon.com/HealthSystemV2/qb\_inventory/)
* [For esx\_legacy sql item list](https://docs.0resmon.com/HealthSystemV2/esx/)

| name             | label           | image                                                                                                                                         | usable |
| ---------------- | --------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| bandageg         | Bandage Gauzed  | [![](https://docs.0resmon.com/HealthSystemV2/assets/gauze.png)](https://docs.0resmon.com/HealthSystemV2/assets/gauze.png)                     | true   |
| forceps          | Forceps         | [![](https://docs.0resmon.com/HealthSystemV2/assets/forceps.png)](https://docs.0resmon.com/HealthSystemV2/assets/forceps.png)                 | false  |
| iodine           | Iodine          | [![](https://docs.0resmon.com/HealthSystemV2/assets/iodine.png)](https://docs.0resmon.com/HealthSystemV2/assets/iodine.png)                   | false  |
| scalpel          | Scalpel         | [![](https://docs.0resmon.com/HealthSystemV2/assets/scalpel.png)](https://docs.0resmon.com/HealthSystemV2/assets/scalpel.png)                 | false  |
| pill             | Pill            | [![](https://docs.0resmon.com/HealthSystemV2/assets/pill.png)](https://docs.0resmon.com/HealthSystemV2/assets/pill.png)                       | false  |
| surgical\_gloves | Surgical gloves | [![](https://docs.0resmon.com/HealthSystemV2/assets/surgical-gloves.png)](https://docs.0resmon.com/HealthSystemV2/assets/surgical-gloves.png) | false  |
| surgical\_staple | Surgical staple | [![](https://docs.0resmon.com/HealthSystemV2/assets/surgical-staple.png)](https://docs.0resmon.com/HealthSystemV2/assets/surgical-staple.png) | false  |
| surgical\_tray   | Surgical tray   | [![](https://docs.0resmon.com/HealthSystemV2/assets/surgical-tray.png)](https://docs.0resmon.com/HealthSystemV2/assets/surgical-tray.png)     | false  |
| syringe          | Syringe         | [![](https://docs.0resmon.com/HealthSystemV2/assets/syringe.png)](https://docs.0resmon.com/HealthSystemV2/assets/syringe.png)                 | false  |
| tape             | Tape            | [![](https://docs.0resmon.com/HealthSystemV2/assets/tape.png)](https://docs.0resmon.com/HealthSystemV2/assets/tape.png)                       | false  |
