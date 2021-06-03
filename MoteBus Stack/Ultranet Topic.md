# Ultranet Topic 

## Mote
| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| mote://bash            |            |        |
| mote://xstorage        |            |        |
| mote://nearby          |            |        |
| mote://drop            |            |        | 
| mote://shot            |            |        |
| mote://measure         |            |        |
| mote://qsnap           |            |        |
| mote://apt             |            |        |
| mote://time            |            |        |
| mote://setUser         |            |        |
| mote://getUser         |            |        |
| mote://listPeripherals |            |        |
| mote://env             |            |        |
| mote://schedule        |            |        |
| mote://window          |            |        |
| mote://keybot          |            |        |
| mote://audio           |            |        |
| mote://shortcut        |            |        |
   

## Qbix
**mpodman**
   
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
  
**qman**
1. qbix

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

2. qman

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| qman://list   | list objects kind of qsite | {} |
| qman://run    | run a qbix | { "site_name": "any-qbix", "qbix_type": "any", "payload": { } } |
| qman://delete | delete specified qbix | { "site_name": "any-qbix", "qbix_type": "any", "payload": { } } |

3. qociman

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
| ss://touch | 
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
   
   
### object store
1. file://topic: function

| <div style="width: 150px">topic | <div style="width: 230px">description | <div style="width: 100px">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| file://addbucket    | Create bucket | { "bucket":"(bucket name)" }       |
| file://deletebucket | Delete bucket | { "bucket":"(bucket name)" } } |
| file://listbucket   | List bucket | {} |
| file://set          | Update bucket |         |
| file://get          | Get object | { "bucket":"(bucket name)", "object":"(object name)", "filetype":"url" } |
| file://delete       | Delete object | { "bucket":"(bucket name)", "object":"(object name)" }        |
| file://list         | List object | { "bucket":"(bucket name)", "object":"(object name)" }   |



2. obj://topic: function

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| obj://add    | Insert object | { "name":"(object name)", "data":{} } |
| obj://set   | Update object |{ "oid":"(object oid)", "name":"(object name)", "data":{} }|
| obj://delete | Delete object | { "oid":"(object oid)" } |
| obj://list   | List object | { "oid":"(object oid)" } |
| obj://get   | Get object | { "oid":"(object oid)" } |  


### comm

| <div style="width: 230pt">topic | <div style="width: 250pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
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


### sys

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| in://local  |             |         |
| xs://config |             |         |
| xs://bucket |             |         |
| xs://secret |             |         |
| xs://cached |             |         |



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
| kanban://disp | Display msg on page://kanban?mqname=kanban_tag | { "tag":"(kanban tag)", "kanban":[{ "name":"(item name)", "data":{}}] } | |
| kanban://create  | Create kanban | { "tag":"(kanban tag)" } | |
| kanban://clear  | Clear kanban | { "tag":"(kanban tag)" } | |
| kanban://delete  | Delete kanban | { "tag":"(kanban tag)" } | |  

### UC

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| uc://login |  Login  | { "UserName":"jujuetv@gmail.com", "Password":"02********" }    |  |



### MUSTME

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload | <div style="width: 100pt">result|
|:------------ |:-----------|:-------|:-------|   
| blog://mms |  Mustme get blog data  | { "tags": ["#photo"] }  |  |


