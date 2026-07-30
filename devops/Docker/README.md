Docker :







Docker is a contanarization tool,



using docker we can run our application code in any machine without thinking about dependencies.







Docker :Docker is a contanarization tool.



using docker we can run our applications in any machine without thinking about dependencies.















LAB 1: Install Docker using Ec2 amazon Linux



LAB 2: create docker hub



LAB 3: Docker Commands



LAB 4: Create Docker File



LAB 5: dockarize java web application



LAB 6: dockerize springboot application


LAB 7: dockerize python application


LAB 8: Docker Volumes



LAB 9: Docker Networks



LAB 10: Docker Compose and Springboot With my Sql









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







LAB 4: Create Docker File



=> Dockerfile contains set of instructions to build docker image



=> To write Dockerfile we will use below keywords



1\) FROM

2\) MAINTAINER

3\) RUN

4\) CMD

5\) COPY

6\) ADD

7\) WORKDIR

8\) EXPOSE

9\) ENTRYPOINT

10\) USER

11\) ARG

12\) VOLUME



Step 1 : Launch Instance using instance type t3.micro and key pair and os has amazon Linux allow tcp port 8080 and CIDR 0.0.0.0/0

&#x20;connect Instance public ip in Mobaxterm ssh create virtual machine.



Step 2: Install Docker ina terminal



Step 3: vi Dockerfile Create Dockerfile using vi editor

vi Dockerfile

FROM OpenJDK:17-jdk-slim

MAINTAINER /app

EXPOSE 8080

COPY target/\*.jar app.jar

CMD echo "this is devops"

ENTRYPOINT \["java", "-jar" , "app.jar"]



esc :wq enter



cat Dockerfile added content is visible



docker build -t imagename(backendapp) .

docker images

docker run backendapp

docker ps

docker ps -a

docker images

docker login

enter username of the docker hub

enter password for the docker hub

docker tag imagename dockerhub username/repositoryname:latest

docker push dockerhubusername/repositoryname:latest



The repository is visible in docker hub 







LAB 5: How to Dockerize Java Web Application ?



Step 1 : Launch Instance using instance type t3.micro and key pair and os has amazon Linux allow tcp port 8080 and CIDR 0.0.0.0/0

&#x20;connect Instance public ip in Mobaxterm ssh create virtual machine.



Step 2: :: Install git client software



$ sudo yum install git -y



\## Step-2:: Clone git repo



$ git clone 



Step-3 :: Go inside project directory



$ cd maven-web-app



\## Step-4 :: Install Maven software



$ sudo yum install maven -y



Step-5 :: Build Project using maven goals



$ mvn clean package



Step-4 :: Create Dockerfile



$ vi Dockerfile



&#x09;FROM tomcat:8.0.20-jre8

&#x09;MAINTAINER nandini <nandinic@gmail.com>

&#x09;EXPOSE 8080

&#x09;COPY target/maven-web-app.war /usr/local/tomcat/webapps/maven-web-app.war



Step-5 : Build Docker Image



$ docker build -t <image-name> .



Step-6 : Check Docker Image created



$ docker images



Step-7 :: Run Docker Image



$ docker run -p 8080:8080 -d <image-name>



Step-8 :: Check Docker Container



$ docker ps



Step-9 :: Enable 8080 port in EC2 VM security group inbound rules





Step-10 :: Access Application in browser



URL : http://public-ip:8080/maven-web-app/





LAB 6: How to Dockerize Spring Boot Application ?



&#x20;Spring Boot is java based framework



Step 1 : 

&#x20;Launch Instance using instance type t3.micro and key pair and os has amazon Linux allow tcp port 8080 and CIDR 0.0.0.0/0

&#x20;connect Instance public ip in Mobaxterm ssh create virtual machine.

&#x20;

Step 2 :



Install Docker



Install git



Clone git repo

$ git clone 



get into project directory

$ cd spring-boot-docker-app



Build project using maven

$ mvn clean package



check target directory content

$ ls -l target



Build docker image using below command0,m 

$ docker build -t imagename



Check docker images created

$ docker images



Run docker image

$ docker run -p 8080:8080 -d sb-app



Note: Enable 8080 port in EC2 VM security Groups inbound run



&#x09;URL : http://public-ip:8080/



\# Check docker container logs



$ docker logs <container-id>



LAB 6 :Python with Docker

Step 1: Launch Instance connect mabaxterm 

Step 2: Install Docker on Linux terminal

Step 3: install git

$ git clone 

$ cd folder

$ docker build -t imagename.

$ docker run -p 5000:5000 -d imagename


=> Access Application like below

	URL : http://public-ip:5000/



LAB 7:Docker Volumes 

stateless container: data will be deleted after container deleted


Step 1:
log in to AWS console
create instance launch instance using amazon Linux
connect instance using public ip into mobaxterm terminal

Step 2:
update and install docker
check docker is installed or not

create image name 
docker pull nginx

check image 
docker images

run image in container
docker run --name c1 -d nginx

check container is running
docker ps 

duplicate container c1 name change

go to host give sudo su

go to container create files
touch file{1..10}.txt
ls -l
display files


go to host 

find / -name file1.txt the files are stored in host machine particular location 
cd copy paste /var to dif/
ls -l displayed all files


docker ps 
docker rm -f c1
container is deleted
check data ls data also deleted
check in host machine and check in container data deleted



Statefull Container : using docker volume we can create statefull container there are three types 

anonymous volume:    docker run -it --name c2 -v /test nginx/bin/bash
named volume:        docker run -it  --name c3 -v my-volume:/test1 nginx/bin/bash
bind mounts :        docker run -it --name c4 -v /home/ec2-user/nandini:/dir2 nginx /bin/bash


1 Ananymous volume:


cd ~ go inside the home directory
give sudo su

Step 1 : docker volume ls

docker run -it iiname c2 -v /test nginx/bin/bash
container created 
duplicate
create host machine
go to host 
give docker ps 

go inside container
ls
cd test/


host docker volume ls
docker inspectcopypaste volume id
copy mountpoint location and paste in notepad
cd paste
ls
touch nandini{}.txt
ls-l


go to container
ls -l
touch container2files{}.txt
ls-l created filkes
 
go to host check ls -l
appear files
docker ps
docker run -f c2
docker ps container deleted 
ls
data is display 
if container is deleted data is safe using anonymous container


2 Named volume: if container is deleted data is available 



3 Bound mounts directly link directories between host and container

give command 

docker run -it --name c4 -v /home/ec2-user/nandini:/dir2 nginx /bin/bash
container is created container 4 machine
duplicate
host machine host 
go to container
ls
cd dir2/
ls
touch nandini{1..10}.php
ls -l
files are created 

check in host the files are created both 
ls -l
docker ps container display
docker rm -f c4
container is deleted

ls data is available...



LAB 8 : Docker Networks:


connect ec2 instance using mobaxterm

install docker 

check docker installed or not docker -v (by default networks are created) to check docker network ls

docker inspect bridge       to check containers

go to docker hub select one container 

paste docker pull paste

docker images

go to docker hub select one container 

paste docker pull paste

docker images

docker run -p 8080:8080 -d copyimageid
docker run -p 8081:8080 -d imagenamepaste 

same port is work in containers but different host port

docker ps 

docker inspect bridge
copy paste containers ip address into notepad


docker ps

docker exec -it containerid /bin/bash

ping second container ip address

we get responce 

exit


docker ps 

docker exec -it containerid /bin/bash

ping first container ip address

without ping we can install ping using apt update && apt install iputils-ping -y
 ping containerip address

we get responce.




LAB 10: Docker Compose and Spring boot With my Sql

log in to aws console

launch instance using amazon Linux connect instance using instance public ip connect mobAXTERM.

Install docker 

install git

install maven
 
another way to install commands
vi nandini.sh
copy all the insalls in one file
sh nandini.sh


git -v
mvn -v
docker -v

docker-compose -v it is a tool we want to install

copy paste docker compose install

exit


git clone 

cd inside the folder

mvn clean package

docker build spring-boot-mysql-app .

docker images

ls
docker-compose up -d
cat docker-compose.yml
docker network ls
docker ps


edit inbound role 8080 custom tcp

public ip copy:8080



docker ps
copy 
docker exec -it paste /bin/bash
MySQL -u root -proot
show databases;
use sbms;
show tables;
select * from book;

go to browser output
add 

terminal
select * from book;


exit

exit

pwd

docker ps

docker-compose down

docker ps

docker ps -a

ls

cd ..
rm -rf *

ls




easiest way:

vi nandini.sh

#! bin/bash

git clone

cd

docker build

do -compose up -a

sh nandini.sh









 















