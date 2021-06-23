# Keybot (short cut)
###        desktop-wm_panel-main-menu, press 5
###        desktop-wm_switch-to-workspace-1, press 1
###        desktop-wm_switch-to-workspace-2, press 2
###        desktop-wm_switch-to-workspace-3, press 3
###       desktop-wm_switch-to-workspace-4, press 4
###        desktop-wm_switch-to-workspace-last, press 6
###        setting-daemon_screenshot, press 7
###        setting-daemon_window-screenshot, press 8
###        setting-daemon_screencast, press 9
###        desktop-wm_switch-applications, press /
###        setting-daemon_mic-mute, press 0
###        setting-daemon_volume-down, press -
###        setting-daemon_volume-up,  press +
###        setting-daemon_volume-mute, press *

# Chrome Remote Desktop (CRD)
## Benefits: To let others use your desktop without ssh
## How to install
### 1. update & wget
```
    sudo apt update
```
```
    sudo apt-get install --assume-yes wget
```
### 2. wget crd
```
    wget https://dl.google.com/linux/direct/chrome-remote-desktop_current_amd64.deb
```
### 3. install package & dependencies
```
sudo dpkg --install chrome-remote-desktop_current_amd64.deb
```
```
sudo apt install --assume-yes --fix-broken
```
## How to use it 
When you want to use someone's CRD
<br>url: https://remotedesktop.google.com/headless and forward the token to the computer's terminal
<br>Tips: CRD doesn't allow same user account to approach UI at the same time so you have to make sure the remote user account is logged out or else you will only see black screen
