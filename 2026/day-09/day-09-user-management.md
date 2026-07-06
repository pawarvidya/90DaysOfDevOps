## Users & Groups Created
# Users 
- tokyo
- berlin
- professor
- nairobi
### Groups 
- developers
- admins
- project-team

# Group Assignments
## User and Groups 
- tokyo- tokyo, developers, project-team 
- berlin-berlin, developers, admins 
- professor- professor, admins 
- nairobi-nairobi, project-team
## Directories Created
| Directory | Group Owner | Permissions | Purpose |
|-----------|-------------|-------------|---------| 
| /opt/dev-project | developers | 775 (rwxrwxr-x) | Shared workspace for developers | 
| /opt/team-workspace | project-team | 775 (rwxrwxr-x) | Shared workspace for project team |
## Commands Used
#Create Users
```bash
sudo useradd -m tokyo
sudo passwd tokyo

sudo useradd -m berlin
sudo passwd berlin

sudo useradd -m professor
sudo passwd professor

sudo useradd -m nairobi
sudo passwd nairobi
Verify Users
cat /etc/passwd
ls /home
Create Groups
sudo groupadd developers
sudo groupadd admins
sudo groupadd project-team
Verify Groups
cat /etc/group
Add Users to Groups
sudo usermod -aG developers tokyo

sudo usermod -aG developers berlin
sudo usermod -aG admins berlin

sudo usermod -aG admins professor

sudo usermod -aG project-team tokyo
sudo usermod -aG project-team nairobi
Verify Group Membership
groups tokyo
groups berlin
groups professor
groups nairobi

id tokyo
id berlin
id professor
id nairobi
Create Shared Directories
sudo mkdir -p /opt/dev-project
sudo chgrp developers /opt/dev-project
sudo chmod 775 /opt/dev-project

sudo mkdir -p /opt/team-workspace
sudo chgrp project-team /opt/team-workspace
sudo chmod 775 /opt/team-workspace
Verify Directories
ls -ld /opt/dev-project
ls -ld /opt/team-workspace
Test Access
sudo -u tokyo touch /opt/dev-project/tokyo.txt
sudo -u berlin touch /opt/dev-project/berlin.txt

sudo -u nairobi touch /opt/team-workspace/nairobi.txt
Verify Files
ls -l /opt/dev-project
ls -l /opt/team-workspace

** What I learned **
Learned how to create Linux users with home directories and assign passwords.
Learned how to create groups, add users to multiple groups, and verify memberships using groups and id.
Learned how to create shared directories, change group ownership using chgrp, set permissions with chmod 775, and test access by switching users with sudo -u. 

