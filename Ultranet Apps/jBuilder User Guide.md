# jBuilder User Guide
jbuilder is used to build jboards. 

## Table of Contents
jBuilder
Dock Builder


### Access jBuilder: 
1. To login to jbuilder, you need a Jujue account. If you don't have one yet, register at account.ypcloud.com
2. Go to jbuilder.ypcloud.com 
3. Afterwards, sign into jbuilder. If you can't sign in, ask someone for help

## jBuilder UI: 
In the left hand side the user can define the board grid by specifying the number of columns and rows and enable/disable header/footer of the board frame. 

*The grid serves as the framework for the board’s layout and helps us manage the proportions between elements aligned on the board. The columns on the grid (not necessarily visible) will shrink and expand as you resize the browser window, enabling us to design for screens across different types of digital devices (responsive design in a multi-device landscape).*

The icons in the upper right corner allows the user to add panels , refresh window , view data in json format , view the board list , and view 
user’s information . 
![image alt](https:// "title" =WidthxHeight)

## Creating a jBoard: 
1. Click on add panels icon on the upper right hand corner to add panels . 
2. Click on the pencil icon to edit the panel.
3. In the Width and Height fields you can specify the dimension of the panel. 
4. Assign a name to the panel inside the Name field. 
5. Enter an url inside the App field to specify the type of frame-style for the panel. * See a list of available types further below.  
6. Hit Confirm after you are done. 

## Saving a jBoard 
1. Always remember to save your jboard. You need to save it first before you can display it. To save a jboard, click on the icon on the upper right hand corner. Enter a name and hit Save. The name entered will be the QName of your jboard. 
*This name cannot be changed

## Available Types of Frame-Style 
#### Web Page 
A. Just paste the url into the App Field or 
B. Type page://url into the App Field and {"url":"<url>"} into the Params field, replacing <url> with the actual url of the website. 
#### YouTube Video 
Just paste the url into the App Field.
Create live channels by putting Youtube Videos with live sessions. (create the option to directly switch between channels on a jboard)
#### Image 
A. Just paste the url into the App Field or 
B. Type page://url into the App Field and {"url":"<url>"} into the Params field, replacing <url> with the actual url of the website. 
#### Slider 
A. Type page://slider into the App Field and 
{"json":["<url>","<url>",..."<url>"]} into the Params field, replacing <url> with the actual url of the image. 
#### Charts 
Currently there are 6 available chart types: bar, hbar, line, linearea, pie and circle. 

![image alt](https:// "title" =WidthxHeight)

Type page://chart into the App Field and 
>{"chart":{"type":"line","title":"Chart","data":{"columns":[{"type":"x","field":"fiel d_name","name":"Course Name"},{"type":"y","field":"numerical_weight","name":"measured_aspect"}],"rows":[{"numerical_weight":450,"field_name":"A"},{"numerical_weight":350,"f ield_name":"B"},{"numerical_weight":300,"field_name":"C"},{"numerical_weig ht":400,"field_name":"D"}]}}} 

into the Data field, replacing”type”,“numerical_weight” and “field_name” content to make your customized charts. 

You could also see the jboard with the QName chart and go to 
https://git.page/jj/board?qname=chart for charts demo

*Data:{"chart":{"type":"line","title":"Sample Chart","data":{"columns":[{"type":"x","field":"field name","name":"Course name"},{"type":"y","field":"numerical weight","name":"measured aspect"}],"rows":[{"numerical weight":450,"field name":"A"},{"numerical weight":350,"field name":"B"},{"numerical weight":300,"field name":"C"},{"numerical weight":370,"field name":"D"},{"numerical weight":400,"field name":"E"}]}}}

#### Cloud Room Display 
A. Type page://room into the App Field and {"tag":"<tag>"} into the 
Params field, replacing <tag> with your own room flow tag or 
B. Type page://panel into the App Field and {"tag":"<tag>"} into the 
Params field, replacing <tag> with your own panel flow tag. 
#### Bricks 
Just paste the url of the brick into the App Field. 
See the jboard with the QName jbrick and go to 
https://git.page/jj/board?qname=jbrick​ for bricks demo 
![image alt](https:// "title" =WidthxHeight)

#### View  (log)
1. Create a flow in fbuilder and set the destination to your view name 2. Type page://view into the App Field and {"tag":"<view name>"} into the Params field, replacing <view name> with your view name 
#### Header 
Type page://header into the App Field and {"title":"<title>","logo":"<url>"} into the Params field, replacing <title> with the title you want for the header and <url> with the url of the logo file


## Copy and Pasting jBoard Data 
You can save your jBoard data in json format. 
1. Click on the icon on the upper right hand corner to go to view data in json format. 
2. Then click on the icon if you want to copy the current jboard in json format, or the icon if you want to paste the jboard data in json format.

![image alt](https:// "title" =WidthxHeight)

## Displaying a jBoard 
There are 2 ways of displaying your jBoard: 
A. 
1. Click on the ![] icon to go to view data in json format 
2. Then on the upper right hand corner click on the ![] icon then your jboard will be displayed in a new window. 

B. 
1. To display your jboard using a url link, you need to get either the QName or the QCode of your jboard. To do so , click on the icon on the upper right hand corner. 
2. Enter p: or p:// in the search bar to see a list of all the jboards with their corresponding QName and QCode. 

![image alt](https:// "title" =WidthxHeight)

3. To display using the QName enter https://git.page/jj/board?qname=<QName> in the browser, replacing the <QName> with your jboard’s QName; to display using the QCode enter https://git.page/jj/board?qcode=<QCode> in the browser, replacing the <QCode> with your jboard’s QCode.

# Dock Builder User Manual 
A dock board consists of a series of jboards. 
In a dock board, you can navigate from one jboard to another using the dock menu on the bottom, much like the Mac OS Desktop. 
An example of what a dock can look like: 

How to Access Dock Builder: 
1. From jBuilder, click on the icon on the upper left hand corner to go to dock builder. To leave the dock builder and go back to jbuilder, click the home icon

## Dock Builder UI: 

### Adding and Removing jBoards from the Dock: 
In the Dock Builder, click the icon on the bottom. 
1. Assign a name to the board inside the Title field (If you don’t assign a name, you cannot add a jboard to the dock, or delete the dock itself, i.e. you’ll have to restart the whole dock board)
2. Enter the url of the icon image you want to use for the current board.
3. For the Icon Url field enter the url of the dock menu image icon you want to use for the board when it is unselected. 
4. For the Active Icon Url field enter the url of the dock menu image icon you want to use for the board when it is selected. 
(For nice icons, consider searching at flaticon.com. Simply search by keyword, click on an icon, right click and select ‘Copy Image Address’, then paste.) 
5. Hit Confirm after you are done. 
6. To add the jboard, click on the icon in the middle of the page, and select the board you want to link. If you want to remove the current board, click on the icon. To remove the dock menu (image icon), click the (-) icon in the middle of the page after removing the existing jboard. 

### Saving a Dock 
1. Always remember to save your dock. To save a dock, click on the icon on the upper right hand corner. Enter a name and hit Save. 
Copy and Pasting Dock Data 
You can save your dock data in json format. 
1. Click on the icon on the upper right hand corner to go to view data in json format. 
2. Then click on the icon if you want to copy the current dock layout in json format, or the icon if you want to paste the dock data in json format.

### Displaying a Dock 
There are 2 ways of displaying your dock: 
A. 
1. Click on the icon to go to view data in json format 
2. Then on the upper right hand corner click on the icon then your dock will be displayed in a new window. 
B. 
1. To display your dock using a url link, you need to get either the QName or the QCode of your dock. To do so , click on the icon on the upper right hand corner. 
2. Enter p: or p:// in the search bar to see a list of all the docks with their corresponding QName and QCode. 
3. To display using the QName enter 
https://git.page/jj/jboard?qname=<QName> in the browser, replacing the <QName> with your dock’s QName; to display using the QCode enter https://git.page/jj/jboard?qcode=<QCode> in the browser, replacing the <QCode> with your dock’s QCode.


###### tags: `yp-md`
