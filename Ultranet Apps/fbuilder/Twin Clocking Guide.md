## Twin Clocking
Clouder interns are usually requested to set up a clock-in flow on fBuilder. The main purpose of clocking in is not to check if you arrive on time to work. It’s to test the qrun system, and make it is easier for the maintainer at YPCloud to identify bugs and make improvements. 

You should clock in 4 times a day: 00:00, 09:00, 12:00, and 18:00. 
If you are asked to clock in, follow these steps: 

* Click <img src="https://i.imgur.com/66dK5wO.png" width=20 height=20> button in the top right corner and select "Create Project" 
<img src="https://i.imgur.com/i8YrWeI.jpg" width=1000 height=500>

* In project details: type "twin" for Name & QName
<img src="https://i.imgur.com/jspv6Fy.png" width=800 height=400>

### Drag in nodes form the left column to workspace

* Drag in 5x <img src="https://i.imgur.com/dcq5SnC.png" width=100 height=30> node, they become <img src="https://i.imgur.com/UOdTwVI.png" width=100 height=30>
* Drag in 2x <img src="https://i.imgur.com/Qzisc1K.png" width=100 height=30> node,they become <img src="https://i.imgur.com/hpUnuGs.png" width=100 height=30>
* Drag in 1x <img src="https://i.imgur.com/1664YQI.png" width=100 height=30> node, it becomes <img src="https://i.imgur.com/BUNoE2p.png" width=100 height=30>
* Drag in 1x <img src="https://i.imgur.com/6vCZIev.png" width=100 height=30> node, it becomes <img src="https://i.imgur.com/ocPKneJ.png" width=120 height=40>
 
 ### Connect nodes
 
* Connect your nodes like this
<img src="https://i.imgur.com/uDfxHLv.png" width=800 height=400>
 
### Each Node contents
#### timestamp

* You can set name for timestamp 
* For 1st timestamp content

<img src="https://i.imgur.com/XSxu5vX.png" width=700 height=900>

* For 2nd timestamp content

<img src="https://i.imgur.com/kAmxGdU.png" width=700 height=900>

* Try to modify rest of the timestamps yourself

#### Payload
<img src="https://i.imgur.com/1M8lEsY.png" width=700 height=300> 

* Double click the first "payload" node and fill the following codes in mail-box icon

```
{
    "type": "message", 
    "content": "xxxxx initial clocking", 
    "bot": "pinponboy"
}
```
for the second payload
```
{
    "type": "message", 
    "content": "xxxxx clocking", 
    "bot": "pinponboy"
}
```
* Replace xxxxx with your English name

#### Send

#### Debug

