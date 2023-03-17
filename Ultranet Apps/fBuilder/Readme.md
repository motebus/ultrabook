# fBuilder User Guide
URL - [RUN](https://run.ypcloud.com) -> Login -> Choose "fBuilder" then click "go" to start 

Flow Builder (fBuilder) is a low-code programming environment developed by YPCloud, and modelled off IBM’s Node-RED

When you launch a flow, the message travels down the chain of nodes until it reaches the end, with the output of one node being the input of the following node.

---

## Introduction

- [User Interface](#User-Interface)

- [Basic Nodes](#Basic-Nodes)

- [QRun](#QRun)

- [Flow Import & Export](#Flow-Import-and-Export)

### FlowBot Guide (Sample)

- [Twin Clocking](https://github.com/YPCloudInc/Clouder/blob/main/md/twin.md)

- [ChatBot](https://github.com/YPCloudInc/Clouder/blob/main/md/chatbot.md)

- [FormBot](https://github.com/YPCloudInc/Clouder/blob/main/md/form.md)

### [Samples](https://github.com/motebus/ultrabook/blob/main/Ultranet%20Apps/fBuilder/Sample%20Flows/Readme.md)

---

# User Interface

[<img src="https://i.imgur.com/V8hyXg5.png" width=1200 height=600>](https://run.ypcloud.com)

---

## Left Column - List of Nodes

  * You won't be able to install nodes from palette, you may explore [Node-RED](https://nodered.org/) if you're interested in trying nodes out of the list.

---

## Middle - Workspace

Flow Tabs - [<img src="https://i.imgur.com/iOCKLDh.png" width=800 height=30>](https://run.ypcloud.com)

[<img src="https://i.imgur.com/QSdg0nI.png" width=30 height=30>](https://run.ypcloud.com) - Add Tabs

[<img src="https://i.imgur.com/xXm16T3.png" width=30 height=30>](https://run.ypcloud.com) - List of Tabs

---

## Top Right Corner [<img src="https://i.imgur.com/KCUock7.png" width=150 height=30>](https://run.ypcloud.com)

[<img src="https://i.imgur.com/SbNMST5.png" width=120 height=30>](https://run.ypcloud.com) - Click Deploy to **save** your flow after your edits

Log Out - [<img src="https://i.imgur.com/LVwWqqI.png" width=30 height=30>](https://run.ypcloud.com)

[<img src="https://i.imgur.com/w56SCE1.png" width=30 height=30>](https://run.ypcloud.com) - List
> [<img src="https://i.imgur.com/Ovl4J96.png" width=200 height=600>](https://run.ypcloud.com)

---

## Right Column - Flow Management Window [<img src="https://i.imgur.com/xEKRbxs.png" width=200 height=30>](https://run.ypcloud.com)

[<img src="https://i.imgur.com/yf4T3Be.png" width=30 height=30>](https://run.ypcloud.com) - Information: Include "enable/disable flows"
> [<img src="https://i.imgur.com/UHPdPPh.png" width=230 height=250>](https://run.ypcloud.com)
  
[<img src="https://i.imgur.com/BZNT7Ak.png" width=30 height=30>](https://run.ypcloud.com) - Help

> Examples:
> [<img src="https://i.imgur.com/s82Kq0t.png" width=200 height=600>](https://run.ypcloud.com) 
[<img src="https://i.imgur.com/ICqFXMv.png" width=200 height=600>](https://run.ypcloud.com) 
[<img src="https://i.imgur.com/uk6Nhu8.png" width=200 height=600>](https://run.ypcloud.com) 
  
[<img src="https://i.imgur.com/hxlCBls.png" width=30 height=30>](https://run.ypcloud.com) - Debug
> Example:
> [<img src="https://i.imgur.com/u7tT20h.png" width=500 height=150>](https://run.ypcloud.com)

- Funtion Node Content

  ```
  msg.payload=
  {
    "content": "Hello World~",
  }
  return msg;
  ```
  
[<img src="https://i.imgur.com/uJXy3dz.png" width=30 height=30>](https://run.ypcloud.com) - Configuration
> [<img src="https://i.imgur.com/EU3SoQz.png" width=200 height=300>](https://run.ypcloud.com)
  
[<img src="https://i.imgur.com/KB6AFa4.png" width=30 height=30>](https://run.ypcloud.com) - Overall
> [<img src="https://i.imgur.com/MoOSTGu.png" width=200 height=200>](https://run.ypcloud.com) 

---

# Basic Nodes

## Tips

1. "Double click" each node to edit contents, press each node's [<img src="https://i.imgur.com/a1M9i9h.png" width=60 height=25>](https://run.ypcloud.com) when finish

2. You may use "ctrl+c" & "ctrl+v" to copy/paste nodes

3. You may "frame up" multi nodes using your mouse to move or copy/paste

4. Click [<img src="https://i.imgur.com/SbNMST5.png" width=100 height=25>](https://run.ypcloud.com) before debug/leaving page, or else the changes you've made  won't be saved, the button turns blue after deploying

5. Example - [<img src="https://i.imgur.com/7KWSIGM.png" width=110 height=45>](https://run.ypcloud.com) 
  - If the "Red triangle" appears, the content of node is empty or there's bug in the json code 
  - If the "Blue dot" appears, the node is not "Deployed" yet click [<img src="https://i.imgur.com/SbNMST5.png" width=100 height=25>](https://run.ypcloud.com) 

---

## Nodes Table
* [inject](#inject) [<img src="https://i.imgur.com/CLSpzfz.png" width=110 height=30>](https://run.ypcloud.com)

* [set](#set) [<img src="https://i.imgur.com/mrUJBKE.png" width=110 height=30>](https://run.ypcloud.com)

* [payload](#payload) [<img src="https://i.imgur.com/XlbGGpk.png" width=110 height=30>](https://run.ypcloud.com)

* [function](#function) [<img src="https://i.imgur.com/QX7O8PO.png" width=110 height=30>](https://run.ypcloud.com)

* [send](#send) [<img src="https://i.imgur.com/LQ1jsMD.png" width=110 height=30>](https://run.ypcloud.com)

* [call](#call) [<img src="https://i.imgur.com/cF7R86U.png" width=110 height=30>](https://run.ypcloud.com)

* [switch](#switch) [<img src="https://i.imgur.com/UuE2qCf.png" width=110 height=30>](https://run.ypcloud.com)

* [debug](#debug) [<img src="https://i.imgur.com/zdAEqm1.png" width=110 height=30>](https://run.ypcloud.com)

* [comment](#comment) [<img src="https://i.imgur.com/URNpYxU.png" width=110 height=30>](https://run.ypcloud.com)

* [on/ret event](#1) [<img src="https://i.imgur.com/6mbbHyl.png" width=110 height=30>](https://run.ypcloud.com) & [<img src="https://i.imgur.com/HCFQkIE.png" width=110 height=30>](https://run.ypcloud.com)

---

### | inject [<img src="https://i.imgur.com/CLSpzfz.png" width=110 height=30>](https://run.ypcloud.com)
> [<img src="https://i.imgur.com/sWgEnlW.png" width=120 height=35>](https://run.ypcloud.com)

* It's also known as a "timestamp" node as it can trigger on specific time

* Usually the first node of a chain

* After Deploying click the blue button on the left of the node to trigger

* The check box of "inject once after 0.1/customize seconds" means that after Deploying it will auto inject once

* Repeat can customize the time to execute the chain repeatedly

> [<img src="https://i.imgur.com/ppCarhZ.png" width=500 height=700>](https://run.ypcloud.com)

---

### | set [<img src="https://i.imgur.com/mrUJBKE.png" width=110 height=30>](https://run.ypcloud.com)
* To set the name of device (e.g. your container), set the “EiName” field to a name you want

* Then connect an inject node to the set node, deploy, and click the button

* Device is now set to that name

> [<img src="https://i.imgur.com/5N7rr5q.png" width=300 height=200>](https://run.ypcloud.com)

---

### | payload [<img src="https://i.imgur.com/XlbGGpk.png" width=110 height=30>](https://run.ypcloud.com)
* To configure a payload that other Motechat devices can receive

* It's in JSON format

---

### | function [<img src="https://i.imgur.com/QX7O8PO.png" width=110 height=30>](https://run.ypcloud.com)
* One of the most versatile of the basic nodes 

* Allows to run JavaScript code against the messages passed through

* By default, messages are passed in as an object called msg, and the function would return the input with the line “return msg;”

* Returning “null” ends the flow

* Can work many way as long as it returns an msg object, returning anything else results error. 

---

### | send [<img src="https://i.imgur.com/LQ1jsMD.png" width=110 height=30>](https://run.ypcloud.com)
> [<img src="https://i.imgur.com/Y9R4kge.png" width=120 height=35>](https://run.ypcloud.com)

* To send payloads to other devices or channels.

* The Send node has two output ports: the top one is for successful sends and the bottom one is for errors

* Send DDN by >>xxx & topic by xxx://xxx (ex:>>comm,tg://-12345678)

---

### | call [<img src="https://i.imgur.com/cF7R86U.png" width=110 height=30>](https://run.ypcloud.com)
* Can be used to request services from a number of Motechat-configured devices

* This will be used to acquire information stored in YPCloud’s Object Store

---

### | switch [<img src="https://i.imgur.com/UuE2qCf.png" width=110 height=30>](https://run.ypcloud.com)
* Can add as many output ports as you need.

* Can be use like for loop

---

### | debug [<img src="https://i.imgur.com/zdAEqm1.png" width=110 height=30>](https://run.ypcloud.com)
> [<img src="https://i.imgur.com/jJW9AuB.png" width=120 height=35>](https://run.ypcloud.com)

Options
> [<img src="https://i.imgur.com/AQMj9hI.png" width=400 height=300>](https://run.ypcloud.com) [<img src="https://i.imgur.com/hkZe0nE.png" width=400 height=300>](https://run.ypcloud.com)

---

### | comment [<img src="https://i.imgur.com/URNpYxU.png" width=110 height=30>](https://run.ypcloud.com)
* Used to add text comments to flows

---

### <h3 id="1">| on/ret event</h3> [<img src="https://i.imgur.com/6mbbHyl.png" width=110 height=30>](https://run.ypcloud.com) & [<img src="https://i.imgur.com/HCFQkIE.png" width=110 height=30>](https://run.ypcloud.com)
It is used on a contanier to receive Motechat messages from other containers

* These nodes are connected like this

> [<img src="https://i.imgur.com/6JCxVpb.png" width=450 height=120>](https://run.ypcloud.com)

---

# QRun

After finishing the flow, click [<img src="https://i.imgur.com/66dK5wO.png" width=20 height=20>](https://run.ypcloud.com) (top right corner) and select "QRun"

Select one of the following to deploy
[<img src="https://i.imgur.com/ZUuFPvK.png">](https://run.ypcloud.com)

If a "Deploy success" or "Timeout" message shows up on your page, your QRun has been successful

If its showing something else, your QRun has failed
> (ask for help)[<img src="https://i.imgur.com/GV3RRGW.png">](https://run.ypcloud.com)

Check whether your flow works (through Telegram Group, ioc, etc.) after you've logged out of fBuilder / shutdown your pc
> Remember to logout of fBuilder after use!

---

# Flow Import and Export

## Import flow
Import flow.json or xxx.flow

[<img src="https://i.imgur.com/U82C32z.png" width=790 height=437>](https://run.ypcloud.com)

Paste your flow or choose flow file

[<img src="https://i.imgur.com/ELGRqsg.png" width=790 height=437>](https://run.ypcloud.com)

---

## Export flow
You may export specific nodes or the whole flow

You may download json file or copy json to clip board (& "ctrl + v" to paste it directly anywhere

[<img src="https://i.imgur.com/L8p0Qwt.png">](https://run.ypcloud.com)
