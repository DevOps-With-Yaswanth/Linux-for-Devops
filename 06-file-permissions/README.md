# 🔐 File Permissions in Linux

Linux file permissions control who can:

- Read files
- Modify files
- Execute programs

File permissions are very important for:

- Security
- User access control
- System protection

Every Linux file and directory has permissions.

---

# 📌 Why File Permissions are Important?

File permissions help to:

✅ Protect important files  
✅ Prevent unauthorized access  
✅ Control who can modify files  
✅ Improve Linux security  

---

# 👥 Types of Users in Linux

Linux permissions are divided into 3 categories.

| Type | Meaning |
|---|---|
| User (u) | File owner |
| Group (g) | Group users |
| Others (o) | Remaining users |

---

# 🔑 Types of Permissions

| Permission | Symbol | Number | Meaning |
|---|---|---|---|
| Read | r | 4 | View file content |
| Write | w | 2 | Edit file |
| Execute | x | 1 | Run file/program |

---

# 📄 Checking File Permissions

Use:

```bash
ls -l
```

Example:

```bash
-rwxr--r-- 1 ubuntu devops 1200 May 21 test.sh
```

---

# 📖 Understanding Permission Structure

```text
-rwxr--r--
```

Breakdown:

| Part | Meaning |
|---|---|
| `-` | File type |
| `rwx` | User permissions |
| `r--` | Group permissions |
| `r--` | Others permissions |

---

# 📊 Permission Meaning

| Permission | Meaning |
|---|---|
| `rwx` | Read, Write, Execute |
| `rw-` | Read, Write |
| `r--` | Read only |
| `---` | No permissions |

---

# 📁 Directory Permissions

Directory permissions work differently.

| Permission | Meaning |
|---|---|
| Read (r) | View files |
| Write (w) | Create/Delete files |
| Execute (x) | Enter directory |

---

# 🔧 Changing Permissions with chmod

`chmod` is used to change file permissions.

---

# 🔹 Symbolic Mode

## Add Execute Permission

```bash
chmod u+x file.sh
```

Adds execute permission to user.

---

## Remove Write Permission

```bash
chmod g-w file.sh
```

Removes write permission from group.

---

## Read Only for Others

```bash
chmod o=r file.sh
```

---

# 🔹 Full Permission Example

```bash
chmod u=rwx,g=rx,o= file.sh
```

Meaning:

| User | Group | Others |
|---|---|---|
| Full access | Read & Execute | No access |

---

# 🔢 Numeric (Octal) Permissions

Linux also supports numeric permissions.

| Permission | Number |
|---|---|
| Read | 4 |
| Write | 2 |
| Execute | 1 |

---

# 📊 Common Permission Values

| Number | Permission |
|---|---|
| 755 | rwxr-xr-x |
| 644 | rw-r--r-- |
| 700 | rwx------ |

---

# 🔹 chmod Examples

## Give Full Access to Owner

```bash
chmod 700 file.sh
```

---

## Public Read Access

```bash
chmod 644 file.txt
```

---

## Executable Script

```bash
chmod 755 script.sh
```

---

# 👤 Changing Ownership with chown

Used to change file owner.

---

## Change Owner

```bash
chown user1 file.txt
```

---

## Change Owner and Group

```bash
chown user1:devops file.txt
```

---

## Recursive Ownership Change

```bash
chown -R user1:devops project/
```

---

# 👥 Changing Group with chgrp

Used to change group ownership.

---

## Change Group

```bash
chgrp devops file.txt
```

---

## Recursive Group Change

```bash
chgrp -R devops project/
```

---

# ⭐ Special Permissions

Linux provides special permissions for advanced access control.

---

# 🔹 SUID (Set User ID)

Runs a file with owner's permissions.

```bash
chmod u+s file
```

Example:

```bash
/usr/bin/passwd
```

Allows users to change passwords.

---

# 🔹 SGID (Set Group ID)

Files run with group permissions.

```bash
chmod g+s file
```

For directories:

```bash
chmod g+s shared-folder
```

Files created inside inherit the same group.

---

# 🔹 Sticky Bit

Only file owner can delete files.

```bash
chmod +t folder
```

Example:

```bash
/tmp
```

---

# 📌 Understanding umask

`umask` defines default permissions for new files.

Check current umask:

```bash
umask
```

Set new umask:

```bash
umask 022
```

---

# 📊 Default Permissions

| Item | Default Permission |
|---|---|
| Files | 644 |
| Directories | 755 |

---

# 🚀 Real-Time DevOps Usage

DevOps Engineers use file permissions for:

- Shell scripts
- Jenkins pipelines
- Kubernetes files
- SSH keys
- Log files
- Server security

---

# 🔐 Important Security Tips

✅ Never give `777` permissions unnecessarily  
✅ Use least required permissions  
✅ Protect private keys with `600`  
✅ Use `755` for executable scripts  
✅ Regularly audit permissions  

---

# ⚠️ Dangerous Permission Example

```bash
chmod 777 file.txt
```

This gives:

- Read
- Write
- Execute

to everyone.

⚠️ Avoid using this in production servers.

---

# 📊 Simple Permission Workflow

```text
Create File → Check Permissions → Modify Permissions → Assign Ownership
```

---

# 🎯 Summary

In this section, we learned:

✅ Linux file permissions  
✅ User, Group, Others  
✅ Read, Write, Execute  
✅ chmod command  
✅ chown command  
✅ chgrp command  
✅ Special permissions  
✅ umask basics  

---

# 🧪 Practice Commands

## Create File

```bash
touch test.sh
```

---

## Check Permissions

```bash
ls -l test.sh
```

---

## Add Execute Permission

```bash
chmod +x test.sh
```

---

## Change Owner

```bash
sudo chown ubuntu test.sh
```

---

## Verify Changes

```bash
ls -l test.sh
```
