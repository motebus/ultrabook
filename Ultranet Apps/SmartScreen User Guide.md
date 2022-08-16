# SmartScreen User Guide

SmartScreen is a web-based screening service.
Content across multiple displays and locations can be controlled remotely, @Smartscreen bot, or ubot on Node-Red control.
Simply send images, Youtube videos, and urls from your Telegram-app.

![](https://i.imgur.com/aupapFd.png)

## SmartScreen setting
1. Access SmartScreen through URL: smartscreen.tv
![](https://i.imgur.com/aupapFd.png)

* If you are using a Linux device, SmartScreen can be downloaded from snapcraft. 

2. Click the menu button on the top-left corner to reach "Setting". Here you can name your device, add tags, and setup OnStart and other schedule events. 

Don't forget to click "save" after you make any changes.
![](https://i.imgur.com/yxYGmVf.png)
![](https://i.imgur.com/tCI4kYq.png)
![](https://i.imgur.com/Fe8eNGz.png)
![](https://i.imgur.com/VQEv5KI.png)
![](https://i.imgur.com/lZTAYbQ.png)
![](https://i.imgur.com/3lVwZPY.png)
![](https://i.imgur.com/SpLQi2p.png)
![](https://i.imgur.com/wAWL7a6.png)
![](https://i.imgur.com/bKnA3nW.png)

4. Click "SmartScreen" to exit back to the Home Page.

## How to display a jBoard on your SmartScreen OnStart or at a scheduled time


## How to "drop" images, videos, and urls from Telegram
1. Make sure SmartScreen is already turned on and online.
2. Open your Telegram-app and search for @SmartScreen bot.
3. Key in "/help" to see all commands.
![](https://i.imgur.com/yAfFu94.jpg)

4. Key in "/pin" to set the SmartScreen display(s) to be connected. Enter your SmartScreen name or tag. 

5. Send your content (photo, video, file or url, ect.). If you'd like, you can also add a caption to it. 
### If @SmartScreen bot replies back “Dropped”, means your content should be successfully displayed on your SmartScreen!
![](https://i.imgur.com/79dAUEf.jpg)

### If it replies “DDN off”, means you are not connected to your SmartScreen. 
![](https://i.imgur.com/9xzqiqJ.jpg)

  ### If you want to drop video through command /pin, make sure that you have already turned your video into "mp4" file.


## Command set for the SmartScreenbot
| Command | Function | 
| -------- | -------- | 
|/pin | device pairing | 
|/drop|drop files on your pairing devices|
|/youtube|enter keyword of youtube to play media|
|/miki|upload file(s) to miki storage|
|/jujue|Jujue command interaction|
|/status|get status of pairing device|
|/post|post subtitle to the screen|
|/flow|trigger flow “format” DDN: trigger ID screen
|/rc| remote control button|
|/view| get snapshot from IP cam|
|/help| See all the commands|
