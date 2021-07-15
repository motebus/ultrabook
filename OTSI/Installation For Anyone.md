# Follow all the steps with terminal(cmd)
## If you are using anypi just burn your SD card nothing else to do
## For AnyRoom & Anypro after os is installed
# Stage 1 update
## 1. Update apt
```
    sudo apt-get update
```
```
    sudo apt-get upgrade
```
## 2. Install wmctrl from apt
wmctrl
```
    sudo apt install  wmctrl
```
# Stage 2 Install snap
## 1.
### sphere
``` 
    sudo snap install sphere 
```
### fbots 
```
    sudo snap install fbots
```
### gwin
```
    sudo snap install gwin
```
### moted
``` 
    cd Downloads 
```
``` 
    wget https://github.com/motebus/moted-snap/releases/download/v1.5.1/moted_amd64.snap
```
``` 
    sudo snap install moted_amd64.snap --dangerous --classic
```
``` 
    cd 
```
### keybot
```
    cd Downloads 
```
```
    wget https://github.com/motebus/keybot-snap/releases/download/v0.0.5/keybot_amd64.snap 
```
```
    sudo snap install keybot_amd64.snap --dangerous --classic
```
```
    cd 
```
### After installing spehre & moted reopen the terminal you should see your udid on your hostsname (ex:jujue@anypro-xxxxxx)
# Please reboot your pc
# Stage 3 
## Run main-app
### After your mouse clicks at "Home" in filesystem press "ctrl+h" to see files with "dots" like ".config"
### If you don't have dirctory autostart/execfile please use the following commands in terminal
```
cd /home/jujue/.config
```
```
mkdir execfile
```
```
mkdir autostart
```
```
cd
```
### Copy "scripts" main.sh under /.config/execfile/ & main.desktop under /.config/autostart/
