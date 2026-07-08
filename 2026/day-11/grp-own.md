## Understanding Owner and Group

### What is an Owner?

The **owner** is the user who owns a file or directory. By default, the user who creates a file becomes its owner. The owner can read, modify, delete the file (subject to permissions), and can change its permissions or ownership.

**Example:**

```text
-rw-r--r-- 1 ubuntu ubuntu 0 Jul 8 devops-file.txt
```

Here, the **owner** is **ubuntu** (the first `ubuntu`).

---

### What is a Group?

A **group** is a collection of users. Every file belongs to one group. Group permissions allow multiple users in the same group to access a file without making each one the owner.

**Example:**

```text
-rw-r--r-- 1 ubuntu heist-team 0 Jul 8 team-notes.txt
```

Here, the **group** is **heist-team**.

---

### Difference Between Owner and Group

| Owner                                               | Group                                                        |
| --------------------------------------------------- | ------------------------------------------------------------ |
| A single user who owns the file.                    | A collection of users who share access to the file.          |
| Usually the user who created the file.              | Assigned to allow multiple users to access the file.         |
| Changed using `chown`.                              | Changed using `chgrp` or `chown owner:group`.                |
| Has permissions based on the owner permission bits. | Members have permissions based on the group permission bits. |

---

### File Format Explanation

```text
-rw-r--r-- 1 ubuntu ubuntu 0 Jul 8 devops-file.txt
```

| Field             | Description          |
| ----------------- | -------------------- |
| `-rw-r--r--`      | File permissions     |
| `1`               | Number of hard links |
| `ubuntu`          | Owner                |
| `ubuntu`          | Group                |
| `0`               | File size (bytes)    |
| `Jul 8`           | Last modified date   |
| `devops-file.txt` | File name            |


