# 📁 Linux Folder Structure

Linux follows a hierarchical file system structure.

Everything in Linux starts from the root directory:

```bash
/
```

Understanding the Linux folder structure is very important for:

- DevOps Engineers
- System Administrators
- Cloud Engineers
- Linux Administrators

---

# 🏗 Linux File System Hierarchy

```text
/
├── bin
├── boot
├── dev
├── etc
├── home
├── lib
├── media
├── mnt
├── opt
├── proc
├── root
├── run
├── sbin
├── srv
├── sys
├── tmp
├── usr
└── var
```

---

# 🔗 Symbolic Links (Less Significant)

In modern Linux systems, some directories are symbolic links.

| Directory | Description |
|---|---|
| `/sbin -> /usr/sbin` | System binaries for administrative commands |
| `/bin -> /usr/bin` | Essential user binaries |
| `/lib -> /usr/lib` | Shared libraries and kernel modules |

Symbolic links help Linux maintain compatibility and simplify file management.

---

# 📌 Important System Directories

| Directory | Description |
|---|---|
| `/boot` | Stores files required for booting the Linux system |
| `/usr` | Contains most user-installed applications and libraries |
| `/var` | Stores logs, cache, and temporary changing files |
| `/etc` | Stores system configuration files |

---

# 👤 User & Application-Specific Directories

| Directory | Description |
|---|---|
| `/home` | Default location for user home directories |
| `/opt` | Used for optional third-party software |
| `/srv` | Stores service-related data |
| `/root` | Home directory of the root user |

---

# ⚡ Temporary & Volatile Directories

| Directory | Description |
|---|---|
| `/tmp` | Stores temporary files |
| `/run` | Holds runtime process information |
| `/proc` | Virtual filesystem for process and system information |
| `/sys` | Virtual filesystem for hardware and kernel information |
| `/dev` | Contains device files |

---

# 💾 Mount Points

| Directory | Description |
|---|---|
| `/mnt` | Temporary mount point for external filesystems |
| `/media` | Mount point for removable media devices |
| `/data` | Common custom mount point for additional storage |

---

# 📂 Detailed Explanation of Important Directories

---

# 📁 `/etc`

The `/etc` directory contains system configuration files.

Examples:

```bash
/etc/passwd
/etc/hostname
/etc/ssh/
```

DevOps engineers frequently work inside this directory while configuring services.

---

# 📁 `/var`

The `/var` directory stores variable and changing files.

Examples:

```bash
/var/log
/var/cache
```

Very important for troubleshooting production issues.

---

# 📁 `/home`

Contains personal directories of normal users.

Example:

```bash
/home/yaswanth
```

Each user gets a separate workspace.

---

# 📁 `/root`

Home directory of the root user.

```bash
/root
```

Used mainly by system administrators.

---

# 📁 `/tmp`

Stores temporary files.

Temporary files may be automatically deleted after reboot.

---

# 📁 `/proc`

A virtual filesystem that provides system and process information.

Useful files:

```bash
/proc/cpuinfo
/proc/meminfo
```

Helpful for monitoring CPU and memory usage.

---

# 📁 `/dev`

Linux treats hardware devices as files.

Examples:

```bash
/dev/sda
/dev/null
/dev/tty
```

---

# 📁 `/usr`

Contains applications, libraries, and utilities.

Examples:

```bash
/usr/bin
/usr/lib
/usr/share
```

Most Linux applications are installed here.

---

# 🔥 Important Linux Navigation Commands

---

## Print Current Directory

```bash
pwd
```

---

## List Files and Directories

```bash
ls
```

Detailed list:

```bash
ls -ltr
```

---

## Change Directory

```bash
cd /etc
```

Move back:

```bash
cd ..
```

Move to home directory:

```bash
cd ~
```

---

# 🧠 Real-Time DevOps Usage

| Directory | DevOps Usage |
|---|---|
| `/etc` | Configuration management |
| `/var/log` | Log troubleshooting |
| `/tmp` | Temporary deployment files |
| `/proc` | Monitoring CPU and memory |
| `/usr` | Installed applications |
| `/dev` | Storage and device management |

---

# 🚀 Why Linux File Structure is Important for DevOps?

Understanding Linux directories helps DevOps engineers:

✅ Troubleshoot servers quickly  
✅ Configure applications properly  
✅ Analyze logs efficiently  
✅ Manage storage and mounts  
✅ Understand Linux internals  
✅ Work confidently in production environments

---

# 🎯 Summary

In this lesson we learned:

✅ Linux file system hierarchy  
✅ Important Linux directories  
✅ Symbolic links  
✅ Temporary directories  
✅ Mount points  
✅ File navigation commands  
✅ Real-time DevOps usage

---
