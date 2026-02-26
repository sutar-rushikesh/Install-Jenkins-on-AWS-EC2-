# 🚀 Jenkins Zero to Production

## 📌 What is Jenkins?

Jenkins is an open-source automation server used to build, test, and
deploy software in DevOps environments.

-   Java-based tool
-   Used in CI/CD pipelines
-   Supports 1800+ plugins
-   Strong community support
-   LTS (Long Term Support) version recommended for production

------------------------------------------------------------------------

# 🧠 Jenkins in DevOps (CI/CD Flow)

Developer → Git Push → Jenkins Trigger → Build → Test → Package → Deploy

Jenkins automates the entire CI/CD lifecycle.

------------------------------------------------------------------------

# ⚙️ Prerequisites

-   AWS EC2 (Ubuntu 22.04)
-   Port 8080 Open
-   Java (JDK 11 Recommended)

------------------------------------------------------------------------

# 🛠 Jenkins Installation on Ubuntu 22.04 (AWS EC2)

## Step 1 -- Launch EC2 Instance

-   Choose Ubuntu 22.04
-   Open Port 8080 in Security Group
-   Allow traffic (for lab/demo)

------------------------------------------------------------------------

## Step 2 -- Install Java

``` bash
sudo apt update
sudo apt install openjdk-11-jdk -y
java -version
```

------------------------------------------------------------------------

## Step 3 -- Install Jenkins (LTS)

Add Jenkins Key:

``` bash
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null
```

Add Repository:

``` bash
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
```

Install Jenkins:

``` bash
sudo apt update
sudo apt install jenkins -y
```

------------------------------------------------------------------------

## Step 4 -- Start Jenkins

``` bash
sudo systemctl start jenkins
sudo systemctl enable jenkins
sudo systemctl status jenkins
```

------------------------------------------------------------------------

# 🌐 Access Jenkins UI

http://`<EC2-Public-IP>`{=html}:8080

------------------------------------------------------------------------

# 🔐 Get Initial Admin Password

``` bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

Paste password in browser and complete setup.

------------------------------------------------------------------------

# 🏗 Jenkins Architecture

Developer → GitHub → Jenkins Master → Agents → Deployment

Master handles scheduling.\
Agents execute builds.

------------------------------------------------------------------------

# 🎯 Common Interview Questions

1.  What is Jenkins?
2.  What is CI/CD?
3.  What is Jenkins Pipeline?
4.  What is Jenkinsfile?
5.  Difference between Freestyle and Pipeline jobs?
6.  What is Master-Agent architecture?
7.  How to secure Jenkins?
8.  How to integrate Jenkins with Git?

------------------------------------------------------------------------

# 🚀 Best Practices

-   Use LTS version
-   Do not allow all traffic in production
-   Use HTTPS
-   Store credentials securely
-   Use build agents
-   Backup Jenkins configuration

------------------------------------------------------------------------

# 👨‍💻 Author

Rushikesh Sutar\
DevOps Engineer
