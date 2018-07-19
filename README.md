# nPose MenuMemoryExtension Plugin
WIP: CURRENTLY NOT RELEASED
## Brief summary
Currently the nPose scripts can handle approx. 200-350 Notecards (buttons inside the menu) depending of the length of the button names.
With this plugin we should be able to increase the number up to the maximum number of items that can be placed into a prim (which may be limited to 10.000 see http://wiki.secondlife.com/wiki/Limits#Inventory)  
Please keep in mind that Button Permissions are still handled by the main menu script. This means that you should optimize the usage of them.
## Requirements
- nPose V3.11 and newer
- one or more nPose MenuMemoryExtension Plugins. Each one should be able to handle approx 400-800 notecards (depending of the length of the button names)
- a configuration notecard called `.nPose MenuMemoryExtension`
## Configuration notecard `.nPose MenuMemoryExtension`
With this notecard, we tell nPose which parts of the menu should be handled by which script. Its content looks line a .ini file. Complex example:
```
[1]
SET:Females
SET:Males
[2]
SET:Childs
SET:Grannies
```
The numbers inside the square brackets are targeting the `nPose MenuMemoryExtension Plugin`.
In this case we are using two of them. The first handles all cards below `SET:Females` (such as `SET:Females:Sit1` and so on) and also the cards below `SET:Males`.
The second Plugin script handles all cards below `SET:Childs` and `SET:Grannies`. All other cards are handled by the main menu script `nPose menu`.

An easy example would be:
```
[1]
SET
```
Which requires one `nPose MenuMemoryExtension Plugin` script and tells nPose that all cards are handled by the plugin. With this configuration you should be able to use approx 400-800 notecards.