# motebus/mpodman

---
Mpodman is a motechat application against kubernetes cluster by using [kubectl] and [helm].

---

## docker version of mpodman
### v1.0.0
kubectl version: v1.19.4

helm version: v3.4.1

k8s-helm3 version: 1.0.6

motechat version: 2.5.5

bluebird: 3.7.2

The Chart Repository:
* stable https://charts.helm.sh/stable 
* mpodman https://motebus.github.io/charts/ 
* gitlab https://charts.gitlab.io/ 
* jetstack https://charts.jetstack.io 
* bitnami https://charts.bitnami.com/bitnami 
* hashicorp https://helm.releases.hashicorp.com
### v1.0.1
added env MCHAT_IOC

### v1.0.2
added topic helm://run that its function as same as helm://create

### v1.1.0
added topic

> kubectl://getPod

> kubectl://getPodLog

> kubectl://listPod

> kubectl://createNamespace

> kubectl://deleteNamespace

> kubectl://getNamespace

> kubectl://listNamespace

### v1.1.1
fixed bug
createNamespace.js param -> params

### v1.1.2
change reply message
```
ErrMsg: "OK",
data: 

ErrMsg: ,
```

****
## Topic

* helm
    * [helm://list](#helm://list)
    * [helm://create](#helm://create)
    * [helm://delete](#helm://delete)
    * [helm://update](#helm://update)
    * [helm://get](#helm://get)
    * [helm://history](#helm://history)
    * [helm://rollback](#helm://rollback)
    * [helm://status](#helm://status)
* kubectl
    * [kubectl://deletePod](#kubectl://deletePod)
    * [kubectl://getPod](#kubectl://getPod)
    * [kubectl://getPodLog](#kubectl://getPodLog)
    * [kubectl://listPod](#kubectl://listPod)
    * [kubectl://createNamespace](#kubectl://createNamespace)
    * [kubectl://deleteNamespace](#kubectl://deleteNamespace)
    * [kubectl://getNamespace](#kubectl://getNamespace)
    * [kubectl://listNamespace](#kubectl://listNamespace)
****


## JSON Payload

### helm://list
* payload
```json
{
    "namespace": "default"
}
```

### helm://create
* payload
```json
{
    "releaseName": "fbuilder",
    "chartName": "mpodman/fbuilder",
    "namespace": "default",
    "values": {
        "nodeSelector": {},
        "replicaCount": "1",
        "podDnsPolicy": "None",
        "podDnsConfig": {
            "nameservers[0]": "8.8.8.8",
            "nameservers[1]": "8.8.4.4"
        },
        "MCHAT_EINAME": "fbuilder-example",
        "MCHAT_APPNAME": "fbuilder-example-app",
        "MCHAT_MBGWIP": "127.0.0.1",
        "MCHAT_MBGWPORT": "6888",
        "MCHAT_DC": "dc",
        "MCHAT_IOC": "ioc",
        "MCHAT_SENDTIMEOUT": "6",
        "MCHAT_WAITREPLY": "12",
        "MCAHT_WATCHLEVEL": "1",
        "USER_MODE": "single",
        "STORAGE_MODE": "cloud",
        "MBSTACK_UPSTREAM": "h3.ypcloud.com",
        "MBSTACK_BUSMODE": "0",
        "MBSTACK_WATCHLEVEL": "3",
        "MBSTACK_BUSNAME": "",
        "MBSTACK_DATAPATH": "/var/motebus",
        "MBSTACK_IPFINDER": "auto",
        "timezone": "Asia/Taipei",
        "fbuilder.image.repository": "motebus/fbuilder",
        "fbuilder.image.tag": "latest",
        "fbuilder.image.pullPolicy": "Always",
        "fbuilder.service.type": "ClusterIP",
        "fbuilder.service.protocol": "TCP",
        "fbuilder.service.nodePort": "",
        "fbuilder.service.port": "1880",
        "fbuilder.container.port": "1880",
        "fbuilder.container.extraEnvs": {},
        "fbuilder.ingress.enabled": "true",
        "fbuilder.ingress.annotation": {
            "nginx.ingress.kubernetes.io/rewrite-target": "/$1",
            "kubernetes.io/ingress.class": "nginx",
            "nginx.ingress.kubernetes.io/ssl-redirect": "false"
        },
        "fbuilder.ingress.tls[0].hosts[0]": "example.ypcloud.com",
        "fbuilder.ingress.tls[0].secretName": "fbuilder-example-tls",
        "fbuilder.ingress.hosts[0]": "example.ypcloud.com",
        "fbuilder.ingress.path": "/fbuilder/(.*)",
        "fbuilder.ingress.pathType": "Prefix",
        "motebus.image.repository": "motebus/motebus",
        "motebus.image.tag": "latest",
        "motebus.image.pullPolicy": "Always",
        "motebus.persistence.enabled": "false",
        "motebus.persistence.accessMode": "ReadWriteOnce",
        "motebus.persistence.storageClass": "nfs",
        "motebus.persistence.size": "1Gi"
    }
}
```

### helm://delete
* payload
```json
{
    "releaseName": "fbuilder",
    "namespace": "default"
}
```

### helm://update
* payload
```json
{
    "releaseName": "fbuilder",
    "namespace": "default",
    "sub_command": "all"
}
```

### helm://get
* payload
```json
{
    "releaseName": "fbuilder",
    "namespace": "default"
}
```

### helm://history
* payload
```json
{
    "releaseName": "fbuilder",
    "namespace": "default"
}
```

### helm://rollback
* payload
```json
{
    "releaseName": "fbuilder",
    "namespace": "default",
    "revision": "1"
}
```

### helm://status
* payload
```json
{
    "releaseName": "fbuilder",
    "namespace": "default"
}
```

### helm://update
* payload
```json
{
    "releaseName": "fbuilder",
    "chartName": "mpodman/fbuilder",
    "namespace": "default",
    "values": {
        "nodeSelector": {},
        "replicaCount": "1",
        "podDnsPolicy": "None",
        "podDnsConfig": {
            "nameservers[0]": "8.8.8.8",
            "nameservers[1]": "8.8.4.4"
        },
        "MCHAT_EINAME": "fbuilder-example",
        "MCHAT_APPNAME": "fbuilder-example-app",
        "MCHAT_MBGWIP": "127.0.0.1",
        "MCHAT_MBGWPORT": "6888",
        "MCHAT_DC": "dc",
        "MCHAT_IOC": "ioc",
        "MCHAT_SENDTIMEOUT": "6",
        "MCHAT_WAITREPLY": "12",
        "MCAHT_WATCHLEVEL": "1",
        "USER_MODE": "single",
        "STORAGE_MODE": "cloud",
        "MBSTACK_UPSTREAM": "h3.ypcloud.com",
        "MBSTACK_BUSMODE": "0",
        "MBSTACK_WATCHLEVEL": "3",
        "MBSTACK_BUSNAME": "",
        "MBSTACK_DATAPATH": "/var/motebus",
        "MBSTACK_IPFINDER": "auto",
        "timezone": "Asia/Taipei",
        "fbuilder.image.repository": "motebus/fbuilder",
        "fbuilder.image.tag": "latest",
        "fbuilder.image.pullPolicy": "Always",
        "fbuilder.service.type": "ClusterIP",
        "fbuilder.service.protocol": "TCP",
        "fbuilder.service.nodePort": "",
        "fbuilder.service.port": "1880",
        "fbuilder.container.port": "1880",
        "fbuilder.container.extraEnvs": {},
        "fbuilder.ingress.enabled": "true",
        "fbuilder.ingress.annotation": {
            "nginx.ingress.kubernetes.io/rewrite-target": "/$1",
            "kubernetes.io/ingress.class": "nginx",
            "nginx.ingress.kubernetes.io/ssl-redirect": "false"
        },
        "fbuilder.ingress.tls[0].hosts[0]": "example.ypcloud.com",
        "fbuilder.ingress.tls[0].secretName": "fbuilder-example-tls",
        "fbuilder.ingress.hosts[0]": "example.ypcloud.com",
        "fbuilder.ingress.path": "/fbuilder/(.*)",
        "fbuilder.ingress.pathType": "Prefix",
        "motebus.image.repository": "motebus/motebus",
        "motebus.image.tag": "latest",
        "motebus.image.pullPolicy": "Always",
        "motebus.persistence.enabled": "false",
        "motebus.persistence.accessMode": "ReadWriteOnce",
        "motebus.persistence.storageClass": "nfs",
        "motebus.persistence.size": "1Gi"
    }
}
```

### kubectl://deletePod
* payload
```json
{
    "pod_name": "mpod-810moj7dp6e-0",
    "namespace": "default"
}
```

### kubectl://getPod
* payload
```json
{
    "pod_name": "mpod-810moj7dp6e-0",
    "namespace": "default"
}
```

### kubectl://getPodLog
* payload
```json
{
    "pod_name": "mpod-810moj7dp6e-0",
    "namespace": "default",
    "container": ""
}
```

### kubectl://listPod
* payload
```json
{
    "namespace": "default"
}
```

###　kubectl://createNamespace
* payload
```json
{
    "namespace": "default"
}
```

### kubectl://deleteNamespace
* payload
```json
{
    "namespace": "default"
}
```

### kubectl://getNamespace
* payload
```json
{
    "namespace": "default"
}
```

### kubectl://listNamespace
* payload
```json
{
}
```


## Mappinng between helm values.yaml and object of values

values.yaml
```yaml
# pod node selector
nodeSelector: {}
# replication
replicaCount: 1
# pod toleration
tolerations: []
#pod DNS policy and config
podDnsPolicy: "None"
podDnsConfig:
  nameservers:
    - 8.8.8.8
    - 8.8.4.4
#motechat ei name
MCHAT_EINAME: fbuilder-example
#motechat appname
MCHAT_APPNAME: fbots-example-app
#motechat motebus gateway IP
MCHAT_MBGWIP: 127.0.0.1
#motechat motebus gateway port
MCHAT_MBGWPORT: 6888
#motechat dc
MCHAT_DC: dc
#motechat ioc
MCHAT_IOC: ioc
#motechat send timeout
MCHAT_SENDTIMEOUT: "6"
#motechat send reply timeout
MCHAT_WAITREPLY: "12"
#motechat log level
MCAHT_WATCHLEVEL: 1
#fbuilder user mode, "single, multi"
USER_MODE: single
#fbuilder mode, "local, xstorage, cloud"
STORAGE_MODE: cloud
# motebus upstream
MBSTACK_UPSTREAM: h3.ypcloud.com
# motebus bus mode
MBSTACK_BUSMODE: 0
# motebus watch level
MBSTACK_WATCHLEVEL: 3
# motebus bus name
MBSTACK_BUSNAME:
# motebus volume
MBSTACK_DATAPATH: /var/motebus
# motebus ip finder
MBSTACK_IPFINDER: "auto"
#timezone
timezone: Asia/Taipei

fbuilder:
  # image settings and pull policy
  image:
    repository: motebus/fbuilder
    tag: latest
    pullPolicy: Always
  # service settings
  service:
    type: ClusterIP
    protocol: TCP
    nodePort:
    port: 1880
  # container env settings
  container:
    # cannot change fbuilder port
    port: 18880
    #extra envs
    extraEnvs: {}
  # ingress host and path
  ingress:
    enabled: true
    annotations:
      nginx.ingress.kubernetes.io/rewrite-target: /$1
      kubernetes.io/ingress.class: "nginx"
      nginx.ingress.kubernetes.io/ssl-redirect: "false"
    tls:
      []
      # - hosts:
      #     - myapps.ypcloud.com
      #   secretName: flowbot-tls
    hosts:
      - myapps.ypcloud.com
    path: /fbuilder/(.*)
    pathType: Prefix

motebus:
  image:
    repository: motebus/motebus
    tag: latest
    pullPolicy: Always
  persistence:
    #Enable config persistence using PVC
    enabled: true
    # PVC Access Mode for config volume
    accessMode: ReadWriteOnce
    # PVC Storage Class for config volume
    storageClass: nfs
    # PVC Storage Request for config volume
    size: 1Gi
```

object of values
```js
"values": {
    "nodeSelector": {},
    "replicaCount": "1",
    "podDnsPolicy": "None",
    "podDnsConfig": {
        "nameservers[0]": "8.8.8.8",
        "nameservers[1]": "8.8.4.4"
    },
    "MCHAT_EINAME": "fbuilder-example",
    "MCHAT_APPNAME": "fbuilder-example-app",
    "MCHAT_MBGWIP": "127.0.0.1",
    "MCHAT_MBGWPORT": "6888",
    "MCHAT_DC": "dc",
    "MCHAT_IOC": "ioc",
    "MCHAT_SENDTIMEOUT": "6",
    "MCHAT_WAITREPLY": "12",
    "MCAHT_WATCHLEVEL": "1",
    "USER_MODE": "single",
    "STORAGE_MODE": "cloud",
    "MBSTACK_UPSTREAM": "h3.ypcloud.com",
    "MBSTACK_BUSMODE": "0",
    "MBSTACK_WATCHLEVEL": "3",
    "MBSTACK_BUSNAME": "",
    "MBSTACK_DATAPATH": "/var/motebus",
    "MBSTACK_IPFINDER": "auto",
    "timezone": "Asia/Taipei",
    "fbuilder.image.repository": "motebus/fbuilder",
    "fbuilder.image.tag": "latest",
    "fbuilder.image.pullPolicy": "Always",
    "fbuilder.service.type": "ClusterIP",
    "fbuilder.service.protocol": "TCP",
    "fbuilder.service.nodePort": "",
    "fbuilder.service.port": "1880",
    "fbuilder.container.port": "1880",
    "fbuilder.container.extraEnvs": {},
    "fbuilder.ingress.enabled": "true",
    "fbuilder.ingress.annotation": {
        "nginx.ingress.kubernetes.io/rewrite-target": "/$1",
        "kubernetes.io/ingress.class": "nginx",
        "nginx.ingress.kubernetes.io/ssl-redirect": "false"
    },
    "fbuilder.ingress.tls[0].hosts[0]": "example.ypcloud.com",
    "fbuilder.ingress.tls[0].secretName": "fbuilder-example-tls",
    "fbuilder.ingress.hosts[0]": "example.ypcloud.com",
    "fbuilder.ingress.path": "/fbuilder/(.*)",
    "fbuilder.ingress.pathType": "Prefix",
    "motebus.image.repository": "motebus/motebus",
    "motebus.image.tag": "latest",
    "motebus.image.pullPolicy": "Always",
    "motebus.persistence.enabled": "false",
    "motebus.persistence.accessMode": "ReadWriteOnce",
    "motebus.persistence.storageClass": "nfs",
    "motebus.persistence.size": "1Gi"
}
```

****


[helm]: https://helm.sh/docs/
[kubectl]: https://kubernetes.io/docs/tasks/tools/install-kubectl/ 
