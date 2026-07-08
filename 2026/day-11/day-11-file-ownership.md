# Day 11 Challenge

## Files & Directories Created

### Files

* devops-file.txt
* team-notes.txt
* project-config.yaml
* heist-project/vault/gold.txt
* heist-project/plans/strategy.conf
* bank-heist/access-codes.txt
* bank-heist/blueprints.pdf
* bank-heist/escape-plan.txt

### Directories

* app-logs/
* heist-project/
* heist-project/vault/
* heist-project/plans/
* bank-heist/

---

## Ownership Changes

| File/Directory              | Before        | After                          |
| --------------------------- | ------------- | ------------------------------ |
| devops-file.txt             | ubuntu:ubuntu | tokyo:ubuntu → berlin:ubuntu   |
| team-notes.txt              | ubuntu:ubuntu | ubuntu:heist-team              |
| project-config.yaml         | ubuntu:ubuntu | professor:heist-team           |
| app-logs/                   | ubuntu:ubuntu | berlin:heist-team              |
| heist-project/              | ubuntu:ubuntu | professor:planners (Recursive) |
| bank-heist/access-codes.txt | ubuntu:ubuntu | tokyo:vault-team               |
| bank-heist/blueprints.pdf   | ubuntu:ubuntu | berlin:tech-team               |
| bank-heist/escape-plan.txt  | ubuntu:ubuntu | nairobi:vault-team             |

---

## Commands Used

```bash
cd ~

touch devops-file.txt
ls -l devops-file.txt

sudo useradd -m tokyo
sudo useradd -m berlin
sudo useradd -m professor
sudo useradd -m nairobi

sudo groupadd heist-team
sudo groupadd planners
sudo groupadd vault-team
sudo groupadd tech-team

sudo chown tokyo devops-file.txt
sudo chown berlin devops-file.txt

touch team-notes.txt
sudo chgrp heist-team team-notes.txt

touch project-config.yaml
sudo chown professor:heist-team project-config.yaml

mkdir app-logs
sudo chown berlin:heist-team app-logs

mkdir -p heist-project/vault
mkdir -p heist-project/plans
touch heist-project/vault/gold.txt
touch heist-project/plans/strategy.conf

sudo chown -R professor:planners heist-project

mkdir bank-heist
touch bank-heist/access-codes.txt
touch bank-heist/blueprints.pdf
touch bank-heist/escape-plan.txt

sudo chown tokyo:vault-team bank-heist/access-codes.txt
sudo chown berlin:tech-team bank-heist/blueprints.pdf
sudo chown nairobi:vault-team bank-heist/escape-plan.txt

ls -l
ls -lR heist-project
ls -l bank-heist
```

---

## What I Learned

* Every file and directory in Linux has an **owner** and a **group** that determine access permissions.
* The **chown** command changes the file owner, **chgrp** changes the group, and **chown owner:group** changes both owner and group in a single command.
* Using the **-R** option with **chown** recursively changes ownership for all files and subdirectories inside a directory.

