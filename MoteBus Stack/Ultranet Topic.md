# Ultranet Topic 

## object store
1. file://topic: function

| <div style="width: 150px">topic | <div style="width: 230px">description | <div style="width: 100px">payload |
|:------------------- |:-----------|:-------:|
| file://addbucket    |             |         |
| file://deletebucket |             |         |
| file://listbucket   |             |         |
| file://set          |             |         |
| file://get          |             |         |
| file://delete       |             |         |
| file://list         |             |         |



2. obj://topic: function

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload |
|:------------ |:-----------|:-------|
| obj://add    |             |         |
| obj://set   |             |         |
| obj://delete |             |         |
| obj://list   |             |         |
   


## mpodman

   | <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload |
   |:---------------- |:----------- |:------- |
   | helm://list      | list releases (= mpod_name)|         |
   | helm://create    | create a new chart_name with the given mpod_name. There are **5** kinds of chart_name  written in "mpodman/xxxx". (xxxx can be **fbuilder, sscreen, ioc, fbots** or **webmms-srv**) |         |
   | helm://delete    |  uninstall a release |         |
   | helm://update    | update a new chart_name with the given mpod_name. There are **5** kinds of chart_name  written in "mpodman/xxxx". (xxxx can be **fbuilder, sscreen, ioc, fbots** or **webmms-srv**) |         |
   | helm://get       | download extended information of a named release  |         |
   | helm://history   | fetch release history |         |
   | helm://rollback  | roll back a release to a previous revision |         |
   | helm://status    | display the status of the named release  |         |
   | kubectl://delete | Delete resources by filenames, stdin, resources and names, or by resources and label selector |         |


## comm

  | <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload |
  |:---------------------- |:----------- |:------- |
  | mail:// *address*      |             |         |
  | sms :// *phone number* |             |         |
  | tg:// *chat id*        |             |         |
  | ioc:// *chat id*       |             |         |
  | git:// *chat id*       |             |         |
  | console:// *chat id*   |             |         |
  | watch:// *chat id*     |             |         |
  | mpod:// *chat id*      |             |         |
  | line:// *line id*      |             |         |
  | fb:// *fb id*          |             |         |
  | sip://                 |             |         |
  | mqtt://*mqtt topic*    |             |         |
  | echo                   |             |         |


## sys

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload |
|:----------- |:----------- | ------- |
| in://local  |             |         |
| xs://config |             |         |
| xs://bucket |             |         |
| xs://secret |             |         |
| xs://cached |             |         |



## redixs

  | <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload |
  |:-------------- | ----------- | ------- |
  | redis://sadd   |             |         |
  | redis://sget   |             |         |
  | redis://delete |             |         |
  | redis://add    |             |         |
  | redis://get    |             |         |
  | redixs://add   |             |         |
  | redixs://get   |             |         |




## moted

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload |
|:------------------- |:----------- |:------- |
| mote://nearby       |             |{"qq":"12 3"}|
| mote://shot         |             |{"t1":24,"t2":48}|
| mote://bash         |             |{"command":"scrot"}     |
| mote://xs_setconfig |             |{"method": "setConfig","catalog": "test","idname": "fisher22","data": {"123": "33"}}|
| mote://xs_getConfig |             |{"method": "getConfig","catalog": "test","idname": "fisher22"}|
| mote://xs_changeEIName|           |{"method": "changeEIName","catalog": "test-app","data": "test02"}|
| mote://xs_getBucket |             |{"method": "getBucket","catalog": "schedule","idname": "flowbot","datatype": "binary","__note*type": "//'hex', 'ascii', 'utf8', 'base64', or 'binary'"}|       
| mote://measure      |             |"method":"info"      |
| mote://time         |             |"method":"now"     |
| mote://fbotSchedule |             |"operate": "start","svcName": "test01"|
| mote://drop         |             |"method": "ls","DDN": ">>xxxx-mote","path": "|
| mote://setUser      |             |"EiTag": "#fisher","EiLoc": "Taipei"    |


## kanban

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload |
|:--------------------- | ----------- | ------- |
| kanban://*kanban tag* |             |         |


## UC

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload |
|:---------- | ----------- | ------- |
| uc://login |             |         |



## MUSTME

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload |
|:---------- | ----------- |:-------|
| blog://mms |             |         |



---

## TWCC
### twapi-data
   | <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload |
   |:-------------------- |:----------:|:------- |
   | twcc://packageList   |            |         |
   | twcc://packageSearch |            |         |
   | twcc://packageShow   |            |         |
   | twcc://resourceShow  |            |         |
   | twcc://groupList     |            |         |
   | twcc://groupShow     |            |         |
   | twcc://tagList       |            |         |
   | twcc://tagShow       |            |         |


## twapi-oci

   | topic | description | payload |
   |:------------------------- | ---------- | ------- |
   | twcc://getToken           |            |         |
   | twcc://getUser            |            |         |
   | twcc://getProject         |            |         |
   | twcc://listSolution       |            |         |
   | twcc://getSolution        |            |         |
   | twcc://getContainer       |            |         |
   | twcc://listContainer      |            |         |
   | twcc://deleteContainer    |            |         |
   | twcc://createContainer    |            |         |
   | twcc://showContainer      |            |         |
   | twcc://associateContainer |            |         |


## twapi-man

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload |
|:------------------ | ----------- | ------- |
| twcc://createImage |             |         |
| twcc://deleteImage |             |         |
| twcc://getLog      |             |         |
| twcc://getUserLog  |             |         |
| twcc://getToken    |             |         |


## qman
1. qhost

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload |
|:------------------ | ----------- | ------- |
| qhost://list |             |         |
| qhost://save |             |         |
| qhost://update |             |         |
| qhost://delete |             |         |

2. qman

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload |
|:------------------ | ----------- | ------- |
| qman://list |             |         |
| qman://run |             |         |
| qman://delete |             |         |

3. mpodman

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload |
|:------------------ | ----------- | ------- |
| mpodman://list |             |         |
| mpodman://run |             |         |
| mpodman://delete |             |         |
| mpodman://update |             |         |

4. qociman

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload |
|:------------------ | ----------- | ------- |
| qociman://run |             |         |
| qociman://delete |             |         |
| qociman://get |             |         |
| qociman://list |             |         |
| qociman://restart |              |          |   
| qociman://start |              |      |   
| qociman://stop |              |      |   
| qociman://status |              |      |   

5. mote

| <div style="width: 150pt">topic | <div style="width: 230pt">description | <div style="width: 100pt">payload |
|:------------------ | ----------- | ------- |
| mote://run |             |         |
| mote://delete |             |         |
| mote://start |             |         |
| mote://stop |             |         |
| mote://restart |              |          |   
| mote://list |              |      |   
| mote://checkAlive |              |      |   
