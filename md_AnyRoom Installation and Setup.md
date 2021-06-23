# Follow all the steps with terminal(cmd)
# Stage1 play remote by chrome
## 1. Update apt
```
    sudo apt-get update
```
```
    sudo apt-get upgrade
```

## 2.Install flowbot from snap
flowbot
```
    sudo snap install flowbot
```
## 3. Install wmctrl from apt
wmctrl
```
    sudo apt install  wmctrl
```
# Stage 2 moted sphere
## 1.
### sphere
``` 
    sudo snap install sphere 
```
### moted
``` 
    cd Downloads 
```
``` 
    wget https://github.com/motebus/moted-snap/releases/download/v1.5.0/moted_amd64.snap ```
```
``` 
    sudo snap install moted_amd64.snap --dangerous --classic```
```
``` 
    cd 
```
### keybot
```
    cd Downloads 
```
```
    wget https://github.com/motebus/keybot-snap/releases/download/v0.0.5/keybot_amd64.snap ```
```
```
    sudo snap install keybot_amd64.snap --dangerous --classic```
```
```
    cd 
```
# Stage 3 program manager
## 1.After installing spehre &moted reopen the terminal you should see your udid on your hostsname 
if not then
```
    sudo snap restart sphere
```
```
    sudo snap restart moted
```
and reopen the terminal again 
## 2.Use pmbot to install rest of the thing including apps(curl,logmms etc) keyboard shortcut
# Tour guide