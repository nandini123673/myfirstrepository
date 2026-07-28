Jenkins: it is a open source CICD tool.







Step 1:







Launch instance in EC2 using ubantu 24.04 



custome tcp 8080 port.







copy public ip create virtual machine using mobaxterm.



open mobaxterm select session select ssh paste public ip give user name upload private key



terminal is open give user permission from ubantu to roo using sudo su command











Step 2:







\* sudo apt update :                               give the command it refresh the list of available software packages







\* sudo apt install fontconfig openjdk-21-jre :    install java







\* java --version :                                to display the installed java version











Install jenkin using below command







\* sudo wget -O /etc/apt/keyrings/jenkins-keyring.asc \\\\



\&#x20; https://pkg.jenkins.io/debian-stable/jenkins.io-2026.key



echo "deb \\\[signed-by=/etc/apt/keyrings/jenkins-keyring.asc]" \\\\



\&#x20; https://pkg.jenkins.io/debian-stable binary/ | sudo tee \\\\



\&#x20; /etc/apt/sources.list.d/jenkins.list > /dev/null



sudo apt update



sudo apt install Jenkins











You can enable the Jenkins service to start at boot with the command:







\* sudo systemctl enable Jenkins







You can start the Jenkins service to start command:







\* sudo systemctl start jenkins







You can check the status of the Jenkins service command:







\* sudo systemctl status jenkins







installed Jenkins installation completed.















Step 3:



copy public ip paste in google like httpp://public ip:8080



start Jenkins signin copy password and paste in Jenkins terminal using 







\* sudo cat password give enter



copy password and paste in Jenkins sign in page click Jenkins installed plugins option



give username password and email for sign in Jenkins start 











Step 4: 







freestyle projects:







\* Manually 







select new item 



click freestyle project give name give description



select execute shell option



execute one shell script using 



\\#!/bin/bash



echo "welcome to devops class"



click aplay and save 



click build now option



open console output to see success option  and displayed the output.







\* Build Triggers







Select new item



click freestyle project give name and description



select source code management 



click git option 



copy repository url and paste in Jenkins git url







select build triggers



select build after other projects are build



give previous job name



select trigger only if build is stable



aplay and save



click build now



job run see console output







\* Build Periodically:







Select new item 



give name select freestyle project 



give description



select source code management click git 



go to GitHub repository copy url paste in Jenkins git url







Select build periodically



give schedule has a every minute \\\* \\\* \\\* \\\* \\\*aplay and save 



without build now also it is run because we gave schedule 



output appears







\* poll scm







select new item



give name select freestyle project



give description



copy GitHub repository url and paste it in a Jenkins source management url







select poll scm option give schedule 



\* \\\* \\\* \\\* \\\*



aplay and save



the ccode is check first time only



second time the code is not run



after we commit any changes 



check first 



after it will not run











\* webhook







select new item



give project name 



select freestyle project give description



copy paste GitHub url into Jenkins git



select GitHub hook triggers pooling



aplay and save







go to GitHub



select settings



select webhooks



add webhook



give password and give payload url select Jenkins dashboard url 



paste jenkinsurl/github-webhook/



add webhook



go to repository select any file and edit commit changes



go to Jenkins



it is run 







whenever developers commit to a code in GitHub it is automatically run in Jenkins.



Pipeline Projects:



select new itm 

give name and select pipeline project 

give description

open pipeline script

write a simple script





pipeline {

&#x20;agent any 

&#x20; stages {

&#x20;    stage ('build') {

&#x20;       steps {

&#x20;              echo "build code"

&#x20;       }

&#x20;    }

&#x20;    stage ('test') {

&#x20;        steps {

&#x20;               echo "test code"

&#x20;        }

&#x20;    }

&#x20;    stage ('deploy')

&#x20;        steps {

&#x20;            echo "deploy code"

&#x20;        }

&#x20;    }

&#x20; }

}



aplay and save click build now output display











































