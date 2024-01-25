# For sql esx


## esx legacy
```sql
INSERT INTO `items` (`name`, `label`, `weight`, `rare`, `can_remove`) VALUES ('bandageg', 'Bandage Gauze', '2', '0', '1');
INSERT INTO `items` (`name`, `label`, `weight`, `rare`, `can_remove`) VALUES ('forceps', 'Forceps', '1', '0', '1'), ('gauze', 'Gauze', '1', '0', '1'), ('iodine', 'Iodine', '1', '0', '1'), ('pill', 'Pill', '1', '0', '1'), ('surgical_gloves', 'Surgical gloves', '1', '0', '1'), ('surgical_staple', 'Surgical staple', '1', '0', '1'), ('surgical_tray', 'Surgical tray', '1', '0', '1'), ('syringe', 'Syringe', '1', '0', '1'), ('tape', 'Tape', '1', '0', '1');
```


## old custom esx 
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