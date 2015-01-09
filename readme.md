Ansible Rails Server Provision
===================
Things to do setup your server a little adduser deploy and 
edit The VISUDO file in better run as a root 
```shell
sudo adduser deploy
sudo adduser deploy sudo
visudo /etc/sudoers
visudo
```
then it will pop up change
```bash
from this -> %sudo   ALL=(ALL:ALL) ALL
to this -> %sudo   ALL=(ALL:ALL) NOPASSWD: ALL
```


First thing assume you are on Mac and install ansible through brew then the "hosts" file should be on 
``` bash
cd /usr/local/etc/ansible/hosts
```
```shell
[droplets]
128.199.1.1 <- Change it to your server ip
```
after the hosts finish setup
cd to the folder where you clone this project
and run this command on your shell
```shell
ansible-playbook playbook.yml
```
