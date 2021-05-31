# How to install and use Ansible

## Step 1. Installation on Ubuntu 20.04
<br> Open terminal enter 
> sudo apt update
<br> ``sudo apt install software-properties-common``
<br> ``sudo apt-add-repository --yes --update ppa:ansible/ansible``
<br> ``sudo apt install ansible``
<br> Confim if ansible is correctly installed 
<br> Open terminal and enter
<br> ``ansible --version``

## Step 2.
<br> Open terminal enter 
<br> ``sudo nano /etc/ansible/hosts`` to get into ansible inventory list

## step 3.
<br> Build your own group [xxx] (ex:[meow])
<br> [meow] (this will become green pattern)
<br> xxx.xxx.xxx.xxx(your remote network IP) 
<br> ansible_port=22(you may have you own port)  
<br> ansible_user=xxx(your remote username) 
<br> ansible_passwd=xxxx(your remote user password)

## step 4.
<br> When finish setup inventory, press ctrl+X to exit. Also, please commit to save file when exitting.
