---
description: You need to add the items listed here to your server.
---

# Required Items

{% tabs %}
{% tab title="ESX" %}
**For ESX Default**

```sql
INSERT INTO `items` (`name`, `label`, `weight`, `rare`, `can_remove`, `type`, `unique`, `description`, `image`, `shouldClose`, `combinable`, `id`) VALUES ('forceps', 'forceps', '0.01', '0', '1', 'item', 'false', 'Bilinmiyor', 'forceps.png', '0', NULL, NULL);
INSERT INTO `items` (`name`, `label`, `weight`, `rare`, `can_remove`, `type`, `unique`, `description`, `image`, `shouldClose`, `combinable`, `id`) VALUES ('gauze', 'gauze', '0.01', '0', '1', 'item', 'false', 'Bilinmiyor', 'gauze.png', '0', NULL, NULL);
INSERT INTO `items` (`name`, `label`, `weight`, `rare`, `can_remove`, `type`, `unique`, `description`, `image`, `shouldClose`, `combinable`, `id`) VALUES ('iodine', 'iodine', '0.01', '0', '1', 'item', 'false', 'Bilinmiyor', 'iodine.png', '0', NULL, NULL);
INSERT INTO `items` (`name`, `label`, `weight`, `rare`, `can_remove`, `type`, `unique`, `description`, `image`, `shouldClose`, `combinable`, `id`) VALUES ('pill', 'pill', '0.01', '0', '1', 'item', 'false', 'Bilinmiyor', 'pill.png', '0', NULL, NULL);
INSERT INTO `items` (`name`, `label`, `weight`, `rare`, `can_remove`, `type`, `unique`, `description`, `image`, `shouldClose`, `combinable`, `id`) VALUES ('surgical_gloves', 'surgical_gloves', '0.01', '0', '1', 'item', 'false', 'Bilinmiyor', 'surgical_gloves.png', '0', NULL, NULL);
INSERT INTO `items` (`name`, `label`, `weight`, `rare`, `can_remove`, `type`, `unique`, `description`, `image`, `shouldClose`, `combinable`, `id`) VALUES ('surgical_staple', 'surgical_staple', '0.01', '0', '1', 'item', 'false', 'Bilinmiyor', 'surgical_staple.png', '0', NULL, NULL);
INSERT INTO `items` (`name`, `label`, `weight`, `rare`, `can_remove`, `type`, `unique`, `description`, `image`, `shouldClose`, `combinable`, `id`) VALUES ('surgical_tray', 'surgical_tray', '0.01', '0', '1', 'item', 'false', 'Bilinmiyor', 'surgical_tray.png', '0', NULL, NULL);
INSERT INTO `items` (`name`, `label`, `weight`, `rare`, `can_remove`, `type`, `unique`, `description`, `image`, `shouldClose`, `combinable`, `id`) VALUES ('syringe', 'syringe', '0.01', '0', '1', 'item', 'false', 'Bilinmiyor', 'syringe.png', '0', NULL, NULL);
INSERT INTO `items` (`name`, `label`, `weight`, `rare`, `can_remove`, `type`, `unique`, `description`, `image`, `shouldClose`, `combinable`, `id`) VALUES ('tape', 'tape', '0.01', '0', '1', 'item', 'false', 'Bilinmiyor', 'tape.png', '0', NULL, NULL);
```

**For ESX Legacy**

```sql
INSERT INTO `items` (`name`, `label`, `weight`, `rare`, `can_remove`) VALUES ('bandageg', 'Bandage Gauze', '2', '0', '1');
INSERT INTO `items` (`name`, `label`, `weight`, `rare`, `can_remove`) VALUES ('forceps', 'Forceps', '1', '0', '1'), ('gauze', 'Gauze', '1', '0', '1'), ('iodine', 'Iodine', '1', '0', '1'), ('pill', 'Pill', '1', '0', '1'), ('surgical_gloves', 'Surgical gloves', '1', '0', '1'), ('surgical_staple', 'Surgical staple', '1', '0', '1'), ('surgical_tray', 'Surgical tray', '1', '0', '1'), ('syringe', 'Syringe', '1', '0', '1'), ('tape', 'Tape', '1', '0', '1');
```
{% endtab %}

{% tab title="QBCore" %}
For QBCore Inventory

```lua
bandageg = { name = 'bandageg', label = 'Bandage', weight = 500, type = 'item', image = 'bandageg.png', unique = false, useable = true, shouldClose = true, combinable = nil, description = 'edit here' },
gauze = { name = 'gauze', label = 'Gauze', weight = 500, type = 'item', image = 'gauze.png', unique = false, useable = false, shouldClose = true, combinable = nil, description = 'edit here' },
tape = { name = 'tape', label = 'Tape', weight = 500, type = 'item', image = 'tape.png', unique = false, useable = false, shouldClose = true, combinable = nil, description = 'edit here' },
surgical_tray = { name = 'surgical_tray', label = 'Surgical tray', weight = 500, type = 'item', image = 'surgical_tray.png', unique = false, useable = false, shouldClose = true, combinable = nil, description = 'edit here' },
iodine = { name = 'iodine', label = 'Iodine', weight = 500, type = 'item', image = 'iodine.png', unique = false, useable = false, shouldClose = true, combinable = nil, description = 'edit here' },
syringe = { name = 'syringe', label = 'Syringe', weight = 500, type = 'item', image = 'syringe.png', unique = false, useable = false, shouldClose = true, combinable = nil, description = 'edit here' },
forceps = { name = 'forceps', label = 'Forceps', weight = 500, type = 'item', image = 'forceps.png', unique = false, useable = false, shouldClose = true, combinable = nil, description = 'edit here' },
pill = { name = 'pill', label = 'Pill', weight = 500, type = 'item', image = 'pill.png', unique = false, useable = false, shouldClose = true, combinable = nil, description = 'edit here' },
surgical_gloves = { name = 'surgical_gloves', label = 'Surgical gloves', weight = 500, type = 'item', image = 'surgical_gloves.png', unique = false, useable = false, shouldClose = true, combinable = nil, description = 'edit here' },
surgical_staple = { name = 'surgical_staple', label = 'Surgical staple', weight = 500, type = 'item', image = 'surgical_staple.png', unique = false, useable = false, shouldClose = true, combinable = nil, description = 'edit here' },
```
{% endtab %}
{% endtabs %}

**Ox Inventory**

```lua
['forceps'] = {
    label = 'forceps',
    description = "",
    weight = 30,
    stack = true
},
['gauze'] = {
    label = 'gauze',
    description = "",
    weight = 30,
    stack = true
},
['iodine'] = {
    label = 'iodine',
    description = "",
    weight = 30,
    stack = true
},
['bandageg'] = {
    label = 'Bandage',
    description = "Stops Bleeding",
    weight = 30,
    stack = true
},
['pill'] = {
    label = 'pill',
    description = "",
    weight = 30,
    stack = true
},
['surgical-gloves'] = {
    label = 'surgical gloves',
    description = "",
    weight = 30,
    stack = true
},
['surgical-staple'] = {
    label = 'surgical staple',
    description = "",
    weight = 30,
    stack = true
},
['surgical-tray'] = {
    label = 'surgical tray',
    description = "",
    weight = 30,
    stack = true
},
['syringe'] = {
    label = 'Syringe',
    description = "",
    weight = 30,
    stack = true
},
['tape'] = {
    label = 'Tape',
    description = "",
    weight = 30,
    stack = true
},

```
