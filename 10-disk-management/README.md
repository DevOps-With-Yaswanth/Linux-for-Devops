# 💽 Disk Management in Linux

Disk management is the process of managing storage devices in Linux.

Linux provides commands to:

- view disks
- create partitions
- format disks
- mount storage
- manage swap space
- monitor disk usage

Disk management is very important for Linux Administrators and DevOps Engineers.

---

# 📌 Why Disk Management is Important?

Disk management helps to:

✅ Manage storage efficiently  
✅ Add new disks to servers  
✅ Monitor disk usage  
✅ Prevent storage issues  
✅ Configure partitions  
✅ Manage application storage  

---

# 🧠 Basic Disk Concepts

---

# 🔹 What is a Disk?

A disk is a storage device.

Examples:
- HDD
- SSD
- NVMe

Linux identifies disks like:

```text
/dev/sda
/dev/sdb
```

---

# 🔹 What is a Partition?

A partition divides a disk into smaller sections.

Examples:

```text
/dev/sda1
/dev/sda2
```

---

# 🔹 What is a Filesystem?

A filesystem organizes data inside partitions.

Common filesystems:

| Filesystem | Usage |
|---|---|
| ext4 | Most common Linux filesystem |
| xfs | Enterprise storage |
| vfat | USB drives |

---

# 🔹 What is Mounting?

Mounting makes storage accessible inside Linux directories.

Example:

```text
/dev/sdb1 → /data
```

---

# 📊 Viewing Disk Information

---

# 🔹 lsblk Command

Displays block devices.

```bash
lsblk
```

Shows:
- disks
- partitions
- mount points

---

# 🔹 fdisk Command

Displays partition information.

```bash
sudo fdisk -l
```

---

# 🔹 blkid Command

Displays UUID information.

```bash
blkid
```

UUID is used for permanent mounting.

---

# 🔹 df Command

Displays disk space usage.

```bash
df -h
```

---

# 🔹 du Command

Shows directory size.

```bash
du -sh /var/log
```

---

# 🛠 Partition Management

---

# 🔹 Create Partition using fdisk

```bash
sudo fdisk /dev/sdb
```

Inside fdisk:

| Key | Purpose |
|---|---|
| `n` | Create partition |
| `p` | Print partition table |
| `w` | Save changes |
| `q` | Quit |

---

# 🔹 parted Command

Alternative to fdisk.

```bash
sudo parted /dev/sdb
```

Used mostly for:
- GPT partitions
- large disks

---

# 💾 Formatting Partitions

Before using a partition, it must be formatted.

---

# 🔹 Format as ext4

```bash
sudo mkfs.ext4 /dev/sdb1
```

---

# 🔹 Format as XFS

```bash
sudo mkfs.xfs /dev/sdb1
```

---

# 📂 Mounting and Unmounting

---

# 🔹 Mount a Partition

```bash
sudo mount /dev/sdb1 /mnt
```

Now storage becomes accessible.

---

# 🔹 Unmount a Partition

```bash
sudo umount /mnt
```

---

# 🔹 Remount as Read-Write

```bash
sudo mount -o remount,rw /mnt
```

---

# 📦 Logical Volume Management (LVM)

LVM provides flexible disk management.

Benefits:
- resize storage
- combine disks
- flexible allocation

---

# 🔹 Create Physical Volume

```bash
sudo pvcreate /dev/sdb
```

---

# 🔹 Create Volume Group

```bash
sudo vgcreate vg_data /dev/sdb
```

---

# 🔹 Create Logical Volume

```bash
sudo lvcreate -L 5G -n lv_data vg_data
```

---

# 🔹 Format Logical Volume

```bash
sudo mkfs.ext4 /dev/vg_data/lv_data
```

---

# 🔹 Mount Logical Volume

```bash
sudo mount /dev/vg_data/lv_data /mnt
```

---

# 🔄 Swap Management

Swap acts as virtual memory when RAM is full.

---

# 🔹 Create Swap

```bash
sudo mkswap /dev/sdb2
```

---

# 🔹 Enable Swap

```bash
sudo swapon /dev/sdb2
```

---

# 🔹 Disable Swap

```bash
sudo swapoff /dev/sdb2
```

---

# 📌 When to Use fdisk?

Use `fdisk` when:
- disk is new
- no partitions exist
- creating new storage layout

---

# 📌 When to Use mount?

Use `mount` when:
- partition already exists
- filesystem already created
- you only want to access storage

---

# 📌 Full Disk Setup Workflow

```text
Disk
   ↓
Partition
   ↓
Format
   ↓
Mount
   ↓
Use Storage
```

---

# 🚀 Full Example

## Check Available Disks

```bash
lsblk
```

---

## Create Partition

```bash
sudo fdisk /dev/sdb
```

---

## Format Partition

```bash
sudo mkfs.ext4 /dev/sdb1
```

---

## Create Mount Point

```bash
sudo mkdir /data
```

---

## Mount Partition

```bash
sudo mount /dev/sdb1 /data
```

---

## Verify Mount

```bash
df -h
```

---

# 🚀 Real-Time DevOps Usage

DevOps Engineers use disk management for:

- mounting storage volumes
- managing cloud disks
- Kubernetes persistent volumes
- monitoring disk usage
- troubleshooting storage issues
- configuring application storage

---

# 🔐 Best Practices

✅ Always check disks using `lsblk`  
✅ Never format wrong disks  
✅ Verify mount points carefully  
✅ Monitor disk usage regularly  
✅ Use UUID for permanent mounts  
✅ Take backups before partitioning  

---

# ⚠️ Important Warning

Be careful with:
- `fdisk`
- `mkfs`
- `rm`

Wrong usage can destroy data permanently.

---

# 🎯 Summary

In this section, we learned:

✅ Disk basics  
✅ Partitions  
✅ Filesystems  
✅ Mounting  
✅ LVM basics  
✅ Swap management  
✅ Disk monitoring commands  
✅ Real-time storage management  

---

# 🧪 Practice Commands

## View Disks

```bash
lsblk
```

---

## Check Disk Space

```bash
df -h
```

---

## Create Partition

```bash
sudo fdisk /dev/sdb
```

---

## Format Partition

```bash
sudo mkfs.ext4 /dev/sdb1
```

---

## Mount Partition

```bash
sudo mount /dev/sdb1 /mnt
```
