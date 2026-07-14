AWS LEARNING REPOSITORY README.md



LAB 1: Launching a sample website using virtual machine in windows.

LAB 2: Finding a instance type according to client requirement.

LAB 3: Vertical Scaling 

LAB 4: Termination Protection 

LAB 5: adding tags into the servers


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

















































