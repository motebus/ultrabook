## Tips

1. "Double click" each node to edit contents, press each node's [<img src="https://i.imgur.com/a1M9i9h.png" width=60 height=25>](https://run.ypcloud.com) when finish

2. You may use "ctrl+c" & "ctrl+v" to copy/paste nodes

3. You may "frame up" multi nodes using your mouse to move or copy/paste

4. Click [<img src="https://i.imgur.com/SbNMST5.png" width=100 height=25>](https://run.ypcloud.com) before debug/leaving page, or else the changes you've made  won't be saved, the button turns blue after deploying

5. Example - [<img src="https://i.imgur.com/7KWSIGM.png" width=110 height=45>](https://run.ypcloud.com) 
  - If the "Red triangle" appears, the content of node is empty or there's bug in the json code 
  - If the "Blue dot" appears, the node is not "Deployed" yet click [<img src="https://i.imgur.com/SbNMST5.png" width=100 height=25>](https://run.ypcloud.com) 

---

## Nodes table
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

### inject 
<img src="https://i.imgur.com/CLSpzfz.png" width=110 height=30> > <img src="https://i.imgur.com/sWgEnlW.png" width=120 height=35>

* It's also known as a "timestamp" node as it can trigger on specific time

* Usually the first node of a chain

* After Deploying click the blue button on the left of the node to trigger

* The check box of "inject once after 0.1/customize seconds" means that after Deploying it will auto inject once

* Repeat can customize the time to execute the chain repeatedly

* <img src="https://i.imgur.com/ppCarhZ.png" width=500 height=700>

### set
* To set the name of device (e.g. your container), set the “EiName” field to a name you want

* Then connect an inject node to the set node, deploy, and click the button

* Device is now set to that name

* <img src="https://i.imgur.com/5N7rr5q.png" width=300 height=200>

### payload
* To configure a payload that other Motechat devices can receive

* It's in JSON format

### function
* One of the most versatile of the basic nodes 

* Allows to run JavaScript code against the messages passed through

* By default, messages are passed in as an object called msg, and the function would return the input with the line “return msg;”

* Returning “null” ends the flow

* Can work many way as long as it returns an msg object, returning anything else results error. 


### send
<img src="https://i.imgur.com/LQ1jsMD.png" width=110 height=30> => <img src="https://i.imgur.com/Y9R4kge.png" width=120 height=35>

* To send payloads to other devices or channels.

* The Send node has two output ports: the top one is for successful sends and the bottom one is for errors

* Send DDN by >>xxx & topic by xxx://xxx (ex:>>comm,tg://-12345678)
 
### call
* Can be used to request services from a number of Motechat-configured devices

* This will be used to acquire information stored in YPCloud’s Object Store

### switch
* Can add as many output ports as you need.

* Can be use like for loop

### debug
<img src="https://i.imgur.com/zdAEqm1.png" width=110 height=30> > <img src="https://i.imgur.com/jJW9AuB.png" width=120 height=35>

* Can choose <img src="https://i.imgur.com/AQMj9hI.png" width=400 height=300> <img src="https://i.imgur.com/hkZe0nE.png" width=400 height=300>

### comment 
* Used to add text comments to flows

### <h3 id="1">on/ret event</h3>
It is used on a contanier to receive Motechat messages from other containers

* These nodes are connected like this

* <img src="https://i.imgur.com/6JCxVpb.png" width=450 height=120>
