# 📂 File Management in Linux

Linux provides powerful commands to create, manage, view, copy, move, and delete files and directories.

File management is one of the most important skills for Linux and DevOps Engineers.

---

# 📌 Why File Management is Important?

In Linux, almost everything is treated as a file:

- Files
- Directories
- Devices
- Logs
- Configuration files

As a DevOps Engineer, you will regularly work with:

- Log files
- Configuration files
- Shell scripts
- Application files
- Backup files

---

# 📁 File and Directory Management

## 🔹 ls — List Files and Directories

Displays files and folders in the current directory.

```bash
ls
```

### Common Options

```bash
ls -l
```

Shows detailed information.

```bash
ls -a
```

Shows hidden files.

```bash
ls -lh
```

Shows file sizes in human-readable format.

---

## 🔹 pwd — Present Working Directory

Displays the current directory path.

```bash
pwd
```

Example:

```bash
/home/ubuntu
```

---

## 🔹 cd — Change Directory

Used to move between directories.

```bash
cd /path/to/folder
```

Example:

```bash
cd /etc
```

### Move Back

```bash
cd ..
```

### Go to Home Directory

```bash
cd ~
```

---

## 🔹 mkdir — Create Directory

Creates a new folder.

```bash
mkdir project
```

### Create Multiple Directories

```bash
mkdir dev test prod
```

---

## 🔹 rmdir — Remove Empty Directory

Deletes an empty folder.

```bash
rmdir test
```

---

## 🔹 rm — Remove Files and Directories

Delete a file:

```bash
rm file.txt
```

Delete a folder recursively:

```bash
rm -r foldername
```

### Force Delete

```bash
rm -rf foldername
```

⚠️ Be careful with `rm -rf` because it permanently deletes files.

---

# 📄 File Copy and Move Operations

## 🔹 cp — Copy Files

Copy a file:

```bash
cp file1.txt file2.txt
```

### Copy Directory

```bash
cp -r dir1 dir2
```

---

## 🔹 mv — Move or Rename Files

Rename a file:

```bash
mv old.txt new.txt
```

Move a file:

```bash
mv file.txt /home/ubuntu/
```

---

# 📖 File Viewing Commands

## 🔹 cat — View File Content

```bash
cat file.txt
```

---

## 🔹 tac — Reverse File Content

Displays content from bottom to top.

```bash
tac file.txt
```

---

## 🔹 less — View Large Files

Allows scrolling up and down.

```bash
less file.txt
```

Press:

- `q` → Quit
- `/word` → Search text

---

## 🔹 more — View File Page by Page

```bash
more file.txt
```

---

## 🔹 head — First Lines of File

```bash
head -n 10 file.txt
```

Shows first 10 lines.

---

## 🔹 tail — Last Lines of File

```bash
tail -n 10 file.txt
```

Shows last 10 lines.

### Live Log Monitoring

```bash
tail -f app.log
```

Very useful for DevOps monitoring.

---

# ✏️ File Editing Commands

## 🔹 nano — Simple Text Editor

Easy editor for beginners.

```bash
nano file.txt
```

### Useful Shortcuts

- `CTRL + O` → Save
- `CTRL + X` → Exit

---

## 🔹 vi / vim — Powerful Linux Editor

```bash
vi file.txt
```

### Modes in VI

| Mode | Purpose |
|---|---|
| Normal Mode | Navigation |
| Insert Mode | Writing text |
| Command Mode | Save & Exit |

### Common Commands

| Command | Action |
|---|---|
| `i` | Insert mode |
| `Esc` | Exit insert mode |
| `:w` | Save |
| `:q` | Quit |
| `:wq` | Save and quit |
| `:q!` | Force quit |

---

# 📝 Writing Content to Files

## 🔹 Overwrite File Content

```bash
echo "Hello Linux" > file.txt
```

Creates or overwrites the file.

---

## 🔹 Append Content

```bash
echo "New Line" >> file.txt
```

Adds content without deleting existing data.

---

# 📊 Basic File Management Workflow

```text
Create File → Edit File → View File → Copy File → Move File → Delete File
```

---

# 🚀 Real-Time DevOps Usage

DevOps Engineers use file management daily for:

- Managing application logs
- Editing configuration files
- Monitoring server files
- Creating automation scripts
- Managing Kubernetes YAML files
- Working with Docker files

---

# ✅ Best Practices

✔️ Use `ls -lh` for readable file sizes  
✔️ Use `tail -f` for monitoring logs  
✔️ Be careful with `rm -rf`  
✔️ Use meaningful file names  
✔️ Keep backups before editing important files  

---

# 🎯 Summary

In this section, we learned:

✅ File and directory management  
✅ Copying and moving files  
✅ Viewing file content  
✅ Editing files using nano and vi  
✅ Removing files safely  
✅ Real-time DevOps file operations  

---

# 📚 Practice Commands

```bash
mkdir devops
cd devops
touch test.txt
echo "Hello Linux" > test.txt
cat test.txt
cp test.txt backup.txt
mv backup.txt newbackup.txt
rm newbackup.txt
```
