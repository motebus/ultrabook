## Twin Clocking
Clouder interns are usually requested to set up a clock-in flow on fBuilder. The main purpose of clocking in is not to check if you arrive on time to work. It’s to test the qrun system, and make it is easier for the maintainer at YPCloud to identify bugs and make improvements. 

You should clock in 4 times a day: 00:00, 09:00, 12:00, and 18:00. 
If you are asked to clock in, follow these steps: 

* 1 Click <img src="https://i.imgur.com/66dK5wO.png" width=20 height=20> button in the top right corner and select Create a new Project. 
* 2 In project details: type "twin" for Name & QName.
<img src="https://i.imgur.com/i8YrWeI.jpg" width=1000 height=600>
<img src="https://i.imgur.com/dgwFKdL.png" width=500 height=500>
* 3 Drag in an  <img src="https://i.imgur.com/dcq5SnC.png" width=100 height=30> node & it becomes <img src="https://i.imgur.com/dcq5SnC.png" width=100 height=30> in the workspace and drag an **Payload** node from the left column.
* 4 Connect the **Inject** node to the input end of the **Payload** node (left). 
* 5 Double click the **Payload** node and type the following string into the second input line with an e-mail icon.
```
{
    "type": "message", 
    "content": "xxxxx clocking", 
    "bot": "pinponboy"
}
```
Replace "xxxxx" with your name. Click "Done" to save.

* 6 Drag in a **Send** node and connect it to the output end of the **Payload** node. Double click the Send node and set both DDN and Topic fields to strings, and then type `>>comm` for DDN and `ioc://xxxxx` for Topic, where "xxxxx" is replaced with the channelID number of the target Telegram channel. Usually the channel ID is the 9-digit part coming right after "p=" in the url bar.
* 7 Connect both outputs of the **Send** node to a **Debug** node, and then click Deploy.
* 8 Click on the button in front of the **Inject** node. Then go to the target channel on Telegram. You should see a message saying "NAME clocking". 
* 9 If the message sends successfully, drag in 3 more **Inject** nodes and connect them all to your **Payload**. There should now be 4 **Inject** nodes connected to your **Payload** node. 
* 10 For each **Inject** node, double click it and scroll to the bottom. Set Repeat every day (with Monday to Sunday checked) "at a specific time". The times of each **Inject** node should be set to 00:00, 09:00, 12:00, and 18:00, respectively. 

Your flow now should look similar to this.
![image](https://user-images.githubusercontent.com/20572126/111123353-3086b080-85aa-11eb-88d7-d0b998e5305c.png)

* 11 Add one more **Inject** node and **payload** node, and set it to inject once after 0.1 seconds with no repeats and also the content```{"type": "message", "content": "NAME initial clocking", "bot": "pinponboy"}.``` This is your initial clocking node. 
![截圖 2021-04-27 下午4 24 46](https://user-images.githubusercontent.com/32254088/116835818-b2807680-abf6-11eb-869c-a748005dcf87.png)
* 12 When you're all done, click Deploy. 
* 13 Next, click the button on the top right corner and select "QRun". Choose "h2-qbix" to deploy. Your twin should continue to clock in even if you close the webpage, logout, or shutdown your computer. 
![image](https://imgur.com/yMwn7ic.png)
![截圖 2021-04-29 下午12 03 30](https://user-images.githubusercontent.com/32254088/116835834-c1ffbf80-abf6-11eb-9288-c2e1c564043a.png)
