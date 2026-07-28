Docker :







Docker is a contanarization tool,



using docker we can run our application code in any machine without thinking about dependencies.







Docker :Docker is a contanarization tool.



using docker we can run our applications in any machine without thinking about dependencies.















LAB 1: Install Docker using Ec2 amazon Linux



LAB 2: create docker hub



LAB 3: Docker Commands







LAB 1: Install Docker using Ec2 amazon Linux







Step 1 :







login to aws management console



click Launch instance



select amazon Linux server



create key pair select instance type



launch instance







Step 2:



connect instance using  copy public ip in to remote host in mobaxterm



Open Linux terminal in mobaxterm



install docker software in Linux using below commands















\* \*\*sudo yum update -y\*\*

\* \*\*sudo yum install docker -y\*\*

\* \*\*sudo service docker start\*\*

\* \*\*sudo usermod -ag docker ec2-user\*\*

\* \*\*exit\*\*

\* \*\*press r to return\*\*











\*\*check docker -v\*\*











\*\*Create Docker HUB\*\*







\* serch in google hub.docker.com

\* using email name and password to sign up



docker hub is created







Docker Commands:







\* Check Docker Version



docker --version







\* list all downloaded images



docker images







\* download image from docker hub



docker pull







\* create and start a container



docker run imagename







\* show running containers



docker ps







\* show all containers running and stopped



docker ps -a







\* Stop a running container



docker stop containerid







\* start a stopped container



docker start containerid











\* restart a container



docker restart containerid







\* remove a stopped container



docker rm container id







\* remove an image



docker rmi imageid







\* view container logs



docker logs containerid







\* rename a container



docker rename old new













