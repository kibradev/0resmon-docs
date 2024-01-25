# Adapting custom ambulancejob scripts

Since the Revive function does not work on every server, we will show you how to adapt it to your own ambulance job script.


## Step 1 : enable revive 

```lua 
Config.EnableRevive = true
```

## Step 2 : adaptation


![Image](../assets/2.png)


Add a new code snippet to the part you see in the picture, the sample code snippet is as follows:

```lua 
  if resource_name == "example_ambulancejob" and GetResourceState(resource_name) == "started" then
        n = true
        break
  end
```

Then write the name of your ambulancejob script in the place indicated by the arrow in the picture.

## Step 3 : Revive event or export adaptation

![Image](../assets/3.png)

Then you need to add your revive function, otherwise the revive will fail. 

Write the name of your ambulancejob script in the place indicated by the red arrow.

Paste your own ambulancejob revive event or export in the green arrow. 

If you don't know this event or export, contact the creator of the script or check the script documentation.

### Note 

If there is a bug in the ambulancejob you are using or a bug in the revive system, the script will automatically disable the revive feature!