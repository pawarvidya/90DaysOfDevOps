# **Linux Architecture**
 Linux is operating system and it"s open source. Linux architecture has different component of a system to interact with each other to manage resources and running applications and provide a stable environments. The main compenents of Linux are :
 - Application
 - Shell
 - Kernel
 - Hardware
 - Utilities
   
   ![Image]( https://github.com/pawarvidya/90DaysOfDevOps/blob/3db1ae5757d4291e1f2597bfbb6441a0095fab14/2026/day-02/Linux%20architecture%20diagram.webp)

- Kernel- It is heart of linux. It controls how processors are executed and scheduled and responsible for memory management and process management.
- Shell - It acts as interface. It takes a  command as input from user and interprets them and transmits to kernel. And kernel provides required output. There are many types of shell like Bourne Shell(sh), C Shell (csh), Bourne Again Shell (bash), Korn Shell (ksh), Z Shell (zsh).
- Hardware -  It includes physical devices such as CPU, Mwmory and Storage devices . It supports memory acess and CPU control and I/O operations.
- System Utility - System utilities are command-line tools that help users and administrators manage, configure, and monitor the Linux system.
- User Space - User space where user application can run. e.g chrome browser, Docker, jenkins.
- init/ systemd- init is first process started by kernel during booting. In modern Linux distributions, systemd is used instead of traditional init systems.and 
  Process of Id (PID) is 1. systemd starts and manages all background services in Linux. e.g nginx, docker.

  # What systemd Does and Why It Matters-
  systemd is the service manager in modern Linux systems. And it is responsible for
- Booting the system
- Starting services
- Restarting failed services
- Managing background processes

# Linux Process States-
-Running - Process is working now. e.g Browser or Java app running.
-Sleeping - Process is waiting for something. e.g Waiting for file or network response
-Ready - Process is ready to run. 
-Stopped - Process is paused temporarily.
- Zombie - Process work is finished but system still shows its entry.
- Terminated - Process is fully closed and removed.

  # Commands -
  - ps -ef : Shows all running processes.
  - top : Shows CPU and memory usage live
  - kill PID : Stops a process.
  - systemctl : it manages services.
  - grep : Searches specific process or text.

  
  



