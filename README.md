# DecodeLabs Internship — Server Commander 🚀

## Project Description

This project is part of the DecodeLabs Cloud Computing Industrial Training Program.

The goal of this project is to provision and configure a Linux virtual server on AWS using Amazon EC2, connect to it securely using SSH, install Nginx as a web server, and host a custom webpage accessible through the Internet.

## Technologies Used

- AWS EC2
- Ubuntu Linux
- Nginx
- SSH
- HTML
- AWS Security Groups

## Infrastructure

The project uses an AWS EC2 instance running Ubuntu Linux.

### Security Group Rules

| Protocol | Port | Source |
|----------|------|--------|
| SSH | 22 | My IP |
| HTTP | 80 | 0.0.0.0/0 |

## How to Run

### 1. Launch an EC2 Instance

Create an AWS EC2 instance using Ubuntu Linux with a public IPv4 address.

### 2. Connect Using SSH

Use the private key created during the EC2 setup:

```bash
chmod 400 "DecodeLabs-Key.pem"
ssh -i "DecodeLabs-Key.pem" ubuntu@ec2-98-84-183-16.compute-1.amazonaws.com

### 3. Update Packages
 """ bash
 sudo apt update

### 4.Install Nginx
""" bash 
sudo apt install nginx -y

 ## 5. Verify Nginx
 sudo systemctl status nginx

The expected status is: Active: active (running)
## 6. Configure the Webpage

Edit the Nginx default webpage: 
""" bash : sudo vim /var/www/html/index.html
The custom webpage displays: Welcome to DecodeLabs 🚀
Server successfully deployed on AWS EC2.
Powered by Ubuntu & Nginx.
## 7. Test the Web Server : curl localhost
## 8. Access the Website

Open the EC2 Public IPv4 address in a web browser:http://YOUR_PUBLIC_IP
The custom DecodeLabs webpage should be displayed.

# Project Results
✅ EC2 Linux server deployed
✅ SSH access configured
✅ Nginx installed and running
✅ Security Group configured
✅ Custom HTML webpage created
✅ Website successfully accessed through the Internet
