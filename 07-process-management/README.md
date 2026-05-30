# ⚙️ Process Management in Linux

A process is a running instance of a program.

Whenever you run a command or application in Linux, a process is created.

Examples:
- Opening a browser
- Running a shell script
- Starting Docker
- Running Jenkins

All these create processes in Linux.

---

# 📌 Why Process Management is Important?

Process management helps to:

✅ Monitor running applications  
✅ Control system resources  
✅ Stop unwanted processes  
✅ Improve system performance  
✅ Troubleshoot servers  

Process management is one of the most important skills for Linux and DevOps Engineers.

---

# 🆔 What is PID?

Every process in Linux has a unique:

```text
PID → Process ID
```

Linux uses PID to identify and manage processes.

---

# 📊 Process Hierarchy

Linux processes follow a parent-child relationship.

```text
System Process
      ↓
Parent Process
      ↓
Child Process
```

Each process is started by another process.

---

# 🔍 Viewing Processes

---

# 🔹 ps Command

Displays running processes.

```bash
ps
```

---

## View All Processes

```bash
ps aux
```

### Meaning of Options

| Option | Description |
|---|---|
| a | All users |
| u | User-oriented format |
| x | Background processes |

---

## View Processes for Specific User

```bash
ps -u username
```

Example:

```bash
ps -u ubuntu
```

---

## Find Process by Name

```bash
ps -C nginx
```

---

# 🔹 pgrep Command

Find process ID using process name.

```bash
pgrep nginx
```

---

# 🔹 pidof Command

Displays PID of running program.

```bash
pidof nginx
```

---

# ❌ Managing Processes

---

# 🔹 kill Command

Terminate process using PID.

```bash
kill PID
```

Example:

```bash
kill 1234
```

---

# 🔹 pkill Command

Kill process using process name.

```bash
pkill nginx
```

---

# 🔥 Force Kill Process

```bash
kill -9 PID
```

Example:

```bash
kill -9 1234
```

⚠️ Force kill should be used carefully.

---

# 🔥 Kill All Instances

```bash
pkill -9 nginx
```

---

# ⏸ Stop a Process

Temporarily stop process execution.

```bash
kill -STOP PID
```

---

# ▶ Resume a Process

```bash
kill -CONT PID
```

---

# 📈 Process Priority

Linux allows setting process priority.

Higher priority process gets more CPU time.

---

# 🔹 nice Command

Start process with custom priority.

```bash
nice -n 10 command
```

Example:

```bash
nice -n 10 python app.py
```

---

# 🔹 renice Command

Change priority of existing process.

Lower priority:

```bash
renice -n 10 -p PID
```

Higher priority:

```bash
sudo renice -n -5 -p PID
```

---

# 📊 Viewing Priority in top

Run:

```bash
top
```

Look at:

```text
NI column
```

NI = Nice Value

---

# 🖥 Monitoring Processes

---

# 🔹 top Command

Interactive Linux process viewer.

```bash
top
```

---

# Useful top Shortcuts

| Key | Action |
|---|---|
| k | Kill process |
| r | Change priority |
| q | Quit |

---

# 🔹 htop Command

Advanced and user-friendly process viewer.

Install:

```bash
sudo apt install htop
```

Run:

```bash
htop
```

Features:
- colorful interface
- easy navigation
- mouse support

---

# ⚙️ Background & Foreground Processes

---

# 🔹 Run Process in Background

```bash
command &
```

Example:

```bash
sleep 100 &
```

---

# 🔹 View Background Jobs

```bash
jobs
```

---

# 🔹 Bring Job to Foreground

```bash
fg %jobnumber
```

Example:

```bash
fg %1
```

---

# 🔹 Suspend Running Process

Press:

```text
Ctrl + Z
```

---

# 🔹 Resume Process in Background

```bash
bg %jobnumber
```

---

# 🔧 Daemon Processes

Daemon processes run in the background continuously.

Examples:
- nginx
- docker
- ssh
- jenkins

---

# 🔹 List Services

```bash
systemctl list-units --type=service
```

---

# 🔹 Start Service

```bash
systemctl start nginx
```

---

# 🔹 Stop Service

```bash
systemctl stop nginx
```

---

# 🔹 Enable Service at Startup

```bash
systemctl enable nginx
```

---

# 🔹 Check Service Status

```bash
systemctl status nginx
```

---

# 📊 Basic Process Workflow

```text
Start Process
      ↓
Monitor Process
      ↓
Manage Priority
      ↓
Stop or Restart Process
```

---

# 🚀 Real-Time DevOps Usage

DevOps Engineers use process management for:

- Monitoring servers
- Managing Docker containers
- Checking Jenkins processes
- Troubleshooting applications
- Monitoring Kubernetes nodes
- Managing system services

---

# 🔐 Best Practices

✅ Monitor high CPU processes regularly  
✅ Avoid unnecessary force kill (`kill -9`)  
✅ Use `top` or `htop` for monitoring  
✅ Restart stuck services properly  
✅ Check logs before killing processes  

---

# ⚠️ Important Notes

| Command | Usage |
|---|---|
| `kill -9` | Forcefully kills process |
| `top` | Monitor live processes |
| `jobs` | Show background jobs |
| `systemctl` | Manage services |

---

# 🎯 Summary

In this section, we learned:

✅ What is a process  
✅ Process ID (PID)  
✅ Viewing processes  
✅ Killing processes  
✅ Background processes  
✅ Process priority  
✅ top and htop  
✅ Daemon services  
✅ systemctl basics  

---

# 🧪 Practice Commands

## View Running Processes

```bash
ps aux
```

---

## Find Nginx Process

```bash
pgrep nginx
```

---

## Run Background Job

```bash
sleep 100 &
```

---

## View Jobs

```bash
jobs
```

---

## Open top

```bash
top
```

---

## Start Nginx Service

```bash
sudo systemctl start nginx
```
