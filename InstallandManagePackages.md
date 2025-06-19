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





