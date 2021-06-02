## qman

===
The motechat mms for managing three kinds of software deployment(docker, helm, snap)

Table of contents
---

* [DDN](#DDN)
* Topic
  * [qman](#qman)
    - [qman://list](#qman://list)
    - [qman://run](#qman://run)
    - [qman://delete](#qman://delete)
### DDN
DDN: >h2/qman/qman-app 
## qman
Including qociman, mote and mpodman, you can use type to determine which software component to run
### qman://list
* Payload
```json
{
}
```
### qman://run
* Payload
```json
{
    "mma": "",
    "type": "",
    "app": {}
}
```
* qoci Example
```json
{
    /*
        uid: user id
        name: user name
        token: token
        site_name: location of site
        qbix_type: "qbix" "snap" "qoci" "mpod"
        app: "fbots" "ibuilder" "mlflow"
    */
    "uid": "",
    "name": "",
    "token": "",
    "site_name": "",
    "qbix_type": "",
    "app": ""
}
```
### qman://delete
* Payload
```json
{
    "qhost": "",
    "type": "",
    "payload": {}
}
```
