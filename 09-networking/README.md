# 🌐 Networking in Linux

Networking allows computers and servers to communicate with each other.

Linux provides many powerful networking commands to:
- test connectivity
- check IP addresses
- monitor ports
- troubleshoot networks
- download files

Networking is one of the most important topics for Linux and DevOps Engineers.

---

# 📌 Why Networking is Important?

Networking is used in:

- Cloud Computing
- DevOps
- Docker
- Kubernetes
- SSH
- APIs
- Web Applications

Without networking, systems cannot communicate.

---

# 🧠 Basic Networking Concepts

---

# 🔹 What is an IP Address?

An IP address is the unique address of a device in a network.

Example:

```text
192.168.1.10
```

Like a home address for computers.

---

# 🔹 Types of IP Addresses

| Type | Description |
|---|---|
| Public IP | Internet-facing IP |
| Private IP | Internal network IP |

---

# 🔹 What is a Port?

Ports are communication endpoints.

Examples:

| Port | Service |
|---|---|
| 22 | SSH |
| 80 | HTTP |
| 443 | HTTPS |

---

# 🔹 What is DNS?

DNS converts domain names into IP addresses.

Example:

```text
google.com → 142.x.x.x
```

Humans remember names.
Computers use IP addresses.

---

# 🔹 TCP vs UDP

| TCP | UDP |
|---|---|
| Reliable | Faster |
| Connection-oriented | Connectionless |

---

# 🌐 Networking Commands in Linux

---

# 🔹 ping Command

Checks connectivity to another server.

```bash
ping google.com
```

Used for:
- testing internet connection
- checking server availability
- troubleshooting network issues

---

# 🔹 ip a Command

Displays IP addresses and network interfaces.

```bash
ip a
```

Shows:
- IP address
- interface name
- network status

---

# 🔹 ifconfig Command

Older networking command.

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

Useful for:
- checking open ports
- troubleshooting services
- monitoring connections

---

# 🔹 ss Command

Modern replacement for netstat.

```bash
ss -tulnp
```

Faster and more efficient.

---

# 🔹 curl Command

Fetches data from websites or APIs.

```bash
curl https://example.com
```

Used for:
- API testing
- checking server responses
- debugging web applications

---

# 🔹 wget Command

Downloads files from the internet.

```bash
wget https://example.com/file.zip
```

Used for:
- downloading software
- scripts
- packages

---

# 📊 Networking Workflow

```text
Device
   ↓
IP Address
   ↓
DNS Resolution
   ↓
Server Connection
   ↓
Data Transfer
```

---

# 🚀 Real-Time DevOps Usage

DevOps Engineers use networking commands for:

- checking server connectivity
- troubleshooting applications
- testing APIs
- verifying open ports
- monitoring Kubernetes networking
- SSH troubleshooting

---

# 🔥 Important Commands Summary

| Command | Purpose |
|---|---|
| `ping` | Test connectivity |
| `ip a` | Show IP address |
| `netstat` | View open ports |
| `ss` | Socket statistics |
| `curl` | Fetch webpage/API |
| `wget` | Download files |

---

# 🔐 Best Practices

✅ Use `ping` to test connectivity  
✅ Use `ss` instead of `netstat`  
✅ Verify open ports regularly  
✅ Check IP before troubleshooting  
✅ Use curl for API testing  

---

# 🎯 Summary

In this section, we learned:

✅ Networking basics  
✅ IP addresses  
✅ Ports  
✅ DNS  
✅ TCP vs UDP  
✅ Linux networking commands  
✅ Real-time troubleshooting basics  

---

# 🧪 Practice Commands

## Check Internet Connectivity

```bash
ping google.com
```

---

## View IP Address

```bash
ip a
```

---

## Check Open Ports

```bash
ss -tulnp
```

---

## Fetch Website Content

```bash
curl https://example.com
```

---

## Download File

```bash
wget https://example.com/file.zip
```
