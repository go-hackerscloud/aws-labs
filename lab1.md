# EC2 Web Server Deployment Lab
Objective - Deploy a simple Apache or Nginx web server using EC2 and User Data.

##  Architecture
User → Internet → EC2 → Apache Web Server

###  Steps

1. Create EC2 key pair
2. Launch EC2 (Amazon Linux 2)
3. Add User Data:

#!/bin/bash
yum update -y
yum install httpd -y
systemctl start httpd
systemctl enable httpd
echo "Welcome to GoHackersCloud EC2 Lab" > /var/www/html/index.html


4. Allow HTTP traffic in security group
5. Access EC2 public IP

###  Validation

Browser shows the webpage.

### Cleanup

Terminate EC2 instance.
