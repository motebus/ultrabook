## How to use jujue-app search bar
* It accept 3 kind of symbol //, @@, >>
![](https://i.imgur.com/e1xV56s.png)
## Symbol //  (It will direct to a new web page for new function
### //urt (to test if your backend is working
![](https://i.imgur.com/CIHZyif.png)
* Get the DDN you want to test from [iocwatch](https://iocwatch.ypcloud.com)
* Then fill in your topic & payload 
* DDN example: >test/test-app or >hub/comm
* Topic example: test://test or 123
* payload can be empty
### //obj -> objstore 
![](https://i.imgur.com/F936A1K.png)
* You can upload your flow json here
1. Use Export in fbuilder to copy your flow json to clipboard first 
2. Click the "+"
3. Click the "P" (If P button doesn't work then paste all your json in the "data" filed
4. Change your title & name & qname according to your need
5. Click the check icon on top right to save
6. Refresh the page and you will see your file
Note:
* Choose public or private on the left hand side, in public you can see and copy others flow, in private you will only see flows of your own
* On the right hand side can choose the directory you want ex: flow, obj, json,etc
### //bucket -> s3 minio
![圖片](https://user-images.githubusercontent.com/77911816/174707920-23cb9a8d-85dd-41aa-9d16-93702a24c775.png)
* You can upload your file in to a specific bucket
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
### //upload
![圖片](https://user-images.githubusercontent.com/77911816/174707999-0e45a0c0-44ef-4ca4-8257-19cde2a00732.png)

