# Jenkins Installation Guide

## Prerequisites

- **Java Development Kit (JDK)**: Jenkins requires Java to run. 

## Installation Steps

### 1. Install Java

First, update your package list:

```bash
sudo apt update
```

Then, install the OpenJDK 17 runtime environment:

```bash
sudo apt install openjdk-17-jre
```

Verify the Java installation:

```bash
java -version
```

### 2. Install Jenkins

Add the Jenkins repository key:

```bash
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null
```

Add the Jenkins repository:

```bash
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
```

Update your package list again:

```bash
sudo apt-get update
```

Install Jenkins:

```bash
sudo apt-get install jenkins
```

### **Note:** 

By default, Jenkins may not be accessible externally due to inbound traffic restrictions by AWS. Ensure that port 8080 is open in your inbound traffic rules to allow external access.
![image](https://github.com/user-attachments/assets/9b3939c6-7698-4fcb-af11-c98b6520031a)

when you allow these setting, you will see
![image](https://github.com/user-attachments/assets/185ba1d4-c437-4495-a5a1-5e44ccf49729)


---
### Happy learning :)

