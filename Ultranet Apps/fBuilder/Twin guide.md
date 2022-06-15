# Twin Clocking
Clouder interns are usually requested to set up a clock-in flow on fBuilder. The main purpose of clocking in is not to check if you arrive on time to work, but to test the QRun system, and make it easier for the maintainer at YPCloud to identify bugs and make improvements. 

Your “twin” should be clocking in 4 times a day: 00:00, 09:00, 12:00, and 18:00. 
If you are asked to create a twin clock-in flow follow these steps: 

### Go to fBuilder
* fbuilder url: [run](https://run.ypcloud.com)
* Login with your YPCloud account and choose "fbuilder" and click "go"
* You will see a page like this: 
<img src="https://i.imgur.com/i8YrWeI.jpg">

### Start a new fBuilder project 
* Click on the <img src="https://i.imgur.com/66dK5wO.png" width=20 height=20> button in the top right corner and select "Create Project" 
* In project details: type "twin" for Name & QName
<img src="https://i.imgur.com/jspv6Fy.png">

### Drag in nodes from the Node Palette sidebar on the left to the workspace. 
* Drag in 5x <img src="https://i.imgur.com/dcq5SnC.png" width=100 height=30> node. They'll become <img src="https://i.imgur.com/UOdTwVI.png" width=100 height=30>
* Drag in 2x <img src="https://i.imgur.com/Qzisc1K.png" width=100 height=30> node. They'll become <img src="https://i.imgur.com/hpUnuGs.png" width=100 height=30>
* Drag in 1x <img src="https://i.imgur.com/1664YQI.png" width=100 height=30> node. They'll become <img src="https://i.imgur.com/BUNoE2p.png" width=100 height=30>
* Drag in 1x <img src="https://i.imgur.com/6vCZIev.png" width=100 height=30> node. They'll become <img src="https://i.imgur.com/ocPKneJ.png" width=120 height=50>
These are the most basic and frequently used nodes on fBuilder.

### Connect nodes
* Connect your nodes like this:
<img src="https://i.imgur.com/uDfxHLv.png">
 
### Modify each Node

* Double click on every node to modify its properties.
* Remember to click "Done" to save your modifications. 

#### timestamp

* Name the timestamp.
* For the 1st timestamp,remember to check the box for "Inject once after `0.2` seconds".
<img src="https://i.imgur.com/XSxu5vX.png">


* For the 2nd timestamp, select "Repeat `at a specific time`". Fill in "at`09:00`", then check the boxes for all days Monday-Sunday.
<img src="https://i.imgur.com/kAmxGdU.png">

* Try to modify the rest of the timestamps yourself.

#### Payload

<img src="https://i.imgur.com/1M8lEsY.png" width=700 height=300> 

* For the 1st payload node, fill in the following lines of code in the field next to the mail-box icon.

```
{
    "type": "message", 
    "content": "xxxxx initial clocking", 
    "bot": "pinponboy"
}
```

* For the 2nd payload node:

```
{
    "type": "message", 
    "content": "xxxxx clocking", 
    "bot": "pinponboy"
}
```

* Replace xxxxx with your English name.

#### Send

* For the send node, fill in

```
>hub/comm
```
```
ioc://-346930568
```

* Remember to change it to "az"

<img src="https://imgur.com/ZTpeMEW"> 

#### Debug

* For the debug node:

<img src="https://i.imgur.com/4EayyVC.png"> 

## Before the next step your flow should somehow look like this:

<img src="https://i.imgur.com/DS4ZGwy.png"> 


### Deploy & inject your initial timestamp 

<img src="https://i.imgur.com/Q6b3Ljd.png"> 

* Press the red "Deploy" button on the top right corner to deploy your flow. 
(Remember to do this every time you change the content of any flow or else your changes won't be saved)
* Press the small blue button in front of the 1st timestamp node "initials" to inject the node for testing.
* Open the debug window in the left-hand sidebar. If your Errmsg is "OK" after injecting the node and you see your message in the telegram clocking group, your test has been successful.

<img src="https://i.imgur.com/TBBg4ZD.png">

### Qrun your twin
* After the successful test, click on the <img src="https://i.imgur.com/66dK5wO.png" width=20 height=20> button again in the top right corner and select "QRun" 
* Choose "h4-node" to deploy

<img src="https://imgur.com/85Sw4nA">

* If a "Deploy success" or "Timeout" message shows up on your page, your QRun has been successful. 
<img src="https://i.imgur.com/GV3RRGW.png">


* Keep watching the Telegram clocking group to see whether your twin works at the four times even after you've logged out of fbuilder/shutdown your pc. 

* Always Remeber to logout fbuidler!!!

# Congrats. You have finished the Guide.
