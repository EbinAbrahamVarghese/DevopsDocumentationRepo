🧑‍💻 Linux User Administration Notes

| User Type                | Description                                                |
| ------------------------ | ---------------------------------------------------------- |
| **Root**                 | Superuser with full system access (`UID 0`)                |
| **System/User Accounts** | Created by the OS for services (e.g., `www-data`, `mysql`) |
| **Normal Users**         | Regular human users (non-root users)                       |

🛠️ 2. User Management Commands

🔹 Create User

      sudo useradd username
	  
🔹 Create User with Home Directory

     sudo useradd -m username
	 
🔹 Set Password

    sudo passwd username
	
🔹 Delete User


    sudo userdel username         # without deleting home
	
    sudo userdel -r username      # delete user + home directory


👥 3. Group Management

🔹 Create Group

sudo groupadd groupname


🔹 Add User to Group


sudo usermod -aG groupname username


🔹 Remove User from Group


Remove manually from /etc/group


🔹 View Groups of a User

groups username


🔹 List Groups 

getent group or cat /etc/group



🔧 4. Modify User Info


| Task            | Command                                 |
| --------------- | --------------------------------------- |
| Change username | `sudo usermod -l newname oldname`       |
| Change home dir | `sudo usermod -d /new/path -m username` |
| Lock user       | `sudo usermod -L username`              |
| Unlock user     | `sudo usermod -U username`              |
| Expire account  | `sudo usermod -e YYYY-MM-DD username`   |


🔐 5. Sudo Access

sudo usermod -aG sudo username


📄 6. Important Files

| File           | Purpose                               |
| -------------- | ------------------------------------- |
| `/etc/passwd`  | Stores user account info              |
| `/etc/shadow`  | Stores encrypted passwords            |
| `/etc/group`   | Group details                         |
| `/etc/sudoers` | Sudo permissions (edit with `visudo`) |


📌 7. Default Files Created for a New User


| File/Dir              | Description                    |
| --------------------- | ------------------------------ |
| `/home/username/`     | User's home directory          |
| `.bashrc`, `.profile` | Shell configuration files      |
| `.ssh/`               | SSH keys and configs if set up |


🔍 8. Viewing Users

cat /etc/passwd


List all logged-in users:

who


Current logged-in user:


whoami


 🔧 Linux: Ownership മാറ്റൽ (Change Ownership) – Explained Clearly
 
 ✅ Ownership in Linux
 
Linux-ൽ ഓരോ ഫയലിനും/ഫോൾഡറിനും രണ്ട് പ്രധാന ഉടമസ്ഥതകൾ ഉണ്ടാകുന്നു:

| Type      | Example                                    |
| --------- | ------------------------------------------ |
| **Owner** | ഫയൽ സൃഷ്ടിച്ച വ്യക്തി (`user`)             |
| **Group** | ആ ഫയലുമായി ബന്ധിപ്പിച്ച ഗ്രൂപ്പ് (`group`) |


📌 Check Ownership:

ls -l filename


Example Output:

-rw-r--r-- 1 **john developers**  1234 Jun 15 10:00 report.txt


🔄 Change Ownership

🔹 Command:

sudo chown newowner filename


🔹 Example:

sudo chown alice report.txt


👥 Change Owner and Group Together


sudo chown newowner:newgroup filename

Example:

sudo chown alice:developers report.txt


📁 Change Ownership Recursively (folder + all contents)


sudo chown -R newowner:newgroup foldername


Example:

sudo chown -R alice:teamA /home/project/


📘 Summary Table:


| Task                 | Command Example                      |
| -------------------- | ------------------------------------ |
| Change owner         | `sudo chown alice file.txt`          |
| Change owner + group | `sudo chown alice:admin file.txt`    |
| Change recursively   | `sudo chown -R alice:admin /folder/` |
| View ownership       | `ls -l`                              |




🐚 Linux: Shell Change & Copying Shell Script File – Explained Clearly

🔁 1. Change Default Shell for a User

🔹 Check available shells:

cat /etc/shells


🔹 View current shell:

echo $SHELL

🔹 Change shell for current user:

chsh -s /bin/bash          # or /bin/zsh, /bin/sh, etc.


🔹 Change shell for another user:

sudo chsh -s /bin/bash username


📄 2. Copy a Shell Script File


🔹 Syntax:


cp source_path target_path


🔹 Example:


cp myscript.sh /usr/local/bin/


🔹 Make it executable:


chmod +x /usr/local/bin/myscript.sh



🧪 Example Workflow:

Create script:

nano backup.sh


Add content:

#!/bin/bash

echo "Backup started..."


Make it executable:


chmod +x backup.sh

Copy to bin:

sudo cp backup.sh /usr/local/bin/


Run:

backup.sh

Set Password Aging Policy for devuser1

sudo chage -m 2 -M 45 -W 7 devuser1


| Option  | Meaning                                             |
| ------- | --------------------------------------------------- |
| `-m 2`  | Minimum 2 days before password can be changed again |
| `-M 45` | Maximum 45 days before password expires             |
| `-W 7`  | Show warning 7 days before password expires         |


 Step 3: Verify the Policy

 sudo chage -l devuser1


 ✅ 1. Set Account Expiry Date (15 days from today)

 sudo chage -E $(date -d "+15 days" +%F) devuser2


🔍 What it does:

chage -E: Sets the account expiration date.


$(date -d "+15 days" +%F): Dynamically calculates the date 15 days from today in YYYY-MM-DD format.


devuser2: The target username.




✅ 2. Lock the Account Temporarily


sudo usermod -L devuser2


🔍 What it does:

usermod -L: Locks the account (disables password-based login).


🔒 The account is locked but not deleted. You can unlock it later using sudo usermod -U devuser2.


✅ Verify the Settings


Check expiry date


sudo chage -l devuser2


Check if account is locked:


sudo passwd -S devuser2


