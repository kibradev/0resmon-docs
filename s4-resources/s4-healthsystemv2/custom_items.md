# How To Add Custom Items

If you want to add a special item and specify which wound areas this item can be used in, you need to read this document.
You do not have to do this.


For example, define an item in your inventory. it can be any item, we added the water item as an example

| name  | label  | image  | usable|
|---|---|---|---|
| water  | water  | [<img src="../assets/gauze.png" width="50"/>](../assets/gauze.png)  | false  |

Then specify which item should be treated with which item for which region via config, for example for the head
Inside ```["head"]`` you must specify the item.

![Image](../assets/1.png)

Just like this, the water item for head treatment will now be defined.

```lua

 Config.ItemsForHeal = {
    ["head"] = {
        "forceps", "gauze", "water" 
    },
    ["body"] = {
        "gauze", "pill", "surgical-gloves", "surgical-staple" 
    },
    ["lleg"] = {
        "forceps", "syringe", "tape" 
    },
    ["rleg"] = {
        "forceps", "syringe", "tape" 
    },
    ["rarm"] = {
        "iodine", "gauze", "tape"
    },
    ["larm"] = {
        "iodine", "gauze", "tape"
    }
}
```