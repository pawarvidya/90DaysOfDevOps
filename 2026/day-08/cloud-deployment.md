# Setup of Cloud Server, Docker, Nginx, Web deployment
# Objective : Deploy a cloud server, connect using SSH, install Nginx, verify web access, and collect logs.
# Part 1 : Launch  AWS EC2 instance.
- Step 1 : Create AWS EC2 instance
- Details for AWS EC2
  Cloud Provider : AWS
  OS: Ubuntu
  Instance Type: t3.micro
  Region : Oregon
- Created an Ubuntu EC2 instance and configured the security group.
  Allowed Ports in Security Group :
  SSH 22
  HTTP 80
  
  
