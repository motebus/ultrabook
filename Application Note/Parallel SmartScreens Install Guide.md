# Parallel instances of SmartScreen
Steps to install and enable running multiple browsers of SmartScreen at the same time:

`$ sudo snap set system experimental.parallel-instances=true `

`$ sudo snap download smartscreen` 

Note what revision of smartscreen has been installed: e.g. `snap install smartscreen_18.snap`, `snap install smartscreen_30.snap`, etc. 

Next:

`$ sudo snap install --dangerous --name smartscreen_s1 ./smartscreen_18.snap `

- Substitute `smartscreen_s1` with the name of your choice. For ease of use, it is recommended that you follow the general general pattern of "smartscreen_s1", "smartscreen_s2", "smartscreen_s3" etc.
- Substitute `smartscreen_18.snap` with the name of the SmartScreen revision installed in the previous command line. 

Repeat this step for as many copies of SmartScreen you need. 

## Using SmartScreen from your terminal:  

To launch: ` $ smartscreen_s1` (using the name of your SmartScreen)

To control the foreground display on your screens/which display you want to launch your SmartScreen on:

`＄ SS_DISPLAY=1 smartscreen_s1`  (change the display number and SmartScreen name)

Find more ways to control your SmartScreen display with: `$ smartscreen --help`

# Other tips:

To delete your snap: `$ snap remove "snap name"`

For a list about the snaps you have installed enter `$ snap list`

For more: https://snapcraft.io/docs/getting-started




