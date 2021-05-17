# jBuilder User Guide
jBuilder is used to build jboards, which can be collated onto a dock to create interactive display dashboards.


## Table of Contents
- [jBuilder](###Access-Jbuilder)
- [Dock Builder](##Dock-Builder-User-Manual)

![](https://i.imgur.com/aISUXNM.png)

### Access jBuilder: 
1. To login to jbuilder, you need a Jujue account. If you don't have one yet, register at account.ypcloud.com
2. Go to jbuilder.ypcloud.com and sign in. <br>
If you are unable to sign in, please contact YP Customer Support for assistance. 

### jBuilder UI: 
On the left hand side <img src="https://i.imgur.com/66dK5wO.png" width=30 height=30> sidebar, the user can define the board grid by specifying the number of columns and rows, as well as enable/disable the header and footer of the board frame. 
The board grid serves as the framework for the board’s layout and helps us manage the proportions between elements for responsive web design. 

<img src="https://i.imgur.com/fuglHd7.png" width=760 height=475>

The icons in the upper right corner allow the user to add panels <img src="https://i.imgur.com/J4a1Laa.png" width=30 height=30>, refresh window to start a new board <img src="https://i.imgur.com/0EQSXdh.png" width=30 height=30>, view data in json format <img src="https://i.imgur.com/9f04Grd.png" width=30 height=30>, view the public/private board list <img src="https://i.imgur.com/rNDVXuk.png" width=30 height=30>, and logout from their account <img src="https://i.imgur.com/EvC18xA.png" width=32 height=30>. 


## Creating a jBoard: 
<img src="https://i.imgur.com/6OoYgUK.png">

1. Click on the <img src="https://i.imgur.com/J4a1Laa.png" width=30 height=30> icon in the upper right hand corner to add a new panel.
2. Click on the <img src="https://i.imgur.com/6biIEa1.png" width=31 height=30> icon to edit the panel.
3. In the Width and Height fields you can specify the dimensions of the panel. 
4. Assign a name to the panel inside the Name field. 
5. Specify the frame style in the App field. * See a list of available types further below.  
6. Add in parameters and/or data. 
7. Hit Confirm once you are done. 

![](https://i.imgur.com/yJR5ynR.png)

## Saving a jBoard 
Always remember to save your jboard. To save a jboard, click on the icon on the upper right hand corner <img src="https://i.imgur.com/TJUZUG1.png" width=35 height=30>. Enter a name* and hit Save. The name entered will be the QName of your jboard. *(This name cannot be changed later on).*

When making new changes, you need to save first before your edits can be displayed.


## Available Types of Frame-Style 
#### Web Page 
1. Type`page://url` into the App Field and {"url":"YourURL"} into the Params field, replacing `YourURL` with the actual url of the website. 
#### YouTube Video 
1. Paste the url into the App Field. 
  Note: Use the address bar url, e.g. https://www.youtube.com/watch?v=VIDEOID, not the video sharing link https://youtu.be/VIDEOID. 

#### Image 
1. Type `page://url` into the App Field.
2. Enter {"url":"<url>"} into the Params field, replacing <url> with the actual url of the website. 
#### Slider 
1. Type `page://slider` into the App Field
2. Enter {"json":["<url>","<url>",..."<url>"]} into the Params field, replacing <url> with the actual url of the image. 
#### Charts 
Currently there are 6 available chart types: bar, hbar, line, linearea, pie and circle. 
1. Type `page://chart` into the App Field
2. Enter into the Data Field: `{"chart":{"type":"line","title":"Sample Chart","data":{"columns":[{"type":"x","field":"field name","name":"Course name"},{"type":"y","field":"numerical weight","name":"measured aspect"}],"rows":[{"numerical weight":450,"field name":"A"},{"numerical weight":350,"field name":"B"},{"numerical weight":300,"field name":"C"},{"numerical weight":370,"field name":"D"},{"numerical weight":400,"field name":"E"}]}}}`
3. Replace ”type”,“numerical_weight”, “field_name” and other content to make your customized charts. 

![](https://i.imgur.com/Rht0Sxn.png)
https://git.page/jj/board?qname=chart for charts demo. <br>
To view the panels data content samples, refer to these boards that can be found in the public board list:
- QName= chartpractice, QCode=1611802967946
- 

#### Cloud Room Display 
* Type `page://room` into the App Field and {"tag":"<tag>"} into the 
Params field, replacing <tag> with your own room flow tag or 

* Type `page://panel` into the App Field and {"tag":"<tag>"} into the 
Params field, replacing <tag> with your own panel flow tag. 
#### Bricks 
Just paste the url of the brick into the App Field. 

See the jboard with the QName jbrick and go to https://git.page/jj/board?qname=jbrick for bricks demo 

![](https://i.imgur.com/xXEWyUx.png)

#### View  (log)
1. Create a flow in fbuilder and set the destination to your view name 
2. Type `page://view` into the App Field.
3. Enter {"tag":"<view name>"} into the Params field, replacing <view name> with your view name 

#### Header 
1. Type `page://header` into the App Field.
2. Enter {"title":"<title>","logo":"<url>"} into the Params field, replacing <title> with the title you want for the header and <url> with the url of the logo icon. 


## Copy and Pasting jBoard Data 
You can save your jBoard data in json format. 
1. Click on the icon on the upper right hand corner <img src="https://i.imgur.com/9f04Grd.png" width=30 height=30> to go to view data in json format. 
2. Then click on the <img src="https://i.imgur.com/g8XRamN.png" width=35 height=30> icon if you want to copy the current jboard in json format, or the <img src="https://i.imgur.com/7ULwkwQ.png" width=35 height=30> icon if you want to paste the jboard data in json format.

![](https://i.imgur.com/IX55C81.png)

## Displaying a jBoard 
There are 2 ways of displaying your jBoard: 
- View in json format, then in a new window 
  1. Click on the <img src="https://i.imgur.com/9f04Grd.png" width=30 height=30> icon to go to view data in json format 
  2. Then on the upper right hand corner click on the <img src="https://i.imgur.com/PeKirIV.png" width=32 height=30> icon then your jboard will be displayed in a new window. 
- jBoard URL
  1. To display your jboard using a url link, you need to get either the QName or the QCode of your jboard. To do so , click on the icon on the upper right hand corner. 
  2. Select `public` or `private` see a list of all jboards with their corresponding QName and QCode. 

![](https://i.imgur.com/VeH6N1a.png)

3. To display using the QName enter https://git.page/jj/board?qname=QName in the browser, replacing the `QName` with your jboard’s QName; to display using the QCode enter https://git.page/jj/board?qcode=QCode in the browser, replacing the `QCode` with your jboard’s QCode.

## Dock Builder User Manual 
A dock board consists of a series of jboards. 
In a dock board, you can navigate from one jboard to another using the dock menu on the bottom, much like the Mac OS Desktop. 
An example of what a dock can look like: 

![](https://i.imgur.com/gBYGHpz.png)

How to Access Dock Builder: 
1. From jBuilder, click on the <img src="https://i.imgur.com/BwmKrTz.png" width=33 height=30> icon on the upper left hand corner to go to dock builder. To leave the dock builder and go back to jbuilder, click the <img src="https://i.imgur.com/HopFYkU.png" width=35 height=30> icon

## Dock Builder UI: 

### Adding and Removing jBoards from the Dock: 
In the Dock Builder, click the <img src="https://i.imgur.com/zSqxjF9.png" width=30 height=30> icon on the bottom for the Dock Add window to pop up. 

![](https://i.imgur.com/NOzmfEH.png)

1. Assign a name to the board inside the Title field (If you don’t assign a name, you cannot add a jboard to the dock, or delete the dock itself, i.e. you’ll have to restart the whole dock board)
2. Enter the url of the icon image you want to use for the current board.
3. For the Icon Url field enter the url of the dock menu image icon you want to use for the board when it is unselected. 
4. For the Active Icon Url field enter the url of the dock menu image icon you want to use for the board when it is selected. 
(For nice icons, consider searching at flaticon.com. Simply search by keyword, click on an icon, right click and select ‘Copy Image Address’, then paste.) 
5. Hit Confirm after you are done. 

<img src="https://i.imgur.com/waoVikf.png" alt=add-dock width=736 height=415>

6. To add the jboard, click on the icon in the middle of the page, and select the board you want to link. If you want to remove the current board, click on the icon <img src="https://i.imgur.com/IKBMLKZ.png" width=35 height=30>. To remove the jboard panel from the dock menu, remove the existing jboard, then click the <img src="https://i.imgur.com/M275YXb.png" width=33 height=30> icon in the middle of the panel. 


### Saving a Dock 
Always remember to save your dock. To save a dock, click on the <img src="https://i.imgur.com/TJUZUG1.png" width=35 height=30> icon on the upper right hand corner. Enter a name and hit Save. 

### Copy and Pasting Dock Data 

You can save your dock data in json format. 
1. Click on the <img src="https://i.imgur.com/9f04Grd.png" width=30 height=30> icon on the upper right hand corner to go to view data in json format. 
2. Then click on the <img src="https://i.imgur.com/g8XRamN.png" width=35 height=30> icon if you want to copy the current dock layout in json format, or the <img src="https://i.imgur.com/7ULwkwQ.png" width=35 height=30> icon if you want to paste the dock data in json format.

### Displaying a Dock 
There are 2 ways of displaying your dock: 

- View in json format, then display in a new window 
1. Click on the <img src="https://i.imgur.com/9f04Grd.png" width=30 height=30> icon to go to view data in json format 
2. Then on the upper right hand corner click on the <img src="https://i.imgur.com/PeKirIV.png" width=32 height=30> icon then your dock will be displayed in a new window. 

- jBoard URL
1. To display your dock using a url link, you need to get either the QName or the QCode of your dock. To do so , click on the <img src="https://i.imgur.com/rNDVXuk.png" width=30 height=30> icon on the upper right hand corner. 
2. Here you can select to view the list of your private docks or the public docks with their corresponding QName and QCode. 
3. To display using the QName enter 
https://git.page/jj/jboard?qname=QName in the browser, replacing the `QName` with your dock’s QName; to display using the QCode enter https://git.page/jj/jboard?qcode=QCode in the browser, replacing the `QCode` with your dock’s QCode.
