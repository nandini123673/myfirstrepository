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







LAB 1: Create vpc, subnet, Internet gate way and Routing table



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



























































