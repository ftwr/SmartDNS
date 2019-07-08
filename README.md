# .::Smart DNS deployment::.

Tested on Ubuntu 16:04 (digitalocean), but must work on other debian based distros.

Install Ansible on your development host:
```shell
apt-get update -y
apt-get install ansible -y
```
Also don’t forget to add your production host ip in inventory file:

Generate SSH Key on dev and copy to the remote production server in ~/.ssh/authorized_keys

Running a playbook from dev host:

Unarchive and put “smartDNS” role in /etc/ansible/roles

```shell
Run: ansible-playbook playbook.yml --extra-vars “remote_ip=prod_ip_here”
```
To add new zones edit: /etc/bind/zones.override
