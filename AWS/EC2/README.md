AWS LEARNING REPOSITORY README.md



LAB 1: Launching a sample website using virtual machine in windows.

LAB 2: Finding a instance type according to client requirement.

LAB 3: Vertical Scaling

LAB 4: Termination Protection

LAB 5: adding tags into the servers

LAB 6: Snapshot and AMI creation data migration

LAB 7: Hosting sample website using Linux

LAB 8: Identity access Management

LAB 9: Cloud watch and light sail\\

LAB 10: Load balancer and auto scalling





Service :EC2



LAB 1: Launching a sample website using virtual machine in windows.

Step 1:

log in to aws console
select regaion click launch instance
give server name select amazon Linux or windows operating system
select instance type create key pair
select security group
click launch instance



Step 2:

select the instance
click connect
download the RDP file
decrypt the administrator password using key pair
copy password paste in notepad
connect using remote desktop
give password then connect
virtual machine is created



Step 3:

search server manager in virtual machine
open server manager
click add roles and features
select installation
choose the web server
click add features
click next until installation



Step 4:

open this pc c drive and select inetpub option
select wwroot
delete two default files
create a file named index.html
save the file has index.html and give all files

Step 5:

go to instance
select or copy public ipv4 address
paste it in google
now we got website



LAB 2: Finding a instance type according to client requirement.

Step 1:

login to aws console
select ec2 instance
select regaion
click launch instance
give name to the server
select operating system
select instant type in that select compare instant type like according to client requirement vcpu=8 and memory = 32 gb instance family and storage
review the configuration, search aws pricing calculator in that we same server name, same regaion and client requirement we got information
launch the ec2 instance



LAB 3: Vertical Scaling : increasing or decreasing the resources of a single server increase cpu increase ram or storage thi is scale up reduce is called scale down

current ec2 instance t2.micro 1vcpu and 1gb ram
scale up to t3.large 2vcpus 8gb ram

Step 1:

login to aws console using EC2 create instance
select regaion click launch instance
give server name select amazon Linux
select instant type create key pair
select security group
launch instance
select the ec2 instance to scale up
click instant state then stop the instance first
click actions go to instance settings, select a new instant type
to change instant type ex now t2.micro i changed t3.micro
click applay
start the instance verify is running with the new instance type



LAB 4: Termination Protection

Step 1:
log in to aws console
select regaion click launch instance
give server name select amazon Linux or windows operating system
select instance type create key pair
select security group
click launch instance

Step 2:

select running instance
stop the instance using instance state option
select actions select instance settings click change termination protection
choose enable option
click and save.

verification:

select ec2 instance
click instance state terminate the instance
aws display an error message
disable termination protection realy want to terminate the instance

LAB 5: adding tags into the servers: the instance can be easily identified using assigned tags

Step 1:
sign in to the aws console
select regaion launch instance
click instance
select the ec2 instance
go to the tags,
click manage tags
click add new tag
enter the key and value.
click and save.
the tags are sucsesfully assigned

Lab 6:Snapshot and AMI creation Data migration

Step 1:

login to aws console

create two instances using different regaions

select one instance and create virtual machine

create folders on virtual machine

select snapshot option create snapshot

select snapshot and click actions select copy snapshot

copied for destination server



Step 2:



select copied snapshot and click actions select create image from snapshot option

give image name select create image option

image  created in AMI



Step 3:



open AMI select AMI then click launch instance from AMI

give AMI image name

create keypair

allow security group rules

launch instance

select instance connect through RDP use previous password  create a virtual machine

vm is created



LAB 7: Hosting sample website using Linux





Step 1:

Lanch instance

select amazon Linux server

select instance type

create key pair

select 3 security groups

click launch instance



Step 2:



connect instance using mobaxterm

select instance

copy public ip and uswr name

go to mobaxterm select sessions select  SSH paste public IP in remote host

give user name

select advanced ssh settings in that we upload private key of the instance

click ok

instance is connected in mobaxterm.





Step 3:



give the command cd Downloads

ssh ec2-user@publicip -i keypairname.pem

ex : ssh ec2-user@13.229.199.216 -i serverkey.pem

sudo dnf update -y

sudo dnf install httpd -y

sudo systemctl start httpd

sudo systemctl enable httpd

sudo sysytemctl ststus httpd

cd var/www/html

sudo vi index.html

enter cintent in vi editor then save it

go to instance copy public ip then search in google

website is appear



LAB 8: Identity access Management



Step 1:

loged in to aws management server

opened the IAM server

created an IAM user

assigned console access

attached the required permissions

created the IAM user

loged in using the iam user credentials

enable mfa for additional security

if try to log in everytime mfa will ask code

created iam users, groups and roles and copy permissions



LAB 9: Cloud watch and light sail

Step 1:

create ec2 instance using linux operating system
open cloudwatch create alarams
click create alaram
click select metric select ec2  per instance metric cpu utillization



Step 2:

click config notification in that alaram state in alaram
create new topic topic name enail
if we waqnt the alaram stop reboot or terminate the instance we can add an ec2 action to the alaram



open emain inboxfind the email from aws sns
click confirm subscription



give alaram name click next
connect our ec2 instance and run
while true; do echo; done this command increases the cpu utillazation



the ec2 instance continuees running because you only configured a notification not an ec2 action.







light sail :



search lightsail create instance

connect using ssh use the commands

sudo dnf update -y

sudo dnf install httpd -y

sudo systemctl start httpd

sudo systemctl enable httpd

sudo vi /var/www/html/index.html

copy paste ipv4 address in google.see the output.





LAB 10 : Load balancer and autoscaling lab: 



Step 1: 



log in to aws console

launch instance in ec2 server using windows os

connect ec2 instance

connect ec2 instance using RDP client

download remote desktop file,upload private key and get password create virtual machine

search server manager and install create one text document inside inetpub wwroot give the name has index.html

select instance click action select image and template option create image

AMI is created.

select snapshot option snapshot also created

select autoscaling group click auto scaling group before we create  click launch template option 

created launch template

select autoscaling group and create auto scaling group using group name instance type keypair availability zone,

select attach to a new load balancer,then select application load balancerselect internet facing 

select new target grop

click health check desired maximum and minimum 

copy public ip and paste in google



































































