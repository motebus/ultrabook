# Ultranet Topic 

## Mote
| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| mote://bash            | Control the device sudch like ssh | {"token":"xxx", "command":"ls"} |
| mote://xstorage        | Operate xstorage | {"method":"setConfig,getConfig,changeEiName,getBucket,setBucket,listBucket,removeBucket", "catalog":"CatalogName", "idname": "IDName", "data":"Content"} |
| mote://nearby          | Search near device | {} |
| mote://drop            | Drop file to other device | {"method":"ls,cp,rcp,cat,rm", "DDN":"xxxx", "path": "path", "files":"filename", "fsize":"123"} | 
| mote://shot            | Screen capture | {} |
| mote://measure         | Check system information | {"method":"info,status"} |
| mote://qsnap           | Computing deploy | {"type": "fbots,aibots", "operate":"list,run,restart,checkAlive,stop,start,delete,open,close", "svcName":"name", "startTime":"2021/06/04-12:0:0", "stopTime":"2021/06/04-16:0:0", "MCHAT_EINAME":"flowbot", "MCHAT_APPNAME":"flowbot-app", "MCHAT_UDID":"1", "MCHAT_DC":"dc", "MCHAT_IOC":"ioc", "MCHAT_WATCHLEVEL":"0", "FBOT_UI":"1", "FBOT_QCODE":"123", "FBOT_FLOWFILE":"", "FBOT_QNAME":"flowbot", "FBOT_MODE":"xstorage", "FBOT_PORT":"18888", "svcSource":"", "modelName":"", "modelSource":"", "parameter":""} |
| mote://apt             | Package management | {"operate":"list,remove,install","type":"snap,apt,npm","packageName":"wmctrl","keyword":"w*"} |
| mote://time            | Timezone setting | {"method":"now,listTimezone,setTimezone","zone":"Asia/Taiwan","keyword":"Asia"} |
| mote://setUser         | User information setting | {"EiTag":"#YP","EiLoc":"Taiwan"} |
| mote://getUser         | User information getting | {} |
| mote://listPeripherals | List peripherals | {"device":"usb,camera,ip,screen","update":true} |
| mote://env             | Process environment parameter | {"method":"read,create,append,update,delete","path":"fbot/test.env","content":["QQ=123","WW=123"]} |
| mote://schedule        | Make schedule | {"operate":"list,create,delete,start,stop","type":"once,routine,boot","hour":"2","minute":"1","month":"1","day":"1","week":"1","command":"ls","job":"qq","workspace":"0","terminal":"0"} |
| mote://window          | Operate window | {"operate":"list,assign,move,change","service":"0x123","key":"pointer","workspace":"0"} |
| mote://keybot          | Define keybot shortcut | {"device": "numPad","shortcuts": {"0": "Mic","1": "Workspace1","2": "Workspace2","3": "Workspace3","4": "Workspace4","5": "Super","6": "Workspace0","7": "Sceenshot","8": "Window","9": "Screencast","/": "Switch","*": "Mute","+": "Volume+","-": "Volume-"}} |
| mote://audio           | Operate audio | {"operate":"adjust,list,change","volume":"+5,50","device":"alsa_xxx","port":"linein","audio":"sink,source"} |
| mote://shortcut        | Manage GNOME shortcut | {"operate":"list,get,set,reset","func":"mic-mute","key":"KP_1"} |
   

## Qbix
### mpodman
   
 | <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
   | helm://list      | list releases (= mpod_name)| {"namespace":"default"} |
   | helm://create    | create a new chart_name with the given mpod_name. There are **5** kinds of chart_name  written in "mpodman/xxxx". (xxxx can be **fbuilder, sscreen, ioc, fbots** or **webmms-srv**) | { "releaseName": "fbots", "chartName": "mpodman/fbots", "namespace": "default", "values": { "MCHAT_EINAME": "fbots-example", "MCHAT_APPNAME": "fbots-example-app", "FBOT_QNAME": "comm", "fbots.ingress.enabled": "true", "fbots.ingress.hosts[0]": "yh.ypcloud.com", "fbots.ingress.path": "/fbots/(.*)" } } |
   | helm://delete    |  uninstall a release | { "releaseName": "fbots", "namespace": "default" } |
   | helm://update    | update a new chart_name with the given mpod_name. There are **5** kinds of chart_name  written in "mpodman/xxxx". (xxxx can be **fbuilder, sscreen, ioc, fbots** or **webmms-srv**) | { "releaseName": "fbots", "chartName": "mpodman/fbots", "namespace": "default", "values": { "MCHAT_EINAME": "fbots-example", "MCHAT_APPNAME": "fbots-example-app", "FBOT_QNAME": "comm", "fbots.ingress.enabled": "true", "fbots.ingress.hosts[0]": "yh.ypcloud.com", "fbots.ingress.path": "/fbots/(.*)" } } |
   | helm://get       | download extended information of a named release  | { "releaseName": "fbuilder", "namespace": "default", "subCommand": "all" } |
   | helm://history   | fetch release history | { "releaseName": "fbuilder", "namespace": "default" } |
   | helm://rollback  | roll back a release to a previous revision | { "releaseName": "fbuilder", "namespace": "default" } |
   | helm://status    | display the status of the named release  | { "releaseName": "fbuilder", "namespace": "default" } |
   | kubectl://deletePod | delete resources by filenames, stdin, resources and names, or by resources and label selector | { "pod_name": "mpod-810moj7dp6e-0", "namespace": "default" } |
   | kubectl://getPod | read the specified Pod | { "pod_name": "mpod-810moj7dp6e-0", "namespace": "default" } |
   | kubectl://getPodLog | read log of the specified Pod | {"pod_name":"mpod-810moj7dp6e-0","namespace":"default","container":""} |
   | kubectl://listPod | list or watch objects of kind Pod | {"namespace":"default"} |
   | kubectl://createNamespace | create a Namespace | {"namespace":"system"} |
   | kubectl://deleteNamespace | Delete a Namespace | {"namespace":"system"} |
   | kubectl://getNamespace | read the specified Namespace | {"namespace":"system"} |
   | kubectl://listNamespace | list or watch objects of kind Namespace | {} |   
  
### qman
**1. qbix**

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| qbix://list   | list objects kind of qbix | { "site_name": "h1-qbix", "qbix_type": "qoci", "payload": {} } |
| qbix://run    | run a qbix | { "site_name": "h2-qbix", "qbix_type": "qoci", "payload": {  } } |
| qbix://add    | add a qbix | { "site_name": "h2-qbix", "qbix_type": "qoci", "payload": {  } } |
| qbix://delete | delete specified qbix | { "site_name": "h2-qbix", "qbix_type": "qoci", "payload": {  } } |
| qbix://get    | read the specified qbix | { "site_name": "twcc-qbix", "qbix_type": "twcc", "payload": { } } |
| qbix://pod    | read the pod info of specified qbix | { "site_name": "twcc-qbix", "qbix_type": "twcc", "payload": { } } |
| qbix://image  | list objects kind of image | { "site_name": "twcc-qbix", "qbix_type": "twcc", "payload": { } } |
| qbix://size   | list object kind of size | { "site_name": "twcc-qbix", "qbix_type": "twcc", "payload": { } } |
| qbix://notify | notify qbix | {"container":"","status":""} |

**2. qman**

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| qman://list   | list objects kind of qsite | {} |
| qman://run    | run a qbix | { "site_name": "any-qbix", "qbix_type": "any", "payload": { } } |
| qman://delete | delete specified qbix | { "site_name": "any-qbix", "qbix_type": "any", "payload": { } } |

**3. qociman**

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| qociman://run | run a new container | {"image": "motebus/fbots:latest","container_name": "test","network_mode": "host","restart": "always","ports": {"1880": "1880"},"env": {"MCHAT_MBGWIP": "127.0.0.1","MCHAT_DC": "dc","MCHAT_IOC": "ioc","MCHAT_UDID": "0","MCHAT_WATCHLEVEL": "1","MCHAT_APPNAME": "test-app","MCHAT_EINAME": "test","FBOT_QNAME": "","FBOT_QDATA": "","FBOT_QTYPE": "","FBOT_QCODE": "","FBOT_UID": "","FBOT_MANY": "1","FBOT_CLUSTER": "0","FBOT_MULTI": "0","FBOT_MODE": "xstorage","FBOT_UI": "0","FBOT_FLOWFILE": "","FBOT_REST": "1","FBOT_PORT": "1880","TZ": "Asia/Taipei"}} |
| qociman://add | add a new container | {"image": "motebus/fbots:latest","container_name": "test","network_mode": "host","restart": "always","ports": {"1880": "1880"},"env": {"MCHAT_MBGWIP": "127.0.0.1","MCHAT_DC": "dc","MCHAT_IOC": "ioc","MCHAT_UDID": "0","MCHAT_WATCHLEVEL": "1","MCHAT_APPNAME": "test-app","MCHAT_EINAME": "test","FBOT_QNAME": "","FBOT_QDATA": "","FBOT_QTYPE": "","FBOT_QCODE": "","FBOT_UID": "","FBOT_MANY": "1","FBOT_CLUSTER": "0","FBOT_MULTI": "0","FBOT_MODE": "xstorage","FBOT_UI": "0","FBOT_FLOWFILE": "","FBOT_REST": "1","FBOT_PORT": "1880","TZ": "Asia/Taipei"}} |
| qociman://delete | remove one container | {"container":"qx-xxx-jujue"} |
| qociman://get | read the specified container | {"container":"qx-xxx-jujue"} |
| qociman://list | list containers | {"filters":{"name":["free"]}} |
| qociman://restart | restart the specified container | {"container":"qx-xxx-jujue"} |   
| qociman://start | start the specified container | {"container":"qx-xxx-jujue"} |   
| qociman://stop | stop the specified container | {"container":"qx-xxx-jujue"} |   
| qociman://status | read status of specified container | {"container":"qx-xxx-jujue"} |      

## Ultra

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| portal://log   | Create the log record into odoo including 4 fields(name, time, fm, and mesaage) |  { "voucher":"(voucher of model)","act":"(tg id)","data":{"name":"(your name)","message":"(message)"} } | {ErrCode:0,ErrMsg:"OK",Reply} |
| portal://event | Create the event record into odoo | { "voucher":"(voucher of model)","act":"(tg id)","data":{"(model field)":"(data)"} }  | {ErrCode:0,ErrMsg:"OK",Reply} |
| portal://cost  | Create the cost record  | { "voucher":"(voucher of model)","act":"(tg id)","data":{"(model field)":"(data)"} }  |{ErrCode:0,ErrMsg:"OK",Reply} |
| portal://form  | Create detail data list of device or equipment into odoo |  { "voucher":"(voucher of model)","act":"(tg id)","data":{"(model field)":"(data)"} }  | {ErrCode:0,ErrMsg:"OK",Reply} |
| query://model  | Query data  | { "voucher":"(voucher of model)","data":{"query_str":["(model field)","=","(data value)"],"query_rst":["(field name you want to query)"]} }   |   {ErrCode:0,ErrMsg:"OK",Reply{id:(id number),"(field name you typing)":"(data)"}} |
   
## Jujue

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| ss://drop | Show image or video on screen | {"cmd":"drop","type":"url","src":["(url1)","(url2)"],"duration":"(duration)","frame":"(frame)","animate":"(animate)","aniduration":"(animate duration)","pmode":"(play mode)" ,"bgcolor":"(background color)"} |      |
| ss://notify | Show a notification message | {"cmd":"notify","msg":"(message)","duration":"(duration)","color":"(color)":"size":"(size)"} |      |
| ss://toast | Show a toast message | {"cmd":"toast","msg":"(message)","heading":"(heading)","icon":"(icon)":"transition":"(transition)","duration":"(duration)"} |   |   
| ss://marquee | Show a marquee text | {"cmd":"marquee","msg":"(message)","duration":"(duration)","color":"(color)":" size":"(size)","bgcolor","(background color)"} |     |
| ss://text | Show text to screen | {"cmd":"text","msg":"(text)","duration":"(duration)","color":"(color)","size":"(siz e)","bgcolor":"(background color)","align":"(text alignment)","frame":"(frame)","animate":"(animate)","aniduration":"(animate duration), "bgcolor":"(background color)"} |     |
| ss://app | Show a website on screen | {"cmd":"app","url":"(url1)","duration":"(duration)","frame":"(frame)"} |   |
| ss://youtube | Show a youtube program on screen | {"cmd":"youtube","search":"(search string","duration":"(duration)","frame":"(frame)","pmode":"(play mode)"} |   |
| ss://touch | Control sscreen | {"cmd":"touch","option":"(arg) ","value":"(argv)"} |   |
| ss://status | Show status of sscreen | {"cmd":"status","option":"(arg) ","value":"(argv)"} |  |
| ss://dj |   | {"cmd":"dj","option":"(arg) ","value":"(argv)"} | |
| watch://event  |            |        |      |
| comm://tg      | send message to tg group with pinponboy |{"type": "message","content": "","from": "pinponboy"} |
| mod://play     |            |        |      |
| filter://chart |            |        |      |

## Others
 
| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| auto://      |            |        |
| pd://        |            |        |
| play://      |            |        |
   
   
### Object store
**1. file**

| <div style="width: 150px">topic | <div style="width: 230px">description | <div style="width: 100px">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| file://addbucket    | Create bucket | { "bucket":"(bucket name)" }   |  {"ErrMsg":"OK"} |
| file://deletebucket | Delete bucket | { "bucket":"(bucket name)" } } |  {"ErrMsg":"OK"} |
| file://listbucket   | List bucket | {} |  {"ErrMsg":"OK","Data":[{"name":"","creationDate":"2020-07-21T03:16:01.841Z"}]} |
| file://set          | Create object |         | {"ErrMsg":"OK","Data":"545c3ce0b22b570d3073e3b15ba9d157"} |
| file://get          | Get object | { "bucket":"(bucket name)", "object":"(object name)", "filetype":"url" } | {"ErrMsg":"OK","Data":"https://s3.ypcloud.com/bucket name/..... "} |
| file://delete       | Delete object | { "bucket":"(bucket name)", "object":"(object name)" } |  {"ErrMsg":"OK"}  |
| file://list         | List object | { "bucket":"(bucket name)", "object":"(object name)" }   |  {"ErrMsg":"OK","Data":[{"name":"","creationDate":"2020-07-21T03:16:01.841Z"}]}  |

**2. obj**

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| obj://add    | Insert object | { "name":"(object name)", "data":{} } | {"ErrMsg":"OK","Data":{"oid":"object oid","access":"public","_id":"","name":"object name","data":{}, updateDate":"2021-06-03T08:17:01.996Z","insertDate":"2021-06-03T08:17:02.004Z","__v":0}} |
| obj://set   | Update object |{ "oid":"(object oid)", "name":"(object name)", "data":{} }| {"ErrMsg":"OK","Data":{}}  |
| obj://delete | Delete object | { "oid":"(object oid)" } |  {"ErrMsg":"OK","Data":{"n":0,"ok":1,"deletedCount":0}} |
| obj://list   | List object | { "oid":"(object oid)" } | {"ErrMsg":"OK","Data”:{[]}}} |
| obj://get   | Get object | { "oid":"(object oid)" } |  {"ErrMsg":"OK","Data”:{}}} |


### comm

| <div style="width: 230pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| mail://address     | Send msg by mail |{ "content":"(mail content)", "subject":"(mail subject)" } | {<br>"ErrCode": 0,<br>"ErrMsg": "OK"<br>}  |
| sms://phone number | Send msg by sms | { "text":"(sms content)" } | {<br>"ErrCode": 0,<br>"ErrMsg": "OK"<br>} |
| tg://chat id      | Send msg by tg | { "content":"(telegram content)", "type":"(send method)", available type:["message", "photo", "audio", "document", "video", "animation", "voice", "sticker"], default is "message", "from":"(telegram bot name)", available bot:["pinponboybot", "jujuebot", "lovetubebot", "ypcloudbot", "ultravisorbot", "smartscreenbot"], default is "pinponboy", "cc": "(chat_id of cc)"(optional), "parse_mode":"MarkdownV2" (optional) } | {<br>"ErrCode": 0,<br>"ErrMsg": "OK"<br>}  |
| ioc://chat id      | Send msg by tg with IOC format |{ "content":"(telegram content)", "from":"(telegram bot name)", "to":"(to_name)", "cc": "(chat_id of cc,options)" } | {<br>"ErrCode": 0,<br>"ErrMsg": "OK"<br>} |
| git://chat id     | Send msg to tg from git | { "content":"(telegram content)", "from":"(telegram bot name)", "to": "(to_name)", "cc": "(chat_id of cc,options)" }  | {<br>"ErrCode": 0,<br>"ErrMsg": "OK"<br>} |
| console://chat id | Send object msg | { "content":"(telegram content)", "from":"(telegram bot name)", "to":"(to_name)", "cc":"(chat_id of cc,options)" } | {<br>"ErrCode": 0,<br>"ErrMsg": "OK"<br>}  |
| watch://chat id     | Send msg from watch | { "sub":"(watch sub)", "data":"(telegram content)" } | {<br>"ErrCode": 0,<br>"ErrMsg": "OK"<br>} |
| mpod://chat id     | Send msg from mpod | { "content":"(telegram content)", "from":"(telegram bot name)", "to":"(to_name)", "cc":"(chat_id of cc,options)" } | {<br>"ErrCode": 0,<br>"ErrMsg": "OK"<br>}  |
| log://username   | Send msg to logmms | { "text":"content", "uid":"user id(optional)" } | {<br>"ErrCode": 0,<br>"ErrMsg": "OK"<br>}  |
| view://username  | Send msg to page://view |{ "text":"content" } |{<br>"ErrCode": 0,<br>"ErrMsg": "OK"<br>} |


### sys

**In Function List**
| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| in://local | Ping to local motechat | ping | [{IN:{From,To,State},Reply}] |
| in://dc |	Ping to DC | ping | [{IN:{From,To,State},Reply}] |
| in://mnL6QHsd	| Ping to device which DDN is mnL6QHsd | Ping | [{IN:{From,To,State},Reply}] |
| in://local |  Trace to local motechat | trace | [{IN:{From,To,State},Reply}] |
| in://dc |	Trace to DC | trace | [{IN:{From,To,State},Reply}] |
| in://mnL6QHsd | Trace to device which DDN is mnL6QHsd | trace | [{IN:{From,To,State},Reply}] |
| in://local | Get my register data | whois | [{IN:{From,To,State},Reply}] |
   
**XS Function list**

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">func|<div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|:-------|     
| xs://config |	Get the contents of config of motebus xstoage | {catalog, idname} | get | {ErrCode,ErrMsg,result} |
| xs://config |	Set the contents of config of motebus xstoage | {catalog, idname, data} | set | {ErrCode,ErrMsg} |
| xs://cached |	Get the contents of cached of motebus xstoage | {catalog, idname} | get | {ErrCode,ErrMsg,result} |
| xs://cached |	Set the contents of cached of motebus xstoage | {catalog, idname, data} | set | {ErrCode,ErrMsg} |
| xs://cached |	Remove the contents of cached of motebus xstoage | {catalog, idname} | remove | {ErrCode,ErrMsg} |
| xs://cached |	Clear the contents of cached of motebus xstoage | {catalog} | clear | {ErrCode,ErrMsg} |
| xs://bucket |	Get the contents of bucket of motebus xstoage | {catalog, idname, datatype} | get | {ErrCode,ErrMsg,result} |
| xs://bucket |	Set the contents of bucket of motebus xstoage | {catalog, idname, data} | set | {ErrCode,ErrMsg} |
| xs://bucket |	List bucket of motebus xstoage | {catalog} | list | {ErrCode,ErrMsg,result} |
| xs://bucket | Remove bucket of motebus xstoage | {catalog, idname} | remove | {ErrCode,ErrMsg} |
| xs://secret | Get the contents of secret of motebus xstoage | {catalog, idname, password} | get | {ErrCode,ErrMsg,result} |
| xs://secret | Set the contents of secret of motebus xstoage | {catalog, idname, data, password} | set | {ErrCode,ErrMsg} |

### Logmms

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| log://save | Save log record to log DB | {"msg":"(msg)","tag":"(tag)","uid":"(uid)"} | {ErrCode,ErrMsg} |
| log://search | Search log records | {"srhtype":"(search type)","srhtext":"(search text)","srhtime":"(search time)","option":"(query option) ,"queryfield":"(query field)"} | {ErrCode,ErrMsg,result} |




### redixs

  | <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
  | redis://sadd   |             |         |
  | redis://sget   |             |         |
  | redis://delete |             |         |
  | redis://add    |             |         |
  | redis://get    |             |         |
  | redixs://add   |             |         |
  | redixs://get   |             |         |


### kanban

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| kanban://disp | Display msg on page://kanban?mqname=kanban_tag | { "tag":"(kanban tag)", "kanban":[{ "name":"(item name)", "data":{}}] } | {<br>"ErrCode": 0,<br>"ErrMsg": "OK"<br>}  |
| kanban://create  | Create kanban | { "tag":"(kanban tag)" } | {<br>"ErrCode": 0,<br>"ErrMsg": "OK"<br>}  |
| kanban://clear  | Clear kanban | { "tag":"(kanban tag)" } | {<br>"ErrCode": 0,<br>"ErrMsg": "OK"<br>}  |
| kanban://delete  | Delete kanban | { "tag":"(kanban tag)" } | {<br>"ErrCode": 0,<br>"ErrMsg": "OK"<br>}  |

### UC

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| uc://login |  Login  | { "UserName":"jujuetv@gmail.com", "Password":"02********" }    | {<br>"ErrCode": 0,<br>"ErrMsg": "OK",<br>"func": "ucLogin",<br>"UserInfo": {<br>"UToken": "g8VMouyj",<br>"Uid": "e4wUQWQc",<br>"UserName": "jujuetv@gmail.com",<br>"MobileNo": null,<br>"NickName": "jujue tv",<br>"FirstName": "jujue",<br>"LastName": "tv",<br>"Sex": null,<br>"EmailVerified": null,<br>"MobileVerified": null<br>},<br>"UseTime": 939<br>} |



### MUSTME

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| blog://mms |  Mustme get blog data  | { "tags": ["#photo"] }  |"Reply": [<br>{<br>"id": 4928,<br>"date": "2021-06-02T17:24:51",<br>"date_gmt": "2021-06-02T09:24:51",<br>"guid": {<br>"rendered": "https://blog.mustme.ypcloud.com/?p=4928"<br>},<br>"modified": "2021-06-02T17:24:51",<br>"modified_gmt": "2021-06-02T09:24:51",<br>"slug": "is-black-coffee-good-to-lose-weight",<br>"status": "publish",<br>"type": "post",<br>"link": "https://blog.mustme.ypcloud.com/4928/",<br>"title": {<br>"rendered": "Is black coffee good to lose weight"<br>},<br>"content": {<br>"rendered": ,<br>"protected": false<br>},<br>"excerpt": {<br>"rendered": "",<br>"protected": false<br>},<br>"author": 6,<br>"featured_media": 0,<br>"comment_status": "open",<br>"ping_status": "open",<br>"sticky": false,<br>"template": "",<br>"format": "standard",<br>"meta": [<br>],<br>"categories": [<br>13<br>],<br>"tags": [<br>],<br>"_links": {<br>"self": [...], // 1 items<br>"collection": [...], // 1 items<br>"about": [...], // 1 items<br>"author": [...], // 1 items<br>"replies": [...], // 1 items<br>"version-history": [...], // 1 items<br>"predecessor-version": [...], // 1 items<br>"wp:attachment": [...], // 1 items<br>"wp:term": [...], // 2 items<br>"curies": [...] // 1 items<br>}<br>}<br>]|


