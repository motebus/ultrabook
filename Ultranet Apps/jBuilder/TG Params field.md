# page://tg Params field
### Basic variables
You must use these variables for page://tg to work
* "id":"tg-group-chat-id"
  * Example: `"id":"-1234567891234"`
* "type":"xxx"
  * Types available: youtube, photo, text, url, pdf, md, 360, video
  * Example: `"type":"youtube"`
* "count":"xx"
  * Example: `"count":"10"`

 ### Other frequently used variables
 * "title":"#xxx"
   * Example: `"title":"#note"` 
 * "tag":"{xxx}"
   * Example: `"tag":"{weekly}"`
   * For multiple tags: `"tag":"{weekly | tdl | ypcloud}"`
 * "caption":"x"
   * Where x is: `yes` or `no`
   * Example: `"caption":"yes"`
* "play":"xxx"
   * Where xxx is `slide` or `list`
   * Example: `"play":"slide"`
* "dark":"xx"
   * Where x is: `yes` or `no`
   * Example: `"dark":"yes"

### Examples:
1.<img src="https://i.imgur.com/MphRaRD.png" width=428 height=500>
```
{"id":"-1001259349556,-1001259349556,-1001259349556,-1001259349556,-1001259349556,-1001259349556,-1001259349556,-1001259349556","title":"Photo,Youtube,Text,URL,PDF,MD,360,Video","type":"photo,youtube,text,url,pdf,md,360,video","count":"20,10,30,20,5,5,5,10","caption":"yes","play":"slide"}
```
2.<img src="https://i.imgur.com/9CLF8rJ.png" width=428 height=500>
```
{"id":"-1001259349556,-1001259349556,-1001259349556,-1001259349556,-1001259349556,-1001259349556","title":"#coffee,#hr,#note,#weekly,#event,#yp","type":"youtube,photo,text,photo,photo,youtube","tag":"{coffee},{hr},{note},{weekly},{event},{yp}","count":"10,20,30,20,20,10","caption":"no","play":"slide"}
```
3.<img src="https://i.imgur.com/i2749Wc.png" width=428 height=500>
```
{"id":"-523456788","type":"photo","count":"50","play":"slide"}
```


