Linux path structure

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

✅To temporarily switch to root:

sudo -i





---

## 🛠️ Linux File Operations  
Learn how to create, move, copy, delete, and manage files like a pro.

📂 Create a new directory

mkdir /ebin/my_folder

📝 Create file with content

echo "Hello, Linux!" > hello.txt

📋 View File Content

| Command            | Description               |
| ------------------ | ------------------------- |
| `cat file.txt`     | View entire file content  |
| `less file.txt`    | Scroll through long files |
| `head file.txt`    | Show first 10 lines       |
| `tail file.txt`    | Show last 10 lines        |
| `tail -f file.txt` | Live view of file updates |

🔄 Copy and Move


📑 Copy a file

cp source.txt backup.txt


📁 Copy a directory (recursive)


cp -r folder1 folder2


🚚 Move (rename) a file

mv oldname.txt newname.txt


🚚 Move file to another directory

mv file.txt /home/user/Documents/


❌ Delete Files and Folders

🗑️ Remove a file

rm file.txt


🗑️ Remove a directory (recursive)

rm -r folder_name


🔍 File Inspection

| Command             | Description                  |
| ------------------- | ---------------------------- |
| `ls`                | List files in current folder |
| `ls -l`             | Detailed file info           |
| `ls -a`             | Show hidden files            |
| `stat filename.txt` | File size, permissions, etc. |
| `file filename.txt` | Check file type              |



🔐 File Permissions

View permissions

ls -l file.txt


Change permissions

chmod 755 script.sh

Change owner

sudo chown user:user file.txt

🧠 Tips
Use tab key to auto-complete file names.

Use man <command> to read manual pages, e.g., man cp.

🔚 Summary Table

| Task              | Command Example          |
| ----------------- | ------------------------ |
| Create file       | `touch myfile.txt`       |
| Create directory  | `mkdir myfolder`         |
| Copy file         | `cp file1.txt file2.txt` |
| Move file         | `mv file.txt /path/`     |
| Delete file       | `rm file.txt`            |
| Delete folder     | `rm -r foldername`       |
| View content      | `cat`, `less`, `tail`    |
| Change permission | `chmod 755 file.sh`      |

Screenshot for Create directory
-----------------------------------------------------------
step1: 


🧾 Command 1:
![mkdir command execution](https://github.com/user-attachments/assets/3d68bded-eb40-420b-b64f-402756060c39)

mkdir /ebin/sample_folder

❌ Output:

mkdir: cannot create directory ‘/ebin/sample_folder’: No such file or directory

🔍 Explanation:

You're trying to create a folder /ebin/sample_folder directly under the root / directory.

But the parent directory /ebin does not exist, and mkdir by default cannot create missing parent folders.

So, the command fails with: No such file or directory.

🧾 Command 2:

mkdir -p /ebin/sample_folder

❌ Output:

mkdir: cannot create directory ‘/ebin’: Permission denied

🔍 Explanation:

The -p option tells mkdir to create parent directories if they don’t exist.

It tries to create /ebin and then /ebin/sample_folder.

But: You are a non-root user (dev@dev:~$), and you don’t have permission to write directly under /, which is protected.

So, you get: Permission denied.

🧾 Command 3:

sudo mkdir -p /ebin/sample_folder

✅ Output: (No error, command works)

🔍 Explanation:

sudo runs the command with superuser (root) privileges.

Now you’re allowed to create /ebin and /ebin/sample_folder under the root directory.

The -p ensures that if /ebin doesn't exist, it will be created too.


step 2:
![list created ddirectory](https://github.com/user-attachments/assets/43c4632e-14d2-4719-84a1-66bd5a74a5c4)

 ✅ 1. Using ls command

      ls /ebin

✅ 2. Using cd and pwd

cd /ebin/sample_folder

Then check your current location:

![find current location](https://github.com/user-attachments/assets/a14f6207-d794-45c0-a6ec-bb6617b11faf)

 pwd

Step 3: Create empty file 
![createnewfileandlistnewfile](https://github.com/user-attachments/assets/2140cc43-e295-4468-a8f5-fbd190f980ec)

  touch file1.txt
  
📌 Summary

| Command                | Purpose                             | Result              |
| ---------------------- | ----------------------------------- | ------------------- |
| `touch file1.txt`      | Try to create file (as normal user) | ❌ Permission denied |
| `sudo touch file1.txt` | Create file with root permission    | ✅ Success           |
| `ls`                   | List files in the current directory | ✅ Shows `file1.txt` |

step 4 : going to open vim editor and add content

![open vim editor and add content](https://github.com/user-attachments/assets/6cfd7a6d-19eb-4311-8861-c9f58f6e3d65)


step 5: view content in a file

![view content](https://github.com/user-attachments/assets/ebc4a113-ecf2-4b3b-acca-f6b4a611a58b)

cat file1.txt

📝 Insert and Save

| Action            | Command |
| ----------------- | ------- |
| Enter Insert mode | `i`     |
| Save file         | `:w`    |
| Quit Vim          | `:q`    |
| Save & Quit       | `:wq`   |
| Force Quit        | `:q!`   |


 Vim Copy / Cut / Paste Summary Table

 | Action                      | Vim Command         | Description                             |
| --------------------------- | ------------------- | --------------------------------------- |
| 📄 Copy (yank) current line | `yy`                | Copy the current line                   |
| 📄 Copy N lines             | `Nyy` (e.g., `5yy`) | Copy N lines starting from current line |
| 📄 Copy selection           | `v` → select → `y`  | Copy selected text in visual mode       |
| ✂️ Cut (delete) line        | `dd`                | Cut (delete) the current line           |
| ✂️ Cut N lines              | `Ndd` (e.g., `3dd`) | Cut N lines starting from current line  |
| ✂️ Cut selection            | `v` → select → `d`  | Cut selected text in visual mode        |
| 📥 Paste below              | `p`                 | Paste below the current line or cursor  |
| 📥 Paste above              | `P`                 | Paste above the current line or cursor  |

✅ Summary Table for Character Copy

| Action                 | Vim Command           | Explanation                  |
| ---------------------- | --------------------- | ---------------------------- |
| Start char-wise select | `v`                   | Start selecting characters   |
| Move right             | `l`, or `→` arrow key | Select characters one-by-one |
| Copy                   | `y`                   | Yank selected characters     |
| Paste                  | `p`                   | Paste after cursor           |
| Paste before cursor    | `P`                   | Paste before cursor          |

---

## 💽 Linux Partition Management  
Master partitioning, mounting, and managing storage devices in Linux.

---

