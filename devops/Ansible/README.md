ANSIBLE : Ansible is a server configuration management tool.

in that we use yaml Language.it is a yet another markup language.

two instances one is Master and another one is Worker

AMI using Ubuntu 24.04

connect instance public ip using Mobaxterm.

password less connection between two servers



LAB 1 :



Passwordless connection between two servers 

Install Ansible on ubuntu 24.04 



Step 1



Create two instances one is Master and another one is Worker

connect two instances using public ip in Mobaxterm through SSH

Rename one is Master and Another one is Worker



* Sudo apt update In Master  
* Sudo apt update in Worker

&#x20;  

&#x20;  We have to make passwordless connection between two servers

Master

* ssh-keygen -t ed25519
* enter
* enter
* enter
* cat ~/.ssh/id_ed25519.pub
* copy password





Worker

* mkdir -p ~/.ssh
* nano ~/.ssh/authorized_keys
* paste password in editor save using control+o enter exit control+x
* chmod 700 ~/.ssh
* chmod 600b ~/.ssh/authorized_keys 





Master

* ssh Ubuntu@worker private key
* nano hosts
* worker
* exit
* Master

test : ansible all  -I ubuntu -m ping

successfully created password less connection







Install Ansible



* ansible --version
* sudo apt update
* sudo apt install ansible -y
* ansible --version

Create inventory file 

* sudo mkdir -p /etc/ansible
* sudo nano /etc/ansible/hosts

open editor in that type

[workers]

worker private ip ansible-user=ubuntu

control+0 for save then enter

control+x for exit



* cat /etc/ansible/hosts
* check ansible all -I /etc/ansible/hosts -m ping



or


check if Ansible is Working 

* ansible all -m ping 
* ansible all -m ping -u ubuntu





To create a folder in ansible is

* sudo mkdir -p /etc/ansible

to create files inside the folder

* sudo touch /etc/ansible/test.txt

verify the file

* ls -l /etc/ansible

edit a file using

* sudo nano /etc/ansible/test.txt

type content control+o to save enter control+x for exit



display the content

* cat /etc/ansible/test.txt

output : added  content display.



* **Linux command create a file on the current server working dairectly on ubuntu master server**

**sudo touch /etc/ansible/test.txt**



* **ansible all -a "touch ansible\_file" creates file on other servers**

























