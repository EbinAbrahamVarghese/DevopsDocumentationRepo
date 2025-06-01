# 🐧 Linux Essentials Guide

## 🔐 User Prompt Meaning

In a Linux terminal, the command prompt shows who you are and where you are in the system.

### 👤 Non-root User Prompt
```bash
dev@dev:~$
| Symbol | Meaning                        |
| ------ | ------------------------------ |
| `dev`  | Username                       |
| `@dev` | Hostname (computer/VM name)    |
| `~`    | Current path (`/home/dev`)     |
| `$`    | Regular (non-root) user prompt |

🧑‍💻 Root User Prompt

root@dev:~#

| Symbol | Meaning                 |
| ------ | ----------------------- |
| `root` | Logged in as superuser  |
| `@dev` | Hostname                |
| `~`    | Current path (`/root`)  |
| `#`    | Root user prompt symbol |


 Note: The # symbol indicates full system access. Use with caution

📂 Path Symbols in Linux

| Symbol | Meaning                           |
| ------ | --------------------------------- |
| `/`    | Root directory (top of all paths) |
| `~`    | Current user’s home directory     |
| `.`    | Current directory                 |
| `..`   | Parent directory                  |


📁 Example Path Use Cases

✅ Navigate to root:

cd /

✅ Go to home directory:

cd ~


✅ Go up one directory:

cd ..

✅ Move to specific path:

cd /etc/network








---

## 🛠️ Linux File Operations  
Learn how to create, move, copy, delete, and manage files like a pro.

---

## 💽 Linux Partition Management  
Master partitioning, mounting, and managing storage devices in Linux.

---

