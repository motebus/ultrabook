# Twin Clocking
Clouder interns are usually requested to set up a clock-in flow on fBuilder. The main purpose of clocking in is not to check if you arrive on time to work. It’s to test the qrun system, and make it is easier for the maintainer at YPCloud to identify bugs and make improvements. 

You should clock in 4 times a day: 00:00, 09:00, 12:00, and 18:00. 
If you are asked to clock in, follow these steps: 

* Click on <img src="https://i.imgur.com/66dK5wO.png" width=20 height=20> button in the top right corner and select "Create Project" 
<img src="https://i.imgur.com/i8YrWeI.jpg" width=1000 height=500>

* In project details: type "twin" for Name & QName
<img src="https://i.imgur.com/jspv6Fy.png" width=800 height=400>

### Drag in nodes form left handside column to workspace

* Drag in 5x <img src="https://i.imgur.com/dcq5SnC.png" width=100 height=30> node, they become <img src="https://i.imgur.com/UOdTwVI.png" width=100 height=30>
* Drag in 2x <img src="https://i.imgur.com/Qzisc1K.png" width=100 height=30> node,they become <img src="https://i.imgur.com/hpUnuGs.png" width=100 height=30>
* Drag in 1x <img src="https://i.imgur.com/1664YQI.png" width=100 height=30> node, it becomes <img src="https://i.imgur.com/BUNoE2p.png" width=100 height=30>
* Drag in 1x <img src="https://i.imgur.com/6vCZIev.png" width=100 height=30> node, it becomes <img src="https://i.imgur.com/ocPKneJ.png" width=120 height=50>
 
### Connect nodes
 
* Connect your nodes like this:
<img src="https://i.imgur.com/uDfxHLv.png" width=800 height=400>
 
### Modify each Node contents

* Double click on every node to modify each content
* Remember to click "Done" to save every node's modify

#### timestamp

* You can set name for timestamp 
* For 1st timestamp content

<img src="https://i.imgur.com/XSxu5vX.png" width=700 height=900>

* For 2nd timestamp content

<img src="https://i.imgur.com/kAmxGdU.png" width=700 height=900>

* Try to modify rest of the timestamps yourself

#### Payload

<img src="https://i.imgur.com/1M8lEsY.png" width=700 height=300> 

* Fill the following codes in mail-box icon for 1st payload node

```
{
    "type": "message", 
    "content": "xxxxx initial clocking", 
    "bot": "pinponboy"
}
```

* For the 2nd payload node

```
{
    "type": "message", 
    "content": "xxxxx clocking", 
    "bot": "pinponboy"
}
```

* Replace xxxxx with your English name

#### Send

* For send content

<img src="https://i.imgur.com/qzP16RF.png" width=800 height=300> 

#### Debug

* For debug content

<img src="https://i.imgur.com/4EayyVC.png" width=700 height=300> 

## Before doing the next step your flow should somehow look like this:

<img src="https://i.imgur.com/DS4ZGwy.png" width=700 height=300> 


### Deploy & inject your initial timestamp 

<img src="https://i.imgur.com/Q6b3Ljd.png" width=300 height=50> 

* Press the red "Deploy" button on the top right corner to deploy your flow 
* Press the small blue button in front of "initails" to inject the "timestamp" node for testing
* If your Errmsg is "OK" after inject in the debug window on right hand side & you do see your message in the telegram clocking group it means testing success

<img src="https://i.imgur.com/TBBg4ZD.png" width=300 height=500>

### Qrun your twin
* After testing success
* Click on <img src="https://i.imgur.com/66dK5wO.png" width=20 height=20> button again in the top right corner and select "Qrun" 
* Choose "h2-qbix" to deploy

<img src="https://i.imgur.com/drivpK5.png" width=500 height=500>


* If it shows this on your page

<img src="https://i.imgur.com/2cFUJHH.png" width=700 height=100>

* It means success deploying to "h2-qibx"
* Keep watching telegram clocking group to see whether your twin works on recommended time after successfully qurn no matter you log out your fbuilder/shutdown your pc

# Congrats you have finish the Guide


