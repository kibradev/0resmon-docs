---
description: S4 Health System V2 Installation Document and Basic Concepts
---

# Adapting Custom Ambulance Job

## Adapting custom ambulancejob scripts <a href="#adapting-custom-ambulancejob-scripts" id="adapting-custom-ambulancejob-scripts"></a>

Since the Revive function does not work on every server, we will show you how to adapt it to your own ambulance job script.

### Step 1 : enable revive <a href="#step-1-enable-revive" id="step-1-enable-revive"></a>

```lua
Config.EnableRevive = true
```

### Step 2 : adaptation <a href="#step-2-adaptation" id="step-2-adaptation"></a>

![Image](https://docs.0resmon.com/HealthSystemV2/assets/2.png)

Add a new code snippet to the part you see in the picture, the sample code snippet is as follows:

```lua
if resource_name == "example_ambulancejob" and GetResourceState(resource_name) == "started" then
    n = true
    break
end
```

Then write the name of your ambulancejob script in the place indicated by the arrow in the picture.

### Step 3 : Revive event or export adaptation <a href="#step-3-revive-event-or-export-adaptation" id="step-3-revive-event-or-export-adaptation"></a>

![Image](https://docs.0resmon.com/HealthSystemV2/assets/3.png)

Then you need to add your revive function, otherwise the revive will fail.

Write the name of your ambulancejob script in the place indicated by the red arrow.

Paste your own ambulancejob revive event or export in the green arrow.

If you don't know this event or export, contact the creator of the script or check the script documentation.

#### Note <a href="#note" id="note"></a>

If there is a bug in the ambulancejob you are using or a bug in the revive system, the script will automatically disable the revive feature!
