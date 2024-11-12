# Jenkins Setup Linux

## What is Jenkins ?
<ul>
  <li>Jenkins is an open-source automation server widely used in DevOps for continuous integration and continuous delivery (CI/CD). It helps streamline and automate the software development process.</li>
  <li>It allows developers to build, test, and deploy code automatically by integrating with various version control tools like Git.</li>
  <li>Jenkins is highly extensible with a vast library of plugins that support different stages of the development lifecycle, including testing, deployment, and monitoring.</li>
  <li>It provides a web-based dashboard to set up and manage jobs, pipelines, and track the status of builds in real time.</li>
</ul>

## Jenkins Architecture Diagram 

![1-Z6Sf32SN8sPktNuvOv0YYw](https://github.com/user-attachments/assets/a7bb2d1c-b8ee-46c4-8fd1-5c76786692e9)

## Jenkins Components 

<ul>
  <li>Jenkins Server (Master)</li>
  <li>Jenkins Agent (Slave)</li>
  <li>Jobs (Projects)</li>
  <li>Build Triggers</li>
  <li>Build Executors</li>
  <li>Plugins</li>
  <li>Pipeline</li>
  <li>Console Output</li>
  <li> Artifacts and Archive</li>
</ul>

### We will update the system repository index by using the following command.

    sudo apt update
    sudo apt upgrade -y

## Step #1 : Install Java 

### Jenkins requires Java, usually OpenJDK 11 or newer

    sudo apt install openjdk-11-jdk -y

## Step #2 : Add Jenkins Repository and Key
### Add the Jenkins repository key

    curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null

### Add the Jenkins repository

    echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

### Update your package lists again

    sudo apt update

## Step #2 : Install Jenkins

    sudo apt install jenkins -y


