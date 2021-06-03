# Ultranet Topic 

## Mote
| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| mote://bash            | Control the device sudch like ssh | {"token":"xxx", "command":"ls"} |
| mote://xstorage        | Operate xstorage | {"method":"setConfig|getConfig|changeEiName|getBucket|setBucket|listBucket|removeBucket", "catalog":"CatalogName", "idname": "IDName", "data":"Content"} |
| mote://nearby          | Search near device | {} |
| mote://drop            | Drop file to other device | {"method":"ls|cp|rcp|cat|rm", "DDN":"xxxx", "path": "path", "files":"filename", "fsize":"123"} | 
| mote://shot            | Screen capture | {} |
| mote://measure         | Check system information | {"method":"info|status"} |
| mote://qsnap           | Computing deploy | {"type": "fbots|aibots", "operate":"list|run|restart|checkAlive|stop|start|delete|open|close", "svcName":"name", "startTime":"2021/06/04-12:0:0", "stopTime":"2021/06/04-16:0:0", "MCHAT_EINAME":"flowbot", "MCHAT_APPNAME":"flowbot-app", "MCHAT_UDID":"1", "MCHAT_DC":"dc", "MCHAT_IOC":"ioc", "MCHAT_WATCHLEVEL":"0", "FBOT_UI":"1", "FBOT_QCODE":"123", "FBOT_FLOWFILE":"", "FBOT_QNAME":"flowbot", "FBOT_MODE":"xstorage", "FBOT_PORT":"18888", "svcSource":"", "modelName":"", "modelSource":"", "parameter":""} |
| mote://apt             | Package management | {"operate":"list|remove|install","type":"snap|apt|npm","packageName":"wmctrl","keyword":"w*"} |
| mote://time            | Timezone setting | {"method":"now|listTimezone|setTimezone","zone":"Asia/Taiwan","keyword":"Asia"} |
| mote://setUser         | User information setting | {"EiTag":"#YP","EiLoc":"Taiwan"} |
| mote://getUser         | User information getting | {} |
| mote://listPeripherals | List peripherals | {"device":"usb|camera|ip|screen","update":true} |
| mote://env             | Process environment parameter | {"method":"read|create|append|update|delete","path":"fbot/test.env","content":["QQ=123","WW=123"]} |
| mote://schedule        | Make schedule | {"operate":"list|create|delete|start|stop","type":"once|routine|boot","hour":"2","minute":"1","month":"1","day":"1","week":"1","command":"ls","job":"qq","workspace":"0","terminal":"0"} |
| mote://window          | Operate window | {"operate":"list|assign|move|change","service":"0x123","key":"pointer","workspace":"0"} |
| mote://keybot          | Define keybot shortcut | {"device": "numPad","shortcuts": {"0": "Mic","1": "Workspace1","2": "Workspace2","3": "Workspace3","4": "Workspace4","5": "Super","6": "Workspace0","7": "Sceenshot","8": "Window","9": "Screencast","/": "Switch","*": "Mute","+": "Volume+","-": "Volume-"}} |
| mote://audio           | Operate audio | {"operate":"adjust|list|change","volume":"+5|50","device":"alsa_xxx","port":"linein","audio":"sink|source"} |
| mote://shortcut        | Manage GNOME shortcut | {"operate":"list|get|set|reset","func":"mic-mute","key":"KP_1"} |
   

## Qbix
##   mpodman
   
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
  
## qman
## 1. qbix

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

## 2. qman

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| qman://list   | list objects kind of qsite | {} |
| qman://run    | run a qbix | { "site_name": "any-qbix", "qbix_type": "any", "payload": { } } |
| qman://delete | delete specified qbix | { "site_name": "any-qbix", "qbix_type": "any", "payload": { } } |

## 3. qociman

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
| portal://log   | create the log record into odoo including 4 fields(name, time, fm, and mesaage) | { "model":"","voucher":"","vid": ,"cmd":"","act":"","data":{"name":"","message":""}}  |
| portal://event | create the event record into odoo |{"model":"","voucher":"","vid": ,"cmd":"","act":"","data":{...}} |
| portal://cost  | create the cost record  | { "model":"","voucher":"","vid": ,"cmd":"","act":"","data":{...}}  |
| portal://form  | create detail data list of device or equipment into odoo | { "model":"","voucher":"","vid": ,"cmd":"","act":"","data":{...}}  |
| query://model  | query data  | { "model":"","voucher":"","vid": ,"cmd":"","act":"","data":{"query_str":[...],"query_rst":[...]}}  |
   
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
   
   
## object store
## 1. file://topic: function

| <div style="width: 150px">topic | <div style="width: 230px">description | <div style="width: 100px">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| file://addbucket    | Create bucket | { "bucket":"(bucket name)" }       |
| file://deletebucket | Delete bucket | { "bucket":"(bucket name)" } } |
| file://listbucket   | List bucket | {} |
| file://set          | Update bucket |         |
| file://get          | Get object | { "bucket":"(bucket name)", "object":"(object name)", "filetype":"url" } |
| file://delete       | Delete object | { "bucket":"(bucket name)", "object":"(object name)" }        |
| file://list         | List object | { "bucket":"(bucket name)", "object":"(object name)" }   |



## 2. obj://topic: function

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| obj://add    | Insert object | { "name":"(object name)", "data":{} } |
| obj://set   | Update object |{ "oid":"(object oid)", "name":"(object name)", "data":{} }|
| obj://delete | Delete object | { "oid":"(object oid)" } |
| obj://list   | List object | { "oid":"(object oid)" } |
| obj://get   | Get object | { "oid":"(object oid)" } |  


## comm

| <div style="width: 230pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| mail://address     | Send msg by mail |{ "content":"(mail content)", "subject":"(mail subject)" } |   |
| sms://phone number | Send msg by sms | { "text":"(sms content)" } |   |
| tg://chat id      | Send msg by tg | { "content":"(telegram content)", "type":"(send method)", available type:["message", "photo", "audio", "document", "video", "animation", "voice", "sticker"], default is "message", "from":"(telegram bot name)", available bot:["pinponboybot", "jujuebot", "lovetubebot", "ypcloudbot", "ultravisorbot", "smartscreenbot"], default is "pinponboy", "cc": "(chat_id of cc)"(optional), "parse_mode":"MarkdownV2" (optional) } |   |
| ioc://chat id      | Send msg by tg with IOC format |{ "content":"(telegram content)", "from":"(telegram bot name)", "to":"(to_name)", "cc": "(chat_id of cc,options)" } |   |
| git://chat id     | Send msg to tg from git | { "content":"(telegram content)", "from":"(telegram bot name)", "to": "(to_name)", "cc": "(chat_id of cc,options)" }  |   |
| console://chat id | Send object msg | { "content":"(telegram content)", "from":"(telegram bot name)", "to":"(to_name)", "cc":"(chat_id of cc,options)" } |   |
| watch://chat id     | Send msg from watch | { "sub":"(watch sub)", "data":"(telegram content)" } |   |
| mpod://chat id     | Send msg from mpod | { "content":"(telegram content)", "from":"(telegram bot name)", "to":"(to_name)", "cc":"(chat_id of cc,options)" } |   |
| log://username   | Send msg to logmms | { "text":"content", "uid":"user id(optional)" } |   |
| view://username  | Send msg to page://view |{ "text":"content" } |   |


## sys

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| in://local  |             |         |
| xs://config |             |         |
| xs://bucket |             |         |
| xs://secret |             |         |
| xs://cached |             |         |



## redixs

  | <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
  | redis://sadd   |             |         |
  | redis://sget   |             |         |
  | redis://delete |             |         |
  | redis://add    |             |         |
  | redis://get    |             |         |
  | redixs://add   |             |         |
  | redixs://get   |             |         |


## kanban

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| kanban://disp | Display msg on page://kanban?mqname=kanban_tag | { "tag":"(kanban tag)", "kanban":[{ "name":"(item name)", "data":{}}] } | |
| kanban://create  | Create kanban | { "tag":"(kanban tag)" } | |
| kanban://clear  | Clear kanban | { "tag":"(kanban tag)" } | |
| kanban://delete  | Delete kanban | { "tag":"(kanban tag)" } | |  

## UC

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| uc://login |  Login  | { "UserName":"jujuetv@gmail.com", "Password":"02********" }    |  |



## MUSTME

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| blog://mms |  Mustme get blog data  | { "tags": ["#photo"] }  |  |


