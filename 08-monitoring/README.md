# 📊 Linux System Monitoring

System monitoring helps us track the health and performance of a Linux system.

Linux provides many powerful tools to monitor:

- CPU usage
- Memory usage
- Disk usage
- Network activity
- Running processes
- System logs

Monitoring is one of the most important skills for Linux Administrators and DevOps Engineers.

---

# 📌 Why System Monitoring is Important?

System monitoring helps to:

✅ Detect performance issues  
✅ Troubleshoot server problems  
✅ Monitor CPU and memory usage  
✅ Check disk space  
✅ Analyze network activity  
✅ Monitor logs and services  

---

# 🖥 CPU and Memory Monitoring

---

# 🔹 top Command

`top` displays real-time system information.

```bash
top
```

Shows:

- CPU usage
- Memory usage
- Running processes
- System load

---

# 📌 Useful top Shortcuts

| Key | Purpose |
|---|---|
| `q` | Quit |
| `k` | Kill process |
| `r` | Change process priority |

---

# 🔹 htop Command

`htop` is an advanced and user-friendly version of top.

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
- easier navigation
- mouse support

---

# 🔹 vmstat Command

Displays CPU, memory, and I/O statistics.

```bash
vmstat
```

---

## Live Monitoring

```bash
vmstat 1 5
```

Meaning:
- update every 1 second
- show 5 updates

---

# 🔹 free Command

Displays memory usage.

```bash
free -m
```

Output shows:
- total memory
- used memory
- free memory

---

# 💾 Disk Monitoring

---

# 🔹 df Command

Checks disk space usage.

```bash
df -h
```

### Meaning

| Option | Purpose |
|---|---|
| `-h` | Human readable format |

---

# 🔹 du Command

Shows size of files and directories.

```bash
du -sh /var/log
```

### Meaning

| Option | Purpose |
|---|---|
| `-s` | Summary |
| `-h` | Human readable |

---

# 🔹 iostat Command

Displays CPU and disk I/O statistics.

```bash
iostat
```

Useful for:
- disk performance analysis
- storage troubleshooting

---

# 🌐 Network Monitoring

---

# 🔹 ip a Command

Displays network interfaces and IP addresses.

```bash
ip a
```

---

# 🔹 ifconfig Command

Older command for viewing network interfaces.

```bash
ifconfig
```

⚠️ Deprecated in modern Linux systems.

Use:

```bash
ip a
```

instead.

---

# 🔹 netstat Command

Displays active network connections and listening ports.

```bash
netstat -tulnp
```

---

# 🔹 ss Command

Modern alternative to netstat.

```bash
ss -tulnp
```

---

# 🔹 ping Command

Tests network connectivity.

```bash
ping google.com
```

---

# 🔹 traceroute Command

Displays network path to a destination.

```bash
traceroute google.com
```

Useful for:
- network troubleshooting
- latency analysis

---

# 🔹 nslookup Command

Checks DNS resolution.

```bash
nslookup google.com
```

---

# 📜 Log Monitoring

Logs are very important for troubleshooting Linux systems.

---

# 🔹 tail Command

Monitor logs in real-time.

```bash
tail -f /var/log/syslog
```

### Meaning

| Option | Purpose |
|---|---|
| `-f` | Follow log updates live |

---

# 🔹 journalctl Command

Displays systemd logs.

```bash
journalctl -f
```

Useful for:
- service troubleshooting
- system logs monitoring

---

# 🔹 dmesg Command

Displays kernel logs.

```bash
dmesg | tail
```

Useful for:
- hardware troubleshooting
- boot issue analysis

---

# 📊 Important Monitoring Commands Summary

| Command | Purpose |
|---|---|
| `top` | Real-time monitoring |
| `htop` | Advanced monitoring |
| `free -m` | Memory usage |
| `df -h` | Disk usage |
| `du -sh` | Directory size |
| `ip a` | Network details |
| `ss -tulnp` | Open ports |
| `ping` | Connectivity check |
| `tail -f` | Live log monitoring |

---

# 🚀 Real-Time DevOps Usage

DevOps Engineers use monitoring commands for:

- Monitoring production servers
- Troubleshooting applications
- Checking server health
- Monitoring logs
- Tracking CPU and memory usage
- Analyzing network issues
- Monitoring Kubernetes nodes

---

# ⚡ Common Troubleshooting Workflow

```text
Check CPU
    ↓
Check Memory
    ↓
Check Disk Space
    ↓
Check Network
    ↓
Check Logs
```

---

# 🔐 Best Practices

✅ Monitor disk usage regularly  
✅ Analyze logs frequently  
✅ Check high CPU processes  
✅ Monitor open ports  
✅ Use `htop` for better visibility  
✅ Keep system resources under control  

---

# 🎯 Summary

In this section, we learned:

✅ CPU monitoring  
✅ Memory monitoring  
✅ Disk monitoring  
✅ Network monitoring  
✅ Log monitoring  
✅ Real-time troubleshooting commands  

---

# 🧪 Practice Commands

## Open top

```bash
top
```

---

## Check Memory

```bash
free -m
```

---

## Check Disk Space

```bash
df -h
```

---

## Check Network Details

```bash
ip a
```

---

## Monitor Logs

```bash
tail -f /var/log/syslog
```

---

## Check Open Ports

```bash
ss -tulnp
```
