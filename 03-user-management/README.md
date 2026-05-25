# 👤 User Management in Linux

Linux is a multi-user operating system.

Multiple users can access and work on the same Linux server simultaneously.

User management is one of the most important responsibilities of a Linux Administrator and DevOps Engineer.

---

# 🎯 Why User Management is Important?

User management helps in:

✅ Security  
✅ Access control  
✅ Permission management  
✅ Resource management  
✅ Audit tracking  
✅ Multi-user collaboration

---

# 📂 Important Files Used in User Management

Linux stores user and group information inside important system files.

| File | Purpose |
|---|---|
| `/etc/passwd` | Stores user account information |
| `/etc/shadow` | Stores encrypted passwords |
| `/etc/group` | Stores group information |
| `/etc/gshadow` | Stores secure group details |

---

# 📄 Understanding `/etc/passwd`

This file stores user account details.

Example:

```bash
cat /etc/passwd
```

Sample entry:

```text
yaswanth:x:1001:1001:Yaswanth:/home/yaswanth:/bin/bash
```

---

# 📌 Fields Explanation

| Field | Meaning |
|---|---|
| yaswanth | Username |
| x | Password stored in shadow file |
| 1001 | User ID (UID) |
| 1001 | Group ID (GID) |
| Yaswanth | Description |
| /home/yaswanth | Home directory |
| /bin/bash | Default shell |

---

# 🔐 Understanding `/etc/shadow`

Stores encrypted user passwords.

Example:

```bash
sudo cat /etc/shadow
```

Only root users can access this file.

---

# 👥 Creating Users in Linux

---

# ➕ Create User using `useradd`

Basic syntax:

```bash
sudo useradd username
```

Example:

```bash
sudo useradd devops
```

This creates a user without a home directory.

---

# 🏠 Create User with Home Directory

```bash
sudo useradd -m username
```

Example:

```bash
sudo useradd -m devops
```

---

# 🐚 Create User with Specific Shell

```bash
sudo useradd -s /bin/bash username
```

Example:

```bash
sudo useradd -m -s /bin/bash devops
```

---

# 🚀 Using `adduser` (Interactive Method)

Mostly used in Ubuntu/Debian systems.

```bash
sudo adduser username
```

Example:

```bash
sudo adduser devops
```

This command:

✅ Creates home directory  
✅ Sets password  
✅ Asks user details interactively

---

# 🔑 Managing Passwords

---

# 🔒 Set or Change Password

```bash
sudo passwd username
```

Example:

```bash
sudo passwd devops
```

---

# ⏳ Password Expiry Policy

Set password expiry after 90 days:

```bash
sudo chage -M 90 username
```

Example:

```bash
sudo chage -M 90 devops
```

---

# 🔐 Lock User Account

```bash
sudo passwd -l username
```

Example:

```bash
sudo passwd -l devops
```

---

# 🔓 Unlock User Account

```bash
sudo passwd -u username
```

Example:

```bash
sudo passwd -u devops
```

---

# ✏️ Modifying Users using `usermod`

---

# 🔄 Change Username

```bash
sudo usermod -l new_username old_username
```

Example:

```bash
sudo usermod -l devopsadmin devops
```

---

# 🏠 Change Home Directory

```bash
sudo usermod -d /new/home/directory -m username
```

Example:

```bash
sudo usermod -d /home/devopsadmin -m devopsadmin
```

---

# 🐚 Change Default Shell

```bash
sudo usermod -s /bin/zsh username
```

Example:

```bash
sudo usermod -s /bin/bash devopsadmin
```

---

# ❌ Deleting Users

---

# Remove User Only

```bash
sudo userdel username
```

Example:

```bash
sudo userdel devops
```

Home directory remains.

---

# Remove User with Home Directory

```bash
sudo userdel -r username
```

Example:

```bash
sudo userdel -r devops
```

---

# 👥 Group Management in Linux

Groups help manage permissions for multiple users.

---

# ➕ Create Group

```bash
sudo groupadd groupname
```

Example:

```bash
sudo groupadd developers
```

---

# 👤 Add User to Group

```bash
sudo usermod -aG groupname username
```

Example:

```bash
sudo usermod -aG developers devops
```

---

# 🔍 Check User Groups

```bash
groups username
```

Example:

```bash
groups devops
```

---

# 🔄 Change Primary Group

```bash
sudo usermod -g groupname username
```

Example:

```bash
sudo usermod -g developers devops
```

---

# 🚀 Sudo Access in Linux

Sudo allows users to execute administrative commands.

---

# ➕ Add User to Sudo Group (Ubuntu/Debian)

```bash
sudo usermod -aG sudo username
```

Example:

```bash
sudo usermod -aG sudo devops
```

---

# ➕ Add User to Wheel Group (RHEL/CentOS)

```bash
sudo usermod -aG wheel username
```

Example:

```bash
sudo usermod -aG wheel devops
```

---

# ⚙️ Edit Sudoers File

Use:

```bash
sudo visudo
```

Example entry:

```text
devops ALL=(ALL) NOPASSWD:ALL
```

This gives passwordless sudo access.

---

# 📊 User Management Workflow

```text
Create User
     ↓
Assign Password
     ↓
Add to Group
     ↓
Grant Permissions
     ↓
Provide Sudo Access
     ↓
Monitor User Activity
```

---

# 🔥 Important Commands Summary

| Command | Purpose |
|---|---|
| `useradd` | Create user |
| `adduser` | Interactive user creation |
| `passwd` | Set password |
| `usermod` | Modify user |
| `userdel` | Delete user |
| `groupadd` | Create group |
| `groups` | View groups |
| `visudo` | Edit sudo permissions |

---

# 🧠 Real-Time DevOps Usage

DevOps Engineers use user management for:

✅ Managing server access  
✅ Creating deployment users  
✅ CI/CD user management  
✅ Kubernetes node access  
✅ SSH access control  
✅ Security hardening  
✅ Production server administration

---

# 🚀 Best Practices

✅ Use strong passwords  
✅ Avoid using root user directly  
✅ Grant minimum required permissions  
✅ Use groups for permission management  
✅ Monitor sudo access regularly  
✅ Remove inactive users

---

# 🎯 Summary

In this lesson we learned:

✅ User management basics  
✅ Important user files  
✅ Creating users  
✅ Password management  
✅ Group management  
✅ Sudo access  
✅ User modification  
✅ Deleting users

---
