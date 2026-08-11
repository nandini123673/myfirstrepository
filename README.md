##### **This Repository contains my hands on practice and notes for AWS, DEVOPS, GIT, GITHUB, LINUX.


AWS : Project: "Static Website Hosting" using Route53,s3,godaddy domain


myfirstrepository/**

Project Structure

 │──StaticWebsiteHosting/

             │── index.html
             
             │── style.css
             
             │── script.js
             
             │── screenshots/
             
 │── README.md**

myfirstrepository/**

 │── AWS/README.md**
 
 │── devops/README.md**

 │── gitcommands/README.md**

 └── linux/README.md**

 │── README.md**



# AWS Static Website Hosting Project

## Project Overview
This project demonstrates how to host a static website using Amazon S3 , route 53  and  godaddy domain  access it through a web browser.

## AWS Services Used
- Amazon S3
- Route 53 (Optional)
- GoDaddy Domain (Optional)

## Prerequisites
- AWS Account
- Static website files (index.html, CSS, JavaScript)
- Domain name (Optional)

## Steps Performed

### Step 1: Create an S3 Bucket
- Log in to the AWS Management Console.
- Open Amazon S3.
- Click **Create bucket**.
- Enter a unique bucket name.
- Select the AWS Region.
- Disable **Block all public access**.
- Create the bucket.

### Step 2: Upload Website Files
- Open the bucket.
- Click **Upload**.
- Upload:
  - index.html
  - style.css
  - script.js
- Click **Upload**.

### Step 3: Enable Static Website Hosting
- Open the bucket.
- Go to **Properties**.
- Select **Static website hosting**.
- Enable it.
- Set:
  - Index document: index.html
  - Error document: error.html (optional)
- Save the changes.

### Step 4: Configure Bucket Policy
Add a bucket policy to allow public read access to the website files.

### Step 5: Test the Website
- Copy the S3 Website Endpoint.
- Open it in a web browser.
- Verify that the website loads successfully.

select route53 and create hosted zone

copy nameservers and paste it in godady dns nameservers

select hostedzone in route53 create records


## Output
The static website is successfully hosted using Amazon S3 and is accessible through the website endpoint.







###### **📂AWS :**

* Compute Services (EC2, Lightsail)
* Storage Services (S3, EBS,)
* Networking (VPC, Internet Gateway, NAT Gateway, VPC Peering)
* Monitoring (CloudWatch)
* AWS Identity and Access Management (IAM)
* Notifications (SNS)
* Databases (RDS)
* Load Balancing \& Auto Scaling
* DNS (Route 53)
* Security and Logging (CloudTrail)
* Static Website Hosting





###### **📂DEVOPS: Jenkins, Ansible, Docker, Kubernetes**

* Jenkins : ubantu 24.04, java 21, jenkins
* Ansible : ubuntu 24.04  Master and Worker servers
* Docker  :  Amazon Linux , Docker, Docker hub
* Kubernates :
* 


###### **📂Git \& GitHub**

* Git Installation= git commands
* GitHub Account Creation= Repository creation



###### **📂Linux**

* Linux Commands:



###### **📂AWS :**

**EC2 :**

* LAB 1: Launching a sample website using virtual machine in windows.
* LAB 2: Finding a instance type according to client requirement.
* LAB 3: Vertical Scaling
* LAB 4: Termination Protection
* LAB 5: adding tags into the servers
* LAB 6: Snapshot and AMI creation data migration
* LAB 7: Hosting sample website using Linux
* LAB 8: Cloud watch and light sail
* LAB 9: Load balancer and auto scalling



**IAM**

* LAB 10: Identity access Management


**VPC** :

* LAB 11: Create vpc, subnet, Internet gate way and Routing table
* LAB 12: Configure EC2 machine with above created networks.
* LAB 13: VPC Peering Connection.
* LAB 14: Jump Server and NATGATEWAY in windows machine
* LAB 15: Jump Server and NATGATEWAY in Linux machine



**S3**

* LAB 16: creating buckets uploading same files in the bucket and sharing with others
* LAB 17: Creating multiple buckets giving access for particular bucket
* LAB 18: Versioning and Cross Regaion Replaction
* LAB 19: SNS and life cycle policy
* LAB 20: Dynamo DB and Amazon Transcribe
* LAB 21: AWS CLI and RDS
* LAB 22: Static Website Hosting



###### **📂DevOps**

**Jenkins :**

* LAB 1: Install Jenkins using ubuntu24.04
* LAB 2 : freestyle projects
* LAB 3 : Pipeline projects
* LAB 4 : Install Plugins

**Ansible:**

* LAB 1 : Passwordless connection between two servers
* LAB 2 : Install Ansible using ubuntu 24.04
* Lab 3 : Ansible Basic commands
* Lab 4 : Ansible Playbook

**Docker:**

* LAB 1 : Docker set up in Linucx machine
* LAB 2 : create docker hub
* LAB 3 : basic docker commands
* LAB 4 : Create Docker File
* LAB 5 : Dockerize java application
* LAB 6 : Dockerize springboot application
* LAB 7 : Dockerize python application
* LAB 8 : Docker Networks
* LAB 9 : Docker Volumes
* LAB 10: Docker compose and sp\[ringboot with mysql



**Kubernetes:**

Created with Pods, Deployments, Replica Sets, Services, Labels, Selectors, and YAML manifests.

Performed Rolling Updates and basic cluster management using kubectl.

Terraform (IaC).



###### **📂Git \& GitHub**

* Git Installation, GitHub account Creation, GitHub Repository
* Git Commands , Cloning,  Branching, Merging,  Pull Requests,  collaborators



###### 📂**Linux**

* Linux Commands
* File Permissions,
* Users \& Groups,
* Shell Commands,
* vi Editor,
* Command line arguments,
* Variables Loops,
* Control Statements,
* Operators,
* Functions ,
* Crontab





















## 👩‍💻 Author
*Nandini C*
