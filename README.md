# 🌐 Website Hosting on AWS EC2 (Linux Server)

![AWS](https://img.shields.io/badge/AWS-EC2-orange?logo=amazon-aws)
![Linux](https://img.shields.io/badge/OS-Linux-lightgrey?logo=linux)
![Web Server](https://img.shields.io/badge/Web%20Server-Apache%2FNginx-blue)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## 📋 Project Overview

This project demonstrates how to host a static website using an **AWS EC2 instance running a Linux-based OS** such as Ubuntu. It includes steps for installing a web server (Apache or Nginx), uploading website files, and configuring public access via a browser.

---

## 🧰 Tech Stack

- **Cloud Platform**: AWS EC2  
- **Operating System**: Ubuntu Server (or other Linux distros)  
- **Web Server**: Apache or Nginx  
- **Website Stack**: HTML, CSS, JavaScript  
- **Security**: SSH (22), HTTP (80), HTTPS (443 optional)

---

## 🚀 Setup Instructions

### Step 1: Launch an EC2 Instance

- Log in to the [AWS EC2 Console](https://console.aws.amazon.com/ec2).
- Launch a new instance:
  - Choose **Ubuntu Server 20.04 LTS** (or preferred Linux AMI)
  - Instance Type: `t2.micro` (Free Tier)
  - Create/use an **SSH key pair (.pem)**  
  - Configure **Security Group**:
    - Port 22 (SSH)
    - Port 80 (HTTP)
    - Port 443 (HTTPS - optional)

---

### Step 2: Connect to Instance via SSH

```bash
chmod 400 your-key.pem
ssh -i "your-key.pem" ubuntu@your-ec2-public-ip
```

### Step 3: commands for enable httpd  

1.	Switch to root user  # sudo –i
2.	Install httpd  # yum install httpd -y
3.  Download zip file of project  # curl –O url of zip file
4.	Unzip file   # unzip filename
5.	Move folder to /var/www/html/ directory    
    ```  #  mv foldername/*   /var/www/html/  ```
7.	Start http service
  ```
    # systemctl start httpd
    # systemctl enable httpd 
```

### Step 4: View Your Website
Open your EC2 instance’s public IPv4 address in a browser: http://<your-ec2-ip> 


🧠 Learning Outcomes
+ Launch and connect to EC2 instances
+ Deploy static content using the Linux CLI
+ Configure firewall and public access for cloud-hosted apps

📈 Future Enhancements
+ SSL configuration using Let's Encrypt
+ Custom domain setup via Route 53
+ Use of CloudFront CDN for performance
+ Automate deployment using CI/CD pipelines

📄 License
This project is licensed under the MIT License.

🙌 Acknowledgements
Thanks to AWS documentation, open-source communities, and Linux server guides.

```
