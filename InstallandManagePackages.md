1️⃣ Package Manager Used

Debian/Ubuntu uses:

| Tool   | Purpose                                       |
| ------ | --------------------------------------------- |
| `apt`  | Main tool to install, update, remove packages |
| `dpkg` | Low-level tool (for .deb files)               |


2️⃣ Update Package List

Always update package list first:

sudo apt update


3️⃣ Upgrade Installed Packages


To upgrade all packages to latest version:

sudo apt upgrade


4️⃣ Install a Package

Example 1: Install curl tool

sudo apt install curl


Example 2: Install git


sudo apt install git


5️⃣ Remove/Uninstall a Package


sudo apt remove curl


Example 2: Completely remove git with config files


sudo apt purge git


6️⃣ Clean Up

After removing packages, clean unused dependencies:

sudo apt autoremove


Clean downloaded package cache:


sudo apt clean


7️⃣ Search for a Package


apt search <package-name>

Example:


apt search nginx


8️⃣ Check Package Info


apt show <package-name>


Example:

apt show curl


9️⃣ Install a Local .deb File


If you have a .deb file (offline):


sudo dpkg -i file_name.deb


To fix missing dependencies:


sudo apt --fix-broken install


| **Action**                              | **Command/Script**                            | **Example**                         |           |            |
| --------------------------------------- | --------------------------------------------- | ----------------------------------- | --------- | ---------- |
| **1. Update package list**              | `sudo apt update`                             | `sudo apt update`                   |           |            |
| **2. Upgrade all packages**             | `sudo apt upgrade`                            | `sudo apt upgrade`                  |           |            |
| **3. Install a package**                | `sudo apt install <package-name>`             | `sudo apt install curl`             |           |            |
| **4. Reinstall a package**              | `sudo apt install --reinstall <package-name>` | `sudo apt install --reinstall curl` |           |            |
| **5. Remove a package (keep config)**   | `sudo apt remove <package-name>`              | `sudo apt remove curl`              |           |            |
| **6. Remove package + config files**    | `sudo apt purge <package-name>`               | `sudo apt purge curl`               |           |            |
| **7. Remove unused dependencies**       | `sudo apt autoremove`                         | `sudo apt autoremove`               |           |            |
| **8. Clean downloaded package files**   | `sudo apt clean`                              | `sudo apt clean`                    |           |            |
| **9. Search for a package**             | `apt search <package-name>`                   | `apt search nginx`                  |           |            |
| **10. Show package details**            | `apt show <package-name>`                     | `apt show curl`                     |           |            |
| **11. List installed packages**         | `dpkg -l`                                     | `dpkg -l`                           |           |            |
| **12. Check if a package is installed** | \`dpkg -l                                     | grep <package-name>\`               | \`dpkg -l | grep git\` |
| **13. Install local .deb file**         | `sudo dpkg -i file_name.deb`                  | `sudo dpkg -i google-chrome.deb`    |           |            |
| **14. Fix broken dependencies**         | `sudo apt --fix-broken install`               | `sudo apt --fix-broken install`     |           |            |
| **15. List files installed by package** | `dpkg -L <package-name>`                      | `dpkg -L curl`                      |           |            |
| **16. Find package owning a file**      | `dpkg -S /path/to/file`                       | `dpkg -S /usr/bin/curl`             |           |            |



📚 curl Usage (Debian/Ubuntu/Linux)

✅ What is curl?

👉 curl is a command-line tool to transfer data to or from a server

👉 It supports many protocols: HTTP, HTTPS, FTP, SFTP, etc.


👉 Mostly used to:


Download files

Test APIs

Send GET/POST requests


✅ Basic Syntax


curl [options] <URL>


✅ Simple Examples


| **Action**                        | **Command**                                                       |
| --------------------------------- | ----------------------------------------------------------------- |
| 1. Download a webpage             | `curl https://example.com`                                        |
| 2. Save output to a file          | `curl -o myfile.html https://example.com`                         |
| 3. Follow redirects               | `curl -L https://example.com`                                     |
| 4. Download a file                | `curl -O https://example.com/file.zip`                            |
| 5. Send GET request (API)         | `curl https://api.example.com/data`                               |
| 6. Send POST request (API)        | `curl -X POST -d "param1=value1" https://api.example.com/post`    |
| 7. Add headers (example: API key) | `curl -H "Authorization: Bearer <token>" https://api.example.com` |
| 8. Check response headers only    | `curl -I https://example.com`                                     |


✅ What is curl?

👉 curl is a command-line tool to transfer data to or from a server

👉 It supports many protocols: HTTP, HTTPS, FTP, SFTP, etc.


👉 Mostly used to:


Download files


Test APIs


Send GET/POST requests

✅ Basic Syntax


curl [options] <URL>


✅ Simple Examples


| **Action**                        | **Command**                                                       |
| --------------------------------- | ----------------------------------------------------------------- |
| 1. Download a webpage             | `curl https://example.com`                                        |
| 2. Save output to a file          | `curl -o myfile.html https://example.com`                         |
| 3. Follow redirects               | `curl -L https://example.com`                                     |
| 4. Download a file                | `curl -O https://example.com/file.zip`                            |
| 5. Send GET request (API)         | `curl https://api.example.com/data`                               |
| 6. Send POST request (API)        | `curl -X POST -d "param1=value1" https://api.example.com/post`    |
| 7. Add headers (example: API key) | `curl -H "Authorization: Bearer <token>" https://api.example.com` |
| 8. Check response headers only    | `curl -I https://example.com`                                     |

