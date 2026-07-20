Service VPC (Virtual Private Cloud): It is a networking service in aws,



to create our own private network in aws where we can launch instances like ec2 instances securely.





Components of a VPC



CIDR Block – Defines the IP address range (e.g., 10.0.0.0/16).



Subnets – Divide the VPC into smaller networks (Public and Private).



Internet Gateway (IGW) – Gives internet access to public subnets.



Route Table – Decides where network traffic goes.



Security Group – Acts as a firewall for EC2 instances.



Network ACL (NACL) – Firewall at the subnet level.



NAT Gateway – Allows instances in private subnets to access the internet without being directly accessible from the internet.



Example

Suppose you create a VPC with CIDR 10.0.0.0/16.



Public Subnet: 10.0.1.0/24 → Launch a web server with internet access.



Private Subnet: 10.0.2.0/24 → Launch a database with no direct internet access.





LAB 1: Create vpc, subnet, Internet gate way and Routing table



LAB 2: Configure EC2 machine with above created networks.



LAB 3: VPC Peering Connection.



LAB 4: Jump Server and NATGATEWAY in windows machine



LAB 5: Jump Server and NATGATEWAY in Linux machine







**LAB 1: Create vpc, subnet, Internet gate way and Routing table**



Step 1:



login AWS Console

search VPC

Select regaion

Click create VPC

create IPV4CIDR block :10.0.0.0/16

click create vpc



Step 2:



Create subnets using same vpc inside the vpc

Public Subnet : CIDR : 10.0.1.0/24

private Subnet : CIDR : 10.0.2.0/24





Step 3 :



Create an internet Gateway and attach it to the vpc



Step 4 :



Create a public route table inside route

edit destination 0.0.0.0/0 through internet gateway

edit subnet association select and save



Create a private route table inside route we cant access destination

edit subnet association select and save



**LAB 2: Configure EC2 machine with above created networks.**



Step 1:



Create vpc

create two subnets public subnet private subnet

create internet gateway

create route table





Step 2:



select EC2 create two servers public server and private server



instance name public server

select AMI amazon Linux

instance type t2.micro

create key pair

edit network settings

select vpc

select subnet1 or public subnet

auto assign enable public ip

create security group

launch instance





Step 3 :



instance name private server

select AMI amazon Linux

instance type t2.micro

create key pair

edit network settings

select vpc

select subnet2 or private subnet

auto assign disable public ip

create security group

launch instance



Step 5:



select public server connect using ssh

copy server 2 private ip

ping server2 private ip in server 1 machine





**LAB 3: Peering Connection :connect one regaion to another regaion**





Step 1:



Create vpc

create two subnets public subnet private subnet

create internet gateway attach to vpc

create route table two routs public route and private route

connect public route to internet gate way edit subnet association

edit subnet association in private





Step 2:



select EC2 create two servers public server and private server



instance name public server

select AMI amazon Linux

instance type t2.micro

create key pair

edit network settings

select vpc

select subnet1 or public subnet

auto assign enable public ip

create security group

launch instance





Step 3 :



instance name private server

select AMI amazon Linux

instance type t2.micro

create key pair

edit network settings

select vpc

select subnet2 or private subnet

auto assign disable public ip

create security group

launch instance





Step 4:



create vpc

select another regaion

CIDR 172.16.0.0/16

CREATE VPC



Step 5 :



create subnet

vpc id

give name has subnet 3

CIDR 172.16.1.0/24

create subnet



Step 6:



create internet gateway

attach to selected vpc





Step 7:



Create Route Table

edit routes

CIDR 0.0.0.0/0

internet gateway

create routes



edit subnet association

click and save



Step 8:



launch instance name has server 3

selected vpc

select subnet 3

public ip enable

add security group

launch instance



Step 9 : Peering connection one regaion server to another regaion server



select peering connection option

select sender  or requester vpc id

select accepter vpc id

create vpc connection



Steap 10:



select server 1 instance  and connect using SSH

select another Regaion server private IP copy private IP

paste  in sever 1 Linux machine using "ping private key"





LAB 4 :Jump Server and Nat gateway in Windows:



Step 1:

create VPC

select Regaion create VPC

CIDR 10.0.0.0/16

create VPC



Step 2 :

create subnet

public subnet

selected VPC CIDR 10.0.1.0/24

create subnet





create subnet

private subnet

selected VPC CIDR 10.0.2.0/24

Create subnet





Step 3 :



create internet gateway

attach to VPC

create



Step 4:





Create route table

public route table selected VPC

edit routs 0.0.0.0/0

edit subnet association click and save



create route table

private route table selected VPC

edit subnet association click and save





Step 5:

Launch instance and create vm  using EC2



give server name has public server

select windows operating system

create key pair and select instant type

edit network settings

selected vpc

select  Public subnet

public ip enable

create security group

launch instance



give server name has Private server

select windows operating system

create key pair and select instant type

edit network settings

selected VPC

select Private subnet

public IP disable

create security group

launch instance



select public server and connect using RDP

select download remote desktop file and get password using password create virtual machine in windows

host sample website using public ip in public server using server manager

copy public IP and paste in google

the public IP is work



select private server and connect

the public IP is disable

the virtual machine has no internet it is not connected



private ec2 has no internet because no public IP

we cant connect directly



connect to the public windows ec2 using RDP

from that public windows server open remote desktop connection (mstsc)

enter the private IP of the private windows ec2

enter the username and password

we are now connection in private server.





Using Nat gate way we get internet in private server



LAB 5: jump Server and Natgateway in LINUX:



Step 1:

create VPC

select Regaion create VPC

CIDR 10.0.0.0/16

create VPC



Step 2 :

create subnet

public subnet

selected VPC CIDR 10.0.1.0/24

create subnet





create subnet

private subnet

selected VPC CIDR 10.0.2.0/24

Create subnet





Step 3 :



create internet gateway

attach to VPC

create



Step 4:





Create route table

public route table selected VPC

edit routs 0.0.0.0/0

edit subnet association click and save



create route table

private route table selected VPC

edit subnet association click and save







Step 5:

Launch instance 



give server name has public server

select amazon Linux operating system

create key pair and select instant type

edit network settings

selected VPC

select  Public subnet

public ip enable

create security group

launch instance



give server name has Private server

select Amazon Linux operating system

create key pair and select instant type

edit network settings

selected VPC

select Private subnet

public IP disable

create security group

launch instance



connect public ec2 instance through SSH

the connection is successful.





in public ec2 instance connection we give private ip 

copy private ipv4 address 

give command chmod 700 privatevm.pem







open nat gate way

create name using public

allocate 

create nat gate way





route table open private route table 

edit routs 0.0.0.0/0

connected through nat gatway

now we get internet in private server













































































































































































&#x20;

