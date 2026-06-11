# Linux Hierarchy 
- / : The root directory is the top-level directory in Linux. Everything starts from here. I observed folders like bin, home, tmp.
     I would use this when i need to see overall linux structure.
- /home : Contains personal directories for normal users. I observed the user like ubuntu is here
  I would this when I need to access user files and documents.
- /root : Home directory for root user . I observed .bashec and .profile  directories.
- I would use when am working as root user and need administartor files
- /etc : it stores configuration files . I obeserved many config files are here like passwd , hostname .
  I would use this when I need to view and modify some configuration files
- /var/log : It stores applications and system log files. I observered kern.log , auth.log and syslog
  I would use this when I need to troubleshoots system and application issues.
- /tmp : it is store temporary files creted by users and applications.
   I wouls use this when i need to store temporary files like scripts
- /bin : Contains essential Linux commands required for system operation. I observed that git, cat, ls commands are here.
  I would like to use this when i need to know where basic commands are stored.
- /usr/bin : It containes most user-level executable commands. I observed that vim, grep here.
   I would like to use this when I need to commonly  used command line tools.
- /opt : Stores optional and third party applications.
  I would use this when i need to install and manage third party applications.
-  cat /etc/hostname : it showe a hostname . I obsered that it shows a ip adress.
  I would use this when iI need to identify which server I connected.
- du -sh /var/log/* 2>/dev/null | sort -h | tail -5  : it shows 5 largest files or directries inside /var/log.I observed that it shows largest 5 files with used disk space used by each file/directory in human redable format.
  I would use this when disk space is running low and i want to identify large  log files.
- ls -la ~  : Lists all files, including hidden files, in the current user's home directory. I observed that common files like .profile, .bashrc and directory .ssh .
 I would use this when  I need to view .user files and shell configuration files.
- ![linux hierarchy](screenshots/linux-hierarchy.png)
