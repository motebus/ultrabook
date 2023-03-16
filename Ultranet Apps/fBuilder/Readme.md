# fBuilder User Guide
URL - [RUN](https://run.ypcloud.com) -> Login -> Choose "fBuilder" then click "go" to start 

Flow Builder (fBuilder) is a low-code programming environment developed by YPCloud, and modelled off IBM’s Node-RED

When you launch a flow, the message travels down the chain of nodes until it reaches the end, with the output of one node being the input of the following node.

---

## Introduction

### [User Interface](#User-Interface)

### [Basic Nodes](https://github.com/motebus/ultrabook/blob/main/Ultranet%20Apps/fBuilder/basic%20nodes%20intro.md)

### [QRun](https://github.com/motebus/ultrabook/blob/main/Ultranet%20Apps/fBuilder/qrun.md)

### [Flow Import & Export](https://github.com/motebus/ultrabook/blob/main/Ultranet%20Apps/fBuilder/import%20%26%20export.md)

### [Twin Clocking Guide](https://github.com/motebus/ultrabook/blob/main/Ultranet%20Apps/fBuilder/Twin%20guide.md)

#### [Samples](https://github.com/motebus/ultrabook/blob/main/Ultranet%20Apps/fBuilder/Sample%20Flows/Readme.md)

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
