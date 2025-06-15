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


