AWS LEARNING REPOSITORY README.md



&#x20;LAB 1: Launching a sample website using virtual machine in windows.

&#x20;LAB 2: Finding a instance type according to client requirement.

&#x20;LAB 3: Vertical Scaling 

&#x20;LAB 4: Termination Protection 

&#x20;LAB 5: adding tags into the servers

&#x20;

Service :EC2



LAB 1: Launching a sample website using virtual machine in windows.

&#x20; 



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



step5
go to instance
select or copy public ipv4 address
paste it in google
now we got website



LAB 2: Finding a instance type according to client requirement.



Step 1: 

&#x20;login to aws console

&#x20;select ec2 instance 

&#x20;select regaion 

&#x20;click launch instance

&#x20;give name to the server

&#x20;select operating system

&#x20;select instant type in that select compare instant type like according to client requirement vcpu=8 and memory = 32 gb instance family and storage

&#x20;review the configuration, search aws pricing calculator in that we same server name, same regaion and client requirement we got information

&#x20;launch the ec2 instance

&#x20;



LAB 3: Vertical Scaling : increasing or decreasing the resources of a single server increase cpu increase ram or storage thi is scale up reduce is called scale down

&#x20;  current ec2 instance t2.micro 1vcpu and 1gb ram

&#x20;  scale up to t3.large 2vcpus 8gb ram

&#x20;  

&#x20;Step 1:

&#x20;  login to aws console using EC2 create instance 

&#x20;  select regaion click launch instance 

&#x20;  give server name select amazon Linux

&#x20;  select instant type create key pair

&#x20;  select security group

&#x20;  launch instance

&#x20;  select the ec2 instance to scale up

&#x20;  click instant state then stop the instance first

&#x20;  click actions go to instance settings, select a new instant type

&#x20;  to change instant type ex now t2.micro i changed t3.micro

&#x20;  click applay 

&#x20;  start the instance verify is running with the new instance type



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





&#x20;



&#x20;

















































