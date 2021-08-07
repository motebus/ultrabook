# fBuilder User Guide
*  [Basic Nodes introduction](https://github.com/motebus/ultrabook/blob/main/Ultranet%20Apps/fBuilder/nodes%20intro.md)

## Introduction
Flow Builder (fBuilder) is a low-code programming environment developed by YPCloud, and modelled off IBM’s Node-RED.When you launch a flow, the message travels down the chain of nodes until it reaches the end, with the output of one node being the input of the following node.

## UI Introduction
<img src="https://i.imgur.com/V8hyXg5.png" width=1200 height=600>

* For left hand side it's list of nodes you can use
* For workspace in the middle
  ### <img src="https://i.imgur.com/iOCKLDh.png" width=800 height=30>
  * Includes flow tabs
  * <img src="https://i.imgur.com/QSdg0nI.png" width=30 height=30> to add tabs
  * <img src="https://i.imgur.com/xXm16T3.png" width=30 height=30> list of all tabs
* For right hand side it's a flow manage window <img src="https://i.imgur.com/xEKRbxs.png" width=200 height=30>  
  ### <img src="https://i.imgur.com/yf4T3Be.png" width=30 height=30>  
  * Information of flows: Includes enable/disble flows 
  * <img src="https://i.imgur.com/UHPdPPh.png" width=200 height=250> 
  ### <img src="https://i.imgur.com/BZNT7Ak.png" width=30 height=30>
  * Help of nodes  
  * Examples:
  * <img src="https://i.imgur.com/s82Kq0t.png" width=200 height=600> <img src="https://i.imgur.com/ICqFXMv.png" width=200 height=600> <img src="https://i.imgur.com/uk6Nhu8.png" width=200 height=600> 
  ### <img src="https://i.imgur.com/hxlCBls.png" width=30 height=30> 
  * Debug of flows
  * Example:
  * <img src="https://i.imgur.com/u7tT20h.png" width=500 height=150>
  * funtion node content
  ```
  msg.payload=
  {
    "content": "Hello World~",
  }
  return msg;
  ```
  ### <img src="https://i.imgur.com/uJXy3dz.png" width=30 height=30> 
  * Configuration
  * <img src="https://i.imgur.com/EU3SoQz.png" width=200 height=300> 
  ### <img src="https://i.imgur.com/KB6AFa4.png" width=30 height=30> 
  * Overall
  * <img src="https://i.imgur.com/MoOSTGu.png" width=200 height=200> 
