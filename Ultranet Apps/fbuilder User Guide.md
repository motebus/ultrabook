# fbuilder User Guide
Table of Contents
- Welcome to fbuilder
- Basic Nodes
- Motechat

## Introduction
Flow Builder (fBuilder) is a low-code programming environment developed by YPCloud, and modelled off IBM’s Node-RED. fBuilder programs are composed of configurable nodes (blocks which perform different functions) which are connected together to create flows. When you launch a flow, the message travels down the chain of nodes until it reaches the end of the flow, with the output of one node being the input of the following node, and so on. 

### Create an account and log in
To use fBuilder, you must first have a Jujue account. 
Go to account.ypcloud.com to create your Jujue account.
Then go to fbuilder at  flow365.ypcloud.com to enter your details and log in. 

If this is your first time logging in, you should see numerous demo flows loaded in the assembly area (center of your window). 

*Option 2: Using the Digital Twin Bot on Telegram, you can create an fBuilder service. Simply use the link provided by the bot after the initialization process is completed.
After clicking on the link, use your Jujue account credentials to log in, and you will be taken to the fBuilder environment.*

![TEST IMAGE](https://i.imgur.com/3pY3o7h.png =800x400)


## Basic Nodes 
Nodes are the building blocks of fBuilder / Node-RED functionality. Here are some basic nodes you should know getting started, and how they are used. 

**Inject**: The Inject node is used to start a flow. Simply connect it to a flow, hit Deploy, and click on the small button on the node to start the flow. 

**Debug**: The Debug node is used to debug a flow. Simply connect it at the end of a flow, or right after the node you want to get the output of. Then hit Deploy and run the flow. The output will be displayed in the debug panel on the right hand side of
the screen (if you can’t see this panel, click on the tab with a bug icon). You can choose to display the entire msg object (all fields of msg), or just msg.payload. 

**Comment**: Used to add text comments to flows. Plain and simple. 

**Function**: This node allows you to run JavaScript code against the messages passed through it, and is one of the most versatile of the basic nodes in fBuilder. By default, messages are passed in as an object called msg, and the function would simply return the input as-is with the line “return msg;”. Returning “null” ends the flow. The function can be anything as long as it returns an msg object in the end, as returning anything else results in an error. 
Frequently, you will use function nodes to edit the payload sent through the flow, like so. 
`msg.payload = “This is a test message.”; return msg;`

The payload can be any type, and can be accessed in the subsequent nodes, where it can be repackaged, manipulated, and sent elsewhere. 
For a more comprehensive description on the function node, refer to the official Node-RED documentation here. 

**Switch**: This node routes messages based on some value (e.g. msg.payload). You can add as many output ports as you need. For example, if you want to use a Telegram bot to process user input, you can use a switch to route to your bot’s different functions depending on the command. 

**Change**: This node provides a direct method to set, change, and delete msg property values. 

**Split**: This node splits msg.payload into a sequence of messages. How the payload is split depends on the payload’s type (e.g. an array of strings would be separated into the constituent strings). 

**Join**: This node joins messages into a single message. If you use a Split node before it in the flow, you can use the “automatic” mode, which will simply undo whatever the Split node did (e.g. joining the array of strings after they were separated into its constituent strings). If you did not use the Split node, or want the messages combined in some other form, you must use the “manual” setting and specify how. You can specify the joined form (e.g. string, array, key/value pairs, etc), as well as
how many objects to join before you send the package (e.g. if you have 30 messages and choose “send the message after 10 parts”, the messages will be sent out in 3 sets of 10). 

**Sort**: This node sorts a message in either ascending or descending order. 

**HTTP Request**: This node can be used to obtain the HTML code of a webpage, and can be used for web-scraping in conjunction with the HTML Parser node. 

**HTML Parser**: This node uses a CSS selector to extract elements by keyword from an HTML document. This can be used for web-scraping if you attach it directly after an HTTP Request node. 

### Installing Additional Nodes 
fBuilder comes with a series of default nodes, but if you require some additional functionality, there’s probably a node for it that you can download from online. If you want to install a node, go to the upper right hand corner and click on “Manage Palette” in the dropdown. Go to “Install” and search for the node by name. Once you find it just click “Install”. From this point forward, this node will be loaded whenever you use fBuilder.

![image alt](https:// "title" =WidthxHeight)

## Node-RED 
fBuilder can be unresponsive at times. If for this reason or some other reason, you want to use Node-RED locally on your computer, you can install Node-RED like so: 
1. Open Terminal 
2. Check that you have Node.js and npm installed. To do this, simply type 
`$ node -v`
`$ npm -v`
If you have both of these installed already, you will get two separate version numbers, one for each. 
If you haven't downloaded either, type 
`$ sudo npm install nodejs`
Once those are installed, download Node-RED by typing 
`$ sudo npm install -g --unsafe-perm node-red`
After installation, type 
`$ node-red`

To start the program head to http://127.0.0.1:1880/ to run it. To stop Node-RED, hit Ctrl-C in Terminal. Pretty much any node you use on fBuilder can be downloaded on Node-RED, and vice versa. 


## Motechat 
If you scroll down on your node palette bar on the left side of your window, you should see several nodes under the category “motechat”. This set of nodes was developed by YPCloud as a means of adaptable, device-to-device communication without the use of IP addresses. Using motechat nodes to properly configure your devices, you can send messages and other types of payloads to all types of compatible devices, such as other computers, servers, Smartscreens, and Telegram channels.

Here are some Motechat nodes to know: 

**Set**: To set the name of your device (e.g. your computer), set the “EiName” field to a name of your choice. Then connect an inject node to the set node, deploy, and click the button. Your device is now set to that name. 
![image alt](https:// "title" =WidthxHeight)

**Payload**: This is used to configure a payload that other Motechat devices can receive. These are in JSON format.

**Send**: This node is used to send payloads to other devices or channels. The Send node has two output ports: the top is for successful sends and the bottom one is for errors (you can connect this one to a debug node to identify errors). 

To send to a Telegram channel, first invite the “Pinponboy” bot into the channel you want to send to. Pinponboy will then return an ID number for the channel. Remember this number. (pin the message the ID number is in to the top of your channel) 

In fBuilder, select the send node and set the fields to strings, then enter “>>comm” for DDN and “-?????????” (ID number) for the Topic. 
![image alt](https:// "title" =WidthxHeight)

To send to another computer, you must know the name of that computer, which you can change with the “Set” node. The receiving computer must also have an onEvent and a retEvent node configured. Then, you can type “>>????”, ???? being the name of that computer, as the DDN, and put the message directly into Topic, to send a message to that computer. 
![image alt](https:// "title" =WidthxHeight)

**OnEvent & retEvent**: These nodes are connected together on a computer to receive Motechat messages from other computers. Without this, you won’t be able to receive any messages so be sure to include them. After you connect the two you don’t have to do anything else with them.
![image alt](https:// "title" =WidthxHeight)

**Call**: This node can be used to request services from a number of Motechat-configured devices. Most likely, this will be used to acquire information stored in YPCloud’s Object Store, which is an online repository. 

## Smartscreen 
A Smartscreen is basically a screen configured to receive Motechat payloads. They can be used for screencasting, for example. To connect to a Smartscreen with fBuilder, you can use the second demo flow on your fBuilder when you first open it up. Look for the label “Smartscreen” to locate the correct flow. 

For a Smartscreen demo, go to “smartscreen.tv” on a separate window on your computer. This is your personal Smartscreen. In the upper left hand corner, click Settings and change the “Name” field to whatever name you want. Hit Save and remember this name.
![image alt](https:// "title" =WidthxHeight)

Then return to fBuilder. To cast, all you have to do is go into the “Send” node of the flow. Make sure both fields are set to “string”. Enter the screen name in the DDN field. You can leave the Topic blank. Finally, hit Deploy and click on any of the inject nodes on the flow, each of which corresponds to a function. Then check your Smartscreen that they are being cast onto it. 

## Clocking In 
Clouder interns are usually requested to set up a clock-in flow on fBuilder near the beginning of their internship. The main purpose of clocking in is not to check if you arrive on time to work. It’s to test the fBuilder system to make sure it’s running, and make it easier for the maintenance personnel at YPCloud to identify bugs and make improvements. 

You should clock in 4 times a day: 00:00, 09:00, 12:00, and 18:00. 
If you are asked to clock in, follow these steps: 
> **Add images between steps**
1) Open a new tab on fBuilder. 
2) Drag in an inject node. Connect it to a Payload node. 
3) In the Payload node, type the following: {“type”: “message”, “content”: “??? clocking in”, “bot”: “pinponboy”}. Replace ??? with your name. Save it.
If you click on the [] next to the payload message, you should see this:

4) Connect a Send node to the Payload node. Set both fields to strings, type “>>comm” for DDN and “ioc://-???” for Topic. The number corresponds to the ID number of ioc://clockin, the Telegram channel where all the clock-in messages are sent. 
5) Connect both ports of the Send node to a debug node. Then hit Deploy. 6) Click on the button in front of the Inject node. Then go to ioc://clockin on Telegram. You should see a message saying “??? clocking in”. 
7) If you send successfully, drag out 3 more Inject nodes and connect them all to your payload. There should now be 4 Inject nodes connected to your payload node. 
8) For each Inject node, scroll to the very bottom and set it to repeat every day at a specific time. The times are 00:00, 09:00, 12:00, and 18:00. Enter one time per node.
9) When you’re done, hit Deploy. Your fBuilder should continue to clock in for you even if you turn off your computer. 


## Telegram Bots 
Implementing a Telegram bot enables you to activate a running fBuilder / Node-RED flow if you type certain commands either directly to a Telegram bot, or to a Telegram channel which the bot is a member of. If this is something you’re interested in doing, here are some basics you should know. 

### How to make a Telegram bot 
Using Telegram (web or mobile version), you can make a bot using BotFather, a bot that helps you make bots. Just look up BotFather in Telegram and type /newbot. You will then receive a prompt to name your bot (which doesn’t have to be unique), then another prompt to type in your bot’s username (which has to be unique, cannot have spaces, and must end with “bot” ).

![image alt](https:// "title" =WidthxHeight)

Congratulations! You now have a bot. You will be given a unique link to your bot (in Telegram, a bot is much like a user account, as you can chat them, add them to groups, etc) and a token to access the HTTP API. The latter piece of info will be particularly important in terms of linking your bot to Node-RED. 

### Group privacy settings 
Say you want other people to be able to use the Telegram bot you made. This can be done by 1) creating a Telegram channel and inviting your friends, 2) inviting your bot into your group, and 3) disabling the privacy settings of your bot. You can do the latter through BotFather: just type “/setprivacy”, choose your bot, and click “Disable”. Note that if your friends want to issue commands to a bot you have made, they have to also include the name of the bot after the command, in the format: “/command@botname”. 

### How to link a Telegram bot to Node-RED 
*Note: some of these functionalities are only available for Node-RED and not for fBuilder. More on that later. 
Given that you have set up a Telegram bot, go to Node-RED and download node-red-contrib-telegrambot (refer to the “Installing Additional Nodes” section if necessary).

This will add five nodes to your palette. The first three (receiver, command, event) are input nodes that take input from Telegram via bot. The latter two (sender, reply) are output nodes that send output to Telegram, also via bot. 
To link any of the input nodes to your bot, drag the node out and double click it. If this is your first time using your bot in Node-RED, click on the small pencil icon next to the “Bot” field. Type your bot name and copy the token you got from BotFather, then click “Update”. 

After you hit “Deploy”, if the linking is successful, the node should display “connected” right below it. If you have a bot registered in Node-RED, you don’t have to type the token again: when using Telegram nodes, just use the dropdown menu and select the name of your bot. 

Receiver: This node is triggered (along with the flow that follows it) when some message is received from the chat. You can test it by connecting both ports of this node to a debug node, going to your bot in Telegram, and sending a random text message. Looking at your debug channel, you should then see a response with the message you sent stored as a string in the field msg.payload.content.

Command: While the receiver node triggers when any message is sent to your bot, the command node only triggers when a specific message of your choosing is sent. Simply link the bot and type the command you want under the Command field. Telegram bot commands typically begin with a forward slash, “/”, so you might want to name your commands accordingly. 

Event: This node is much like the previous two, except it triggers at a specific type of event (e.g. edited message, channel post, etc.) of your choosing. 

Sender: Much like the Motechat send node, this output node sends a message stored in msg.payload to a Telegram channel of your choice (given that your bot is a member of that group and privacy settings are disabled). The msg.payload has to be formatted as follows (you can do this in a function node): 

>msg.payload = { 
chatId: -?????????, 
type: “message”, 
content: [type message here] 
}; 

Replace the ????? with the ID of the Telegram channel you want to send to, and replace [type message here] with the string you want to send. 
Reply: This output node will trigger when someone answers to a specific message in Telegram. The msg.payload should contain the destination chat ID, the ID of the previously sent message in the chat, and the content of the message. This node can be implemented in chatbot-like functions, when you want the bot to have a reaction when you respond to a certain message. 

#### Telegram bots in fBuilder 
Unfortunately, you cannot use node-red-contrib-telegrambot nodes directly in fBuilder, as the bot token will not be automatically passed along like in Node-RED. This is not a problem if you exclusively use Node-RED (e.g. if you run it locally on your computer, or on Node-RED in jServer, etc.). However, if you want to link Telegram bots to flows on fBuilder, you must do it directly through the Telegram Bot API. For the official Telegram documentation and an exhaustive list of commands you can use, see the link here. 
A simple way to obtain the latest message passed to your Telegram bot is to link an inject node which fires very often (e.g. every second), to an HTTP request node with the following URL:
https://api.telegram.org/bot{TOKEN}/getUpdates?offset=-1 
Replace {TOKEN} with your bot’s HTTP API token from BotFather. 

### Web Scraping 
The most straightforward method of web-scraping with fBuilder / Node-RED involves an HTTP request node directly followed by an HTML parser node. The HTTP request node pulls all the HTML code of a webpage given the URL, and the HTML parser node grabs the info you want from the page using keywords. 

To figure out the keyword, you can go to the webpage, right click and select Inspect to bring up the HTML code. If you then click on the small arrow in the upper left corner of the code panel, you can hover over elements of the page to get its tag. 

Insert this tag into the Selector field of the HTML parser node, and use the debug node to view the output. Depending on the nature of the output, you might need to set the Debug node to “complete msg object” instead of “msg.payload” to view the information you are looking for. 

After you capture the raw information you want, you may need to use additional function nodes to repackage or extract the particular entries you want.

### Scan and Watch 
The concept of scan and watch is to configure a program that reports the status of certain devices according to a pre-programmed schedule. If the devices are shown to be faulty or non-functional, they can then be repaired using the provided information. Here is an example of a scan-and-watch fBuilder flow that monitors the status of 6 smartscreens in 5C04. 

Basically, the flow reads from a .ppb file saved in YPCloud’s Object Store repository, which is a list of device specifications it should scan (this is done using Motechat’s “Call” node). It then goes through this list and checks the devices one by one by sending a message to them via Motechat’s “Send” node. It then receives the status of these devices, which it records and sends to a Telegram channel. 

### Configuring Scan-and-Watch 
To configure a scan-and-watch flow, you must first write a .ppb file and upload it to YPCloud’s Object Store repository. Like the Motechat payload, syntax is important or the flow won’t be able to grab the correct information and perform the scans correctly. Specifications for the .ppb are as follows. You can type this in any text file using any text editor; just be sure to change the filename suffix to .ppb afterwards. 

> { 
"catalog": "scan_watch", 
"idname": "???", 
"data": { 
"qname": "???", 
"scan_list": [ 
{ 
"name": "A00", 
"source": "ss", 
"to": "A00", 
"payload":"" 
}, 
{ 
"name": "A01", 
"source": "ss", 
"to": "A00", 
"payload":"" 
}, 
// add as many devices you want to scan using the same format "repeattime": 900000, 
"chatid": -394851932,
"starthour": 9, 
"endhour": 18, 
"ttlcnt": 100 
} 
} 

Note: Idname is the name of the service and can be anything as long as it is descriptive (there should be no spaces in the name, though). Qname is the name used by the fBuilder flow to find the .ppb file, so remember this name (it can be the same as the idname). 

The scan list is a list of objects containing the specifications of each device the flow will scan. Each device is identified by “name” (can be anything, usually the device name), “source” (type of device it is, e.g. Smartscreens are identified by the abbreviation “ss”), “to” (abbreviation of “name” for personal reference, can be the same as “name”), and “payload” (usually left blank). Add as many devices you want to scan using the same format. 

Repeat time, start hour, and end hour dictate when the scans will be performed every day. Based on the above example’s configuration, scans will be performed every 900,000 milliseconds (15 minutes) from 9:00 AM to 6:00 PM every day. The chat id is the ID of the Telegram group the reports are sent to. Don’t worry about ttlcnt for now; you can leave it as 100. 

After you have saved the file as a .ppb file, upload it to the Object Store by going to https://git.page/jj/object. Select “scanwatch” as the bucket and upload the file. Then, open fBuilder, load this flow, and double-click on the “insert name” function node. Simply change the “qname” to match the qname of your .ppb file, hit Deploy, and you’re all set. Reports will be sent to the Telegram channel identified within your .ppb file at intervals of your choice.


###### tags: `yp-md`
