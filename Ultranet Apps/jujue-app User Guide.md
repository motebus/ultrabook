# Jujue App User Guide
https://jujue.app 

aka Jujue Browser

An IoT Browser

<img src="https://i.imgur.com/IoaEtzl.png" width=870 height=488>

## Jujue App Drawer
Open by selecting the app drawer icon ![](https://i.imgur.com/N2RDrgB.png) on the top-right of the homepage.
From here you can access all YPCloud apps.

Note: some apps will only be available once you login. 

## Jujue Live
Open by select the message icon <img src="https://i.imgur.com/5rRd56T.png" width=24 height=19> on the top-left of the homepage.

<img src="https://i.imgur.com/F3AKedY.png" width=600 height=300>

## How to use the Jujue search bar
* It accepts 3 kinds of symbols `//`, `@@`, `>>`

![](https://i.imgur.com/e1xV56s.png)

* `//` directs to a new web page with a specific function
* `@@` is used to send messages to devices and virtual twins/assistants. It indicates the recipient of your messages or commands. A single `@` indicates you are addressing a person, while `@@` is used to address "things". 
* `>>` (tbc)

Clicking on the <img src="https://i.imgur.com/6K4NCnH.png" width=20 height=22> icon on the right to the search bar opens page shortcuts. <br> (This is still just a prototype)

<img src="https://i.imgur.com/WaDyA3X.png" width=400 height=200>


## page // 

### //urt 
Function: to test if your backend is working

![](https://i.imgur.com/CIHZyif.png)

* Get the DDN you want to test from [iocwatch](https://iocwatch.ypcloud.com)
* Then fill in your topic & payload 
* DDN example: >test/test-app or >hub/comm
* Topic example: test://test or 123
* payload can't be empty

### //obj
Function: object storage

![](https://i.imgur.com/F936A1K.png)

* You can upload your flow json here
1. Use Export in fbuilder to copy your flow json to clipboard first 
2. Click the "+"
3. Click the "P" (If P button doesn't work then paste all your json in the "data" filed
4. Change your title & name & qname according to your needs
5. Click the check icon on the top-right to save
6. Refresh the page and you will see your file

Note:
* Choose public or private on the left hand side, in public you can see and copy others flow, in private you will only see flows of your own
* On the right hand side can choose the directory you want ex: flow, obj, json,etc
* If you need to copy others flow just click second button(copy button) on the left, the json in "data" field will be copy to your clipboard
* "Trash can" button is for deletion please be careful

### //bucket
Function: s3 minio

![圖片](https://user-images.githubusercontent.com/77911816/174707920-23cb9a8d-85dd-41aa-9d16-93702a24c775.png)

* You can upload your file into a specific bucket

1. Select buckets on the right hand side that you need
2. Click the "+" after bucket choosen
3. Enter object name and choose/drop the file you want to upload from your pc
4. If the object name you are using already exist please change it or make sure you want to replace the file
5. Refresh the page and your file will be shown 

Note:
* It may take 2.3 minutes for all the buckets to be shown on the bucket page, please be patient
* If bucket doesn't show for more then 5 mintues please ask for help
* If you are replacing the file please check if the upload time is new
* If you need to create a new bucket please ask for help
* If you need to delete a specific file please ask for help

### //upload
Function: general image hosting (s3)
![圖片](https://user-images.githubusercontent.com/77911816/174707999-0e45a0c0-44ef-4ca4-8257-19cde2a00732.png)

* Upload files to drop to SmartScreen, or upload to create image URLs

This page can also be reached via ![](https://i.imgur.com/V6EeP2K.png) on the top-right of the homepage. 

### //nearby
Function: manage nearby devices

This page can also be reached via ![](https://i.imgur.com/EbN8y43.png) on the top-right of the homepage. 


