
# Linux Installation on Windows using WSL2

## 📌 Introduction

In this guide, we will learn how to install Linux (Ubuntu) on Windows using WSL2 (Windows Subsystem for Linux).

WSL2 allows users to run a real Linux environment directly inside Windows without using VirtualBox or VMware.

This setup is lightweight, fast, and best suited for DevOps, Cloud, and Linux practice.

---

# 🚀 Why WSL2?

## Advantages of WSL2

- Lightweight and fast
- No need for Virtual Machine
- Real Linux Kernel support
- Easy to install and use
- Best for DevOps practice
- Low RAM usage
- Supports Docker and Kubernetes later

---

# 🖥️ System Requirements

- Windows 10 or Windows 11
- Minimum 8 GB RAM recommended
- Internet Connection
- Virtualization enabled in BIOS

---

# 📥 Step 1 — Open PowerShell as Administrator

1. Press `Windows Key`
2. Search for:

```powershell
PowerShell
```

3. Right-click on PowerShell
4. Select:

```text
Run as Administrator
```

---

# 📥 Step 2 — Install WSL2

Run the following command:

```powershell
wsl --install
```

This command will:

- Enable WSL feature
- Enable Virtual Machine Platform
- Install WSL2 components

---

# 🔄 Step 3 — Restart the System

After installation completes:

- Restart your laptop or desktop

This step is mandatory.

---

# 📥 Step 4 — Install Ubuntu

After restarting, open PowerShell again and run:

```powershell
wsl --install -d Ubuntu
```

This command will:

- Download Ubuntu
- Install Ubuntu
- Configure Linux environment

---

# ⏳ Step 5 — Wait for Installation

Ubuntu installation may take a few minutes depending on your internet speed.

Example:

```text
Downloading: Ubuntu
Installing: Ubuntu
Provisioning the new WSL instance Ubuntu
```

---

# 👤 Step 6 — Create Username and Password

After installation, Ubuntu will ask:

```text
Create a default Unix user account
```

Example:

```text
Enter new UNIX username: yaswanth
New password:
Retype new password:
```

> ⚠️ Note:
> Password will not be visible while typing.
> This is normal behavior in Linux.

---

# 📊 Step 7 — Verify Ubuntu Installation

Run the following command:

```bash
lsb_release -a
```

Expected Output:

```text
Distributor ID: Ubuntu
Description: Ubuntu 24.xx LTS
```

---

# 🔄 Step 8 — Update Ubuntu

Run:

```bash
sudo apt update && sudo apt upgrade -y
```

This command updates all Linux packages.

---

# ✅ Step 9 — Verify WSL Version

Open PowerShell and run:

```powershell
wsl -l -v
```

Expected Output:

```text
NAME      STATE           VERSION
Ubuntu    Running         2
```

> Ensure the VERSION is `2`

---

# ▶️ How to Open Linux

## Method 1

Press:

```text
Windows Key
```

Search:

```text
Ubuntu
```

Click Ubuntu.

---

## Method 2

Open PowerShell and run:

```powershell
wsl
```

---

# ❌ How to Close Linux

Inside Ubuntu terminal run:

```bash
exit
```

---

# 🛑 How to Shutdown WSL

Open PowerShell and run:

```powershell
wsl --shutdown
```

---

# 📂 Access Linux Files from Windows

Open File Explorer and enter:

```text
\\wsl$
```

You can access Linux files directly from Windows.

---

# 📘 Basic Linux Commands

## Check Current Directory

```bash
pwd
```

## List Files

```bash
ls
```

## Create Folder

```bash
mkdir demo
```

## Change Directory

```bash
cd demo
```

## Create File

```bash
touch file.txt
```

## Display File Content

```bash
cat file.txt
```

## Clear Terminal

```bash
clear
```

---

# 🛠️ Recommended Tools

## Visual Studio Code

Install:

https://code.visualstudio.com/

Recommended Extensions:

- WSL
- Docker
- Kubernetes

---

# 📌 Conclusion

WSL2 is the best way to learn Linux and DevOps on Windows systems.

It provides a lightweight and real Linux environment suitable for:

- Linux Administration
- Shell Scripting
- Git
- Docker
- Kubernetes
- DevOps Tools

This setup is highly recommended for beginners and DevOps learners.

---
