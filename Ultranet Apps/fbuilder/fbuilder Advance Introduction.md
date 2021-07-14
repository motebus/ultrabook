**Introduction**
  
Jujue Flow is a practical, powerful, and user-friendly function flow package, in which YPCloud has built many strong flows following a precise logic. It includes flows with different functions, like sending content to smartscreen, using motechat, clocking in, and more.
  
**Noun Cleaness**
  
First of all, the word “ flow “ refers to a single series of nodes connected to one another that achieves a certain function. 
More formally, the word "flow" is used describe a tab in the fBuilder/Node-RED editor workspace. These tabs are the main way to organise nodes in a project. (The default name for a tab in a new project is "Flow 1").
However, in YPCloud ultrabook documentation, "flow" is mostly used in the informal sense, to refer to a single collection of nodes. 

Technically, a flow(tab) can contain multiple flows (series of connected nodes). 

Next, “Jujue flow “ is actually a package of multiple flows with a variety of functions. It can be found in the flow library simply as "Jujue", but is otherwise referred to as "Jujue flow". 

**Load Flow**
So if you now are interested in jujue(flow), you first click right icon (sign in icon) on the right top corner of jujue browser web page and sign in the jujue account.

Next you click the icon left to the account icon , you would find the fbuilder icon. Click it to open the fbuilder.

(optional, depending on your need)
At here we click the three bar icon on the right top corner, creat a new project and input the “Name” & :”Qname”

Now you open a new project. We now click the three-bar icon again and select flow library for this time. Click it to into the flow library menu, roll down to find “jujue” , and press the” Load flow “ Button on the right side

**Basic Individual Introduction**

1.	whois flow
function: to return the local information ( fbuilder user end) to telegram. The info includes : Einame / EIMMA / DDN
we can set the telegarm group id in the send node. (remember to let pinponboy in the group)

2. smartscreen flow
function: display with smartscreen the material like
<br>image(sticker)
<br>screenshot(sanpshot demo)
<br>upper notification (notify demo)
<br>applocation demo (app demo)
<br>lower notification (toast demo )
<br>youtube search  ( youtube demo)
<br>marquee (marquee demo)
<br>else eith url (drop demo)
<br>most of them can be complete by changing the detail in the payload node. For example. the url link or the text  in msg.
<br>Also, we can set the smartscreen we want to display on by changinng the  DDN in the send node. 

3. comm flow & console flow
function: use the fbuider to deliver things to your email, telegram and so on...


4. motechat 
function: use YPcloude xstrorage tech to do communication.

5. onevent 
function: deploy the script on the system and receive the  report.
