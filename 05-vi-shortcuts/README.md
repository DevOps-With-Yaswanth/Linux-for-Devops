# ✍️ VI Editor Shortcuts

VI Editor is one of the most powerful text editors available in Linux.

It is widely used by:

- Linux Administrators
- DevOps Engineers
- Cloud Engineers
- Developers

Most Linux servers use VI/VIM for editing configuration files, scripts, and logs.

---

# 📌 Modes in VI Editor

VI Editor works in different modes.

| Mode | Purpose |
|---|---|
| Normal Mode | Navigation and commands |
| Insert Mode | Writing and editing text |
| Command Mode | Saving, quitting, searching |

---

# 🔹 Normal Mode

This is the default mode when you open a file.

Example:

```bash
vi file.txt
```

Used for:

- Moving inside the file
- Copying text
- Deleting text
- Searching text

---

# 🔹 Insert Mode

Used for typing and editing content.

Press:

```bash
i
```

to enter Insert Mode.

Press:

```bash
Esc
```

to return to Normal Mode.

---

# 🔹 Command Mode

Used for:

- Saving files
- Quitting editor
- Search and replace

Press:

```bash
:
```

from Normal Mode to enter Command Mode.

---

# 📍 Basic Navigation Shortcuts

| Shortcut | Description |
|---|---|
| `h` | Move left |
| `l` | Move right |
| `j` | Move down |
| `k` | Move up |
| `0` | Move to beginning of line |
| `^` | Move to first character |
| `$` | Move to end of line |
| `w` | Move to next word |
| `b` | Move to previous word |
| `gg` | Go to start of file |
| `G` | Go to end of file |
| `:n` | Go to line number |

Example:

```bash
:20
```

Moves to line 20.

---

# ✏️ Insert Mode Shortcuts

| Shortcut | Description |
|---|---|
| `i` | Insert before cursor |
| `I` | Insert at beginning of line |
| `a` | Insert after cursor |
| `A` | Insert at end of line |
| `o` | Open new line below |
| `O` | Open new line above |
| `Esc` | Exit insert mode |

---

# 🗑 Editing Shortcuts

| Shortcut | Description |
|---|---|
| `x` | Delete character |
| `X` | Delete previous character |
| `dw` | Delete word |
| `dd` | Delete line |
| `d$` | Delete to end of line |
| `d0` | Delete to beginning of line |
| `D` | Delete to end of line |
| `u` | Undo |
| `Ctrl + r` | Redo |
| `yy` | Copy line |
| `yw` | Copy word |
| `p` | Paste after cursor |
| `P` | Paste before cursor |

---

# 🔍 Search and Replace

## Search Text

Search forward:

```bash
/pattern
```

Example:

```bash
/nginx
```

Search backward:

```bash
?pattern
```

---

## Repeat Search

| Shortcut | Description |
|---|---|
| `n` | Next match |
| `N` | Previous match |

---

# 🔄 Replace Text

Replace all occurrences:

```bash
:%s/old/new/g
```

Example:

```bash
:%s/nginx/apache/g
```

Replace only in current line:

```bash
:s/old/new/g
```

---

# 💾 Save and Exit Commands

| Command | Description |
|---|---|
| `:w` | Save file |
| `:q` | Quit |
| `:wq` | Save and quit |
| `:q!` | Quit without saving |

---

# 📂 Working with Multiple Files

Open another file:

```bash
:e filename
```

Example:

```bash
:e test.txt
```

---

# 🖥 Split Screen in VI

## Horizontal Split

```bash
:split filename
```

---

## Vertical Split

```bash
:vsplit filename
```

---

## Switch Between Screens

```bash
Ctrl + w + w
```

---

# 🚀 Real-Time DevOps Usage

DevOps Engineers use VI Editor for:

- Editing Kubernetes YAML files
- Updating Docker configurations
- Editing Jenkins pipelines
- Modifying Linux configuration files
- Monitoring logs
- Writing shell scripts

---

# 📊 Simple VI Workflow

```text
Open File → Edit Content → Save Changes → Exit
```

Example:

```bash
vi app.conf
```

Press:

```bash
i
```

Edit content.

Then:

```bash
Esc
:wq
```

to save and exit.

---

# ⚡ Most Important Shortcuts for Beginners

| Shortcut | Purpose |
|---|---|
| `i` | Insert mode |
| `Esc` | Exit insert mode |
| `:wq` | Save and quit |
| `:q!` | Quit without saving |
| `dd` | Delete line |
| `yy` | Copy line |
| `p` | Paste |
| `/word` | Search word |

---

# ✅ Best Practices

✔️ Always press `Esc` before commands  
✔️ Use `:wq` to save work  
✔️ Practice navigation keys regularly  
✔️ Learn search and replace commands  
✔️ Use split screen for comparing files  

---

# 🎯 Summary

In this section, we learned:

✅ VI Editor modes  
✅ Navigation shortcuts  
✅ Insert mode commands  
✅ Editing shortcuts  
✅ Search and replace  
✅ Save and exit commands  
✅ Multiple file handling  

---

# 🧪 Practice Commands

```bash
vi demo.txt
```

Try these inside VI:

```text
i
Hello Linux
Esc
:wq
```

Then reopen the file and practice:

```text
dd
yy
p
/nginx
```
