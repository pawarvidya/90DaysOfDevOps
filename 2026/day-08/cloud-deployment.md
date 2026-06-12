# Setup of Cloud Server, Docker, Nginx, Web deployment
- Objective : Deploy a cloud server, connect using SSH, install Nginx, verify web access, and collect logs.
# Part 1 : Launch  AWS EC2 instance.
- Step 1 : Create AWS EC2 instance
- Details for AWS EC2
  - Cloud Provider : AWS
  - OS: Ubuntu
  - Instance Type: t3.micro
  - Region : Oregon
- Created an Ubuntu EC2 instance and configured the security group.
  Allowed Ports in Security Group :
  - SSH 22
  - HTTP 80

# Connect via SSH :
- Commands used :
  ssh -i key.pem ubuntu@public ip


# Part 2: Install Docker & Nginx
- Update Sysyem:
 - Command: sudo apt-get update
- Install Docker:
  - Commnad: sudo apt-get install docker.io -y
- Verify:
  - Command: docker --version
- Install nginx:
  - Commnad: sudo apt-get nginx -y
- Verify:
  - Command: systemctl status nginx
- Check Version :
  - Command:  nginx -v
#  Part 3: Verify web access
- Opened Browser
  - http://<public-ip>
  Nginx welcome page displayed successfully.

# Part 4 : Extract Nginx log
- View logs:
  - sudo tail -n 20 /var/log/nginx/access.log
- Save Logs to File:
  - sudo cp /var/log/nginx/access.log ~/nginx-logs.txt
- Verify:
  - cat ~/nginx-logs.txt
-  Download Log File: 
  - scp -i my-key.pem ubuntu@<public-ip>:~/nginx-logs.txt
# Challenges Faced:
- Issue 1: Nginx page not accessible
  - Reason:
    - Port 80 was not allowed in Security Group.
  - Solution:
    - Added HTTP (80) inbound rule and refreshed browser.
-  Issue 2: Permission denied while accessing logs
  - Reason:
    - Nginx logs require sudo access.
  - Solution:
    - sudo tail /var/log/nginx/access.log
# What I Learned:
- How to launch an EC2 instance.
- How to connect to a remote server using SSH.
- How to install and manage Nginx.
- How Security Groups control access to cloud servers.
- How to view and save application logs.

  
  
  
  
