In THis DEMOAPP Summer collection 2024 application deployes through Jenkins 
Intro
**Continuous Integration and Continuous Deployment (CI/CD) streamline application delivery. In this blog, we’ll discuss how to deploy a Java-based application to an Apache Tomcat server using a CI/CD pipeline. We'll use Jenkins for automation, Maven for build management, and Git for version control.
**

Understanding the Tools
Git: Stores your application code and tracks changes.

Maven: Builds and manages Java projects by handling dependencies.

Jenkins: Automates the CI/CD process by integrating code building, testing, and deployment.

Tomcat: A popular server for hosting Java-based applications.

===============================================================
Real-Time Scenario
Imagine a software team working on an e-commerce web application. Every time a developer updates the product catalog, they push the changes to GitHub. Jenkins automatically:

Pulls the updated code.

Builds the application using Maven.

Perform the unit test using Maven.

Deploys the new version to Tomcat.

This process minimizes manual effort and ensures the application is always up-to-date.

===================================================================

Steps to Deploy a Java-Based Application Using CI/CD
STEP-1: Launch 2 EC2 Instances (Kernel 5.10)

Jenkins Server

Tomcat Server

<img width="1849" height="344" alt="image" src="https://github.com/user-attachments/assets/b650d1e4-693f-4082-8c84-b09142ae22e1" />


STEP-2: Connect Jenkins server and Install Jenkins & GIT

#STEP-1: INSTALLING GIT
```
yum install git -y
```

#STEP-2: GETTING THE REPO (jenkins.io --> download -- > redhat)
```
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
```

#STEP-3: DOWNLOAD JAVA17 AND JENKINS
```
yum install java-17-amazon-corretto -y
yum install jenkins -y

#STEP-4: RESTARTING JENKINS (when we download service it will on stopped state)
systemctl start jenkins.service
systemctl status jenkins.service
```

Now copy the public-ip of your system and access it with 8080 port.

<img width="1455" height="696" alt="image" src="https://github.com/user-attachments/assets/70844d22-763d-43fe-a36c-4f01887fadb5" />



