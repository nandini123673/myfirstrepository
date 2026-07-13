Launching a simple website using virtual machine

&#x20;Step1 : 

&#x20;     login to the aws management console

open the ec2 service 

select regaion

click launch instance

give name server name

select window server

choose t3.micro 

create or select key pair

create a security group RDP HTTP HTTPS 

Launch the instance







Step 2:

&#x20;   

&#x20;   select the instance

click connect

download the RDP file 

decrypt the administrator password using key pair

copy password paste in notepad

connect using remote desktop

give password then connect 

virtual machine is created 





Step3

&#x20;    

&#x20;    search service manager in virtual machine 

open server manager 

click add roles and features 

select installation

choose the web server

click add features

click next until installation 







Step 4:



&#x20;open this pc c drive and select inetpub option 

then select wwroot

then delete two default files

create a file named index.html

save the file has index.html and give all files



step5



go to instance 

select or copy public ipv4 address

paste it in google

now we got website

















































