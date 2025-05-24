Understanding the Linux File System Hierarchy
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

![linux-file-system-hierarchy-1](https://github.com/user-attachments/assets/d400582d-e407-48d5-918c-4bb86efd0243)


🔁 Root Directory (/)

ഇത് ഫയൽ സിസ്റ്റത്തിലെ പ്രധാന ഡയറക്ടറിയാണ്. എല്ലാ മറ്റു ഡയറക്ടറികളും ഇതിന്റെ കീഴിലായാണ് ഉള്ളത്. എല്ലാ ഫയലുകളും, ഫോൾഡറുകളും ഇതിൽ നിന്നാണ് തുടങ്ങുന്നത്


അതിന്റെ കീഴിലേയ്ക്ക് മറ്റു എല്ലാ ഡയറക്ടറികളും പന്തലിച്ചിരിക്കുന്നു.

🛠️ /bin – Basic Commands (Binary Executables)

സിസ്റ്റം ബൂട്ട് ചെയ്യുമ്പോഴും പ്രവർത്തിക്കേണ്ട 

അത്യാവശ്യ കമാൻഡുകൾ.

ഉദാ: ls, mkdir, cp, mv, cat, echo.

എല്ലായ്പ്പോഴും ലഭ്യമാകേണ്ടതാണ്.

🧠 /boot – Boot Files

Linux operating system ബൂട്ട് ചെയ്യാൻ kernel, bootloader, initrd തുടങ്ങിയവ ഇതിലുണ്ട്.

ഉദാ: vmlinuz, grub.cfg, initrd.img.

🧩 /dev – Devices

Linux-ന്റെ എല്ലാം ഫയലുകളായി കാണിക്കുന്ന സവിശേഷതയാൽ, ഹാർഡ്‌വെയറുമായി ബന്ധപ്പെട്ട വിവരങ്ങൾ /dev, /proc, /sys പോലുള്ള ഡയറക്ടറികളിൽ നിന്നും ഫയൽ രൂപത്തിൽ ലഭ്യമാണ്.

ഉദാ:

/dev/sda – HDD/SSD

/dev/tty – terminal

/dev/null, /dev/zero – virtual devices

⚙️ /etc – System Configuration

സിസ്റ്റത്തിന്റെ സെറ്റിംഗുകൾ, config ഫയലുകൾ.

ഉദാ:

/etc/passwd – യൂസർ വിവരങ്ങൾ

/etc/fstab – mount info

/etc/hostname, /etc/network/interfaces

👤 /home – User Directories

ഓരോ യൂസർക്കും സ്വന്തം വീടുപോലുള്ള ഫോൾഡർ.

ഉദാ: /home/ebin, /home/leena

📚 /lib & /lib64 – Libraries

Binary commands-നെ suppport ചെയ്യുന്ന shared libraries.

64-bit syste-കൾക്ക് പ്രത്യേകമായ /lib64.

💿 /media – Removable Devices

USB, CD/DVD പോലെ plug ചെയ്യുന്ന ഉപകരണങ്ങൾ mount ചെയ്യാൻ.

ഉദാ: /media/usb, /media/cdrom

🔧 /mnt – Manual Mount Point

adminമാർ അടിയന്തരമായി ഏതെങ്കിലും drive കൈകാര്യം ചെയ്യാൻ.

📦 /opt – Optional Software

manually install ചെയ്യുന്ന third-party software packages.

ഉദാ: Skype, Google Chrome

📋 /proc – Kernel and Process Info

Running kernel process-ുകളുടെ വിവരങ്ങൾ

pseudo-filesystem ആണ് – ഫയലുകൾ ഒറിജിനൽ ആകുന്നില്ല.

ഉദാ:

/proc/cpuinfo, /proc/meminfo – processor & memory info

/proc/[PID] – individual process info

👑 /root – Root User’s Home

സിസ്റ്റം അഡ്മിനിന്റെ (root user) സ്വകാര്യ ഹോം ഫോൾഡർ.

/home/root അല്ല; അതിനെതിരെ /root ആണ്.

🕒 /run – Runtime Data

ബൂട്ട് ചെയ്ത ശേഷം മാത്രം സൃഷ്ടിക്കുന്ന താൽക്കാലിക ഫയലുകൾ.

ഉദാ: process IDs, system state info.

🛠️ /sbin – System Binaries

System-level admin commands.

ഉദാ: shutdown, reboot, fdisk, ifconfig.

🖥️ /srv – Service Data

system services (web server, ftp server മുതലായവ) ഉപയോഗിക്കുന്ന ഡാറ്റ.

ഉദാ: /srv/www, /srv/ftp

📂 /tmp – Temporary Files

താൽക്കാലികമായി ഉപയോഗിക്കുന്ന ഫയലുകൾ.

പലസമയവും reboot കഴിഞ്ഞാൽ ഇത് ശൂന്യമാകും.

👥 /usr – User System Resources

Program files, libraries, documentation

ഉപയോക്താക്കളെ ലക്ഷ്യമിട്ടാണ്:

/usr/bin – user commands


/usr/lib – libraries

/usr/share – shared data

/usr/local – locally compiled software

📈 /var – Variable Files

നേരത്തെ കണ്ടിരുന്നതുപോലെ /etc config-ിനായി, എന്നാൽ /var frequently changing files-ക്കായി.

ഉദാ:

/var/log – log files

/var/mail – mail spool

/var/spool – printer queues
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Classifcation of directory

🗂 1. System Directories

These are essential for the system to boot and operate properly.

| Directory | Purpose                              |
| --------- | ------------------------------------ |
| `/`       | Root of the filesystem               |
| `/boot`   | Boot loader and kernel files         |
| `/sbin`   | System binaries for admin tasks      |
| `/lib`    | Shared libraries for system programs |
| `/lib64`  | 64-bit libraries                     |


👤 2. User Directories

Used to store user data and personal settings.

| Directory    | Purpose                                             |
| ------------ | --------------------------------------------------- |
| `/home`      | User home folders (e.g., `/home/john`)              |
| `/root`      | Home directory of the root (admin) user             |
| `/usr`       | Secondary hierarchy for user applications and tools |
| `/usr/local` | Locally compiled or installed software              |


⚙️ 3. Configuration Directories

Stores system-wide configuration files.


| Directory | Purpose                                                 |
| --------- | ------------------------------------------------------- |
| `/etc`    | Configuration files (e.g., networking, users, services) |

🔧 4. Device & Process Directories

Represents devices and running system information.

| Directory | Purpose                                          |
| --------- | ------------------------------------------------ |
| `/dev`    | Device files (e.g., disks, USB, terminal)        |
| `/proc`   | Virtual filesystem with process and system info  |
| `/sys`    | System information related to devices and kernel |


📁 5. Temporary & Runtime Directories

Used for temporary or runtime-generated data.

| Directory | Purpose                                        |
| --------- | ---------------------------------------------- |
| `/tmp`    | Temporary files; deleted after reboot          |
| `/run`    | Runtime data like process IDs                  |
| `/var`    | Variable files: logs, cache, spool, lock files |


💽 6. Mount Point Directories

Used to mount external and additional filesystems.

| Directory | Purpose                                    |
| --------- | ------------------------------------------ |
| `/mnt`    | Temporary mount point for sysadmin use     |
| `/media`  | Auto-mounted removable media (USB, CD-ROM) |



📦 7. Optional & Service-Specific Directories

| Directory | Purpose                                   |
| --------- | ----------------------------------------- |
| `/opt`    | Optional third-party software packages    |
| `/srv`    | Data for system services (e.g., web, FTP) |


---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Linux ഫയൽ സിസ്റ്റങ്ങൾ (Linux File Systems) എന്നത് ഡാറ്റ ഡിസ്‌കിൽ എങ്ങനെ സംഭരിക്കണം, സംഘടിപ്പിക്കണം, ആക്സസ് ചെയ്യണം തുടങ്ങിയ രീതികൾ നിശ്ചയിക്കുന്ന രീതിയാണ്. Linux-ൽ പല തരത്തിലുള്ള ഫയൽ സിസ്റ്റങ്ങൾ ഉണ്ട്, അവയിൽ ചിലത് വളരെ പ്രസിദ്ധമായവയാണ്: ext, ext2, ext3, ext4, Btrfs, XFS, ZFS തുടങ്ങിയവ.

ഇനിപ്പറയുന്നത് പ്രധാനമായ Linux File System Types ആണ്:


🔹 1. ext (Extended File System)

ആദ്യമായിട്ടുള്ള Linux-നെ ആശ്രയിച്ച ഫയൽ സിസ്റ്റം.

1992-ൽ പുറത്തിറങ്ങി.

ഇപ്പോൾ ഉപയോഗിക്കാറില്ല.

🔹 2. ext2 (Second Extended Filesystem)

Journaling ഇല്ല.

Still used in USB drives and memory cards (വളരെ ലളിതമായതിനാൽ).

Max File Size: 2TB

🔹 3. ext3 (Third Extended Filesystem)

ext2-യുടെ മെച്ചപ്പെടുത്തിയ പതിപ്പ്.

Journaling Support ഉണ്ട് → Crash-നു ശേഷം recovery എളുപ്പം.

ext2-ൽ നിന്ന് ext3-ലേക്ക് convert ചെയ്യാൻ കഴിയുന്നു.

🔹 4. ext4 (Fourth Extended Filesystem)

✅ ഏറ്റവും കൂടുതൽ ഉപയോഗിക്കുന്നത്.

Journaling + Performance boost

Max File Size: 16TB

Max Volume Size: 1EB (Exabyte)

Delayed allocation, extents support, faster fsck

🔹 5. XFS

High-performance journaling file system.

Mainly used in Red Hat, CentOS.

Very good for large files & enterprise-level use.

Used in servers and NAS systems.

🔹 6. Btrfs (B-tree File System)

Advanced Linux file system with snapshotting, compression, and RAID support.

Designed as a replacement for ext4.

Suitable for modern storage needs.

🔹 7. ZFS

Originally from Sun Microsystems (used in Solaris).

Supports snapshotting, deduplication, volume management.

Not built into the Linux kernel by default (needs external modules).

🔹 8. F2FS (Flash-Friendly File System)

Designed by Samsung for NAND flash storage (e.g., SSDs).

Very efficient for mobile and embedded devices.


✅ Summary Table


| File System | Journaling | Max File Size   | Use Case                |
| ----------- | ---------- | --------------- | ----------------------- |
| ext2        | ❌          | 2 TB            | Simple, small devices   |
| ext3        | ✅          | 2 TB            | Basic journaling        |
| ext4        | ✅          | 16 TB           | Default modern Linux FS |
| XFS         | ✅          | 8 EB            | Servers, large data     |
| Btrfs       | ✅          | 16 EB           | Advanced features       |
| ZFS         | ✅          | 16 EB+          | Enterprise systems      |
| F2FS        | ✅          | Device-specific | Flash drives, mobile    |


