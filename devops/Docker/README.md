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




















