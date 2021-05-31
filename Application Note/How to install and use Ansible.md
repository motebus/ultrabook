# How to install and use Ansible

## step 1. Installation on Ubuntu 20.04
open terminal enter 
``sudo apt update``
<br> ``sudo apt install software-properties-common``
sudo apt-add-repository --yes --update ppa:ansible/ansible
sudo apt install ansible``
confim if ansible is correctly installed 
open terminal and enter
``ansible --version``

## step 2
### terminal enter 
### sudo nano /etc/ansible/hosts to get into ansible inventory list

## step 3
### build your own group [xxx] (ex:[meow])
### [meow] (this will become green pattern)
### xxx.xxx.xxx.xxx(your remote network ip) ansible_port=22(you may have you own port)  ansible_user=xxx(your remote username) ansible_passwd=xxxx(your remote user password)

## step 4
### when finish setup inventory ctrl+X to exit also  please commit to save file when exitting
