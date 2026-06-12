# Setup of Cloud Server, Docker, Nginx, Web deployment
- Objective : Deploy a cloud server, connect using SSH, install Nginx, verify web access, and collect logs.
- Part 1 : Launch  AWS EC2 instance.
- Step 1 : Create AWS EC2 instance
- Details for AWS EC2
  Cloud Provider : AWS,
  OS: Ubuntu,
  Instance Type: t3.micro,
  Region : Oregon
- Created an Ubuntu EC2 instance and configured the security group.
  Allowed Ports in Security Group :
  SSH 22,
  HTTP 80

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
  
  
