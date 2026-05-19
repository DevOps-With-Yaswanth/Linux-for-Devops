# 🏗️ Linux Architecture

Linux architecture defines how different components of the Linux operating system interact with each other.

Linux follows a layered architecture where each layer has a specific responsibility.

---

# 📌 Core Components of a Linux Machine

```text
+------------------------------------------------+
| User Applications (Vim, Docker, Apache, etc.) |
+------------------------------------------------+
| Shell (Bash, Zsh, Fish, etc.)                  |
+------------------------------------------------+
| System Libraries (glibc, libc, OpenSSL, etc.) |
+------------------------------------------------+
| System Utilities (ls, grep, systemctl, etc.)  |
+------------------------------------------------+
| Linux Kernel (Process, Memory, FS, Network)   |
+------------------------------------------------+
| Hardware (CPU, RAM, Disk, Network, Devices)   |
+------------------------------------------------+
```

---

# 🔹 Hardware Layer

The hardware layer contains physical components of the computer.

Examples:
- CPU
- RAM
- Hard Disk
- Network Card
- Keyboard
- Mouse

The operating system communicates with hardware using device drivers.

---

# 🔹 Linux Kernel

The kernel is the core part of the Linux operating system.

It directly interacts with hardware and manages system resources.

---

# 📌 Responsibilities of Kernel

## 🧠 Process Management
Manages running processes and CPU scheduling.

Examples:
- process creation
- process termination
- multitasking

---

## 💾 Memory Management
Allocates and deallocates RAM memory efficiently.

Responsibilities:
- virtual memory
- memory allocation
- swapping

---

## 📂 File System Management
Manages how data is stored and retrieved.

Examples:
- ext4
- xfs
- btrfs

---

## 🌐 Network Management
Handles communication between systems.

Examples:
- IP communication
- routing
- network packets

---

## 🔌 Device Management
Controls hardware devices using device drivers.

Examples:
- USB devices
- printers
- disks
- network adapters

---

# 🔹 Shell Layer

The shell acts as an interface between the user and the kernel.

Users execute commands through the shell.

---

# 📌 Popular Linux Shells

| Shell | Description |
|---|---|
| Bash | Most popular Linux shell |
| Zsh | Advanced shell with plugins |
| Fish | User-friendly shell |
| Ksh | Korn shell |

---

# 🔹 System Utilities

Linux provides many built-in utilities for administration and troubleshooting.

Examples:
- ls
- pwd
- grep
- top
- ps
- systemctl

---

# 🔹 System Libraries

System libraries help applications communicate with the kernel.

Examples:
- glibc
- libc
- OpenSSL

---

# 🔹 User Applications

Applications used by end users.

Examples:
- Vim
- Docker
- Apache
- Jenkins
- VS Code

Applications interact with the operating system through the shell and libraries.

---

# 🚀 Linux Architecture Workflow

```text
User
   ↓
Shell
   ↓
System Libraries
   ↓
Kernel
   ↓
Hardware
```

---

# ☁️ Linux Architecture in DevOps

DevOps tools run on top of Linux architecture.

Examples:
- Docker uses kernel namespaces and cgroups
- Kubernetes manages Linux containers
- Jenkins runs as a Linux service
- AWS EC2 servers mostly use Linux

---

# 📚 Summary

In this module we learned:

- Linux architecture
- Hardware layer
- Linux kernel
- Shell
- System utilities
- System libraries
- User applications
- Linux workflow
- Linux architecture in DevOps
