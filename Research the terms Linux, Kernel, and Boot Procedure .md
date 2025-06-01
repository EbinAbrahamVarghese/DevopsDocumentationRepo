🐧 Linux Essentials Guide

Research the terms Linux, Kernel, and Boot Procedure

🧩 സോഫ്റ്റ്‌വെയറിന്റെ രണ്ട് തരം:

1️⃣ സിസ്റ്റം സോഫ്റ്റ്‌വെയർ (System Software)

ഇത് കമ്പ്യൂട്ടറിന്റെ പ്രവർത്തനം നിയന്ത്രിക്കുകയും, മറ്റു സോഫ്റ്റ്‌വെയറുകൾ പ്രവർത്തിക്കാൻ ആവശ്യമായ അടിസ്ഥാനസൗകര്യം ഒരുക്കുകയും ചെയ്യുന്നു

📌 ഉദാഹരണങ്ങൾ:

Ubuntu, Windows, macOS – ഇവല്ലാം ഓപ്പറേറ്റിംഗ് സിസ്റ്റങ്ങളാണ്.

Device Drivers, Boot Loader (bootmgr), BIOS/UEFI മുതലായവയും ഇതിലേക്കാണ് വരുന്നത്.

✅ പ്രധാന ഗുണങ്ങൾ:

ഹാർഡ്‌വെയറും സോഫ്റ്റ്‌വെയറും തമ്മിൽ ഇടപഴകാൻ സഹായിക്കുന്നു.

പ്രോഗ്രാമുകൾ പ്രവർത്തിക്കാൻ ആവശ്യമായ അടിസ്ഥാന സൗകര്യം നൽകുന്നു.

2️⃣ ആപ്ലിക്കേഷൻ സോഫ്റ്റ്‌വെയർ (Application Software)

ഉപയോക്താവ് നിർദ്ദിഷ്ടമായ ഒരു ജോലിയ്ക്കായി നേരിട്ട് ഉപയോഗിക്കുന്ന സോഫ്റ്റ്‌വെയറുകളാണ് ഇവ.

📌 ഉദാഹരണങ്ങൾ:

VS Code – പ്രോഗ്രാമിംഗ്/കോഡിംഗ് നടത്താൻ

Microsoft Word – ഡോക്യുമെന്റുകൾ ടൈപ്പ് ചെയ്യാൻ

Google Chrome – വെബ്ബ് ബ്രൗസിംഗിനായി

✅ പ്രധാന ഗുണങ്ങൾ:

ഉപയോക്താവിന്റെ പ്രത്യേക ആവശ്യങ്ങൾ നിറവേറ്റുന്നു (ഡോക്യുമെന്റേഷൻ, ബ്രൗസിംഗ്, എഡിറ്റിംഗ്, കോഡിംഗ് മുതലായവ).

സിസ്റ്റം സോഫ്റ്റ്‌വെയറിന്റെ മേൽ പ്രവർത്തിക്കുന്നു.


🧩 1. Open Source Software (ഓപ്പൺ സോഴ്സ് സോഫ്റ്റ്‌വെയർ)

📌 വിശദീകരണം:

കോഡ് പബ്ലിക് ആയി ലഭ്യമാണ്.

ആർക്കും കോഡ് നോക്കാനും മാറ്റങ്ങൾ വരുത്താനും അവകാശമുണ്ട്.

സ്വതന്ത്രമായും സൗജന്യമായും ഉപയോഗിക്കാം.

🛠️ ഗുണങ്ങൾ:

കമ്മ്യൂണിറ്റിയുടെ പിന്തുണയും സഹകരണവും.

auditing / സുരക്ഷ പരിശോധനകൾ anyone-ക്കും ചെയ്യാം.

പഠനത്തിനു അനുയോജ്യം.

🧪 ഉദാഹരണങ്ങൾ:

Linux

Mozilla Firefox

LibreOffice

GIMP

VLC Media Player

Android (AOSP)

🏢 2. Inner Source Software (ഇന്നർ സോഴ്സ് സോഫ്റ്റ്‌വെയർ)

📌 വിശദീകരണം:

Open Source പോലെയാണ്, പക്ഷേ ഒരു സ്ഥാപനത്തിനുള്ളിലേയ്ക്ക് മാത്രം പരിമിതപ്പെട്ടതാണ്.

കോഡ് പങ്കുവെക്കുന്നത് only internal teams-ക്കിടയിലാണ്.

കമ്പനി അകത്തെ പല ടീങ്ങൾ തമ്മിൽ same open-source principles പിന്തുടരുന്നു.

🛠️ ഗുണങ്ങൾ:

കോഡ് പുനർ ഉപയോഗം വർദ്ധിപ്പിക്കുന്നു.

സ്ഥാപനത്തിനുള്ളിലെ innovation പ്രോത്സാഹിപ്പിക്കുന്നു.

Collaboration മെച്ചപ്പെടുന്നു.

🧪 ഉദാഹരണങ്ങൾ:

Google, Amazon, Microsoft പോലുള്ള വലിയ കമ്പനികൾ "Inner Source" extensively ഉപയോഗിക്കുന്നു.

GitHub Enterprise, GitLab – Private repos

🔒 3. Closed Source Software (ക്ലോസ്ഡ് സോഴ്സ് സോഫ്റ്റ്‌വെയർ)

📌 വിശദീകരണം:

കോഡ് സർവ്വസാധാരണത്തിന് ലഭ്യമല്ല.

സോഫ്റ്റ്‌വെയർ ഉപയോഗിക്കാമെങ്കിലും, അതിന്റെ അന്തരംഗം കാണാൻ അനുവാദമില്ല.

സാധാരണയായി പണം നൽകിയാലേ ഉപയോഗിക്കാനാവൂ.

🛠️ ഗുണങ്ങൾ:

കൂടുതൽ നിയന്ത്രണവും കമർഷ്യൽ സൗകര്യവും.

അതിന്റെ നിർമ്മാതാവ് maintenance ഉറപ്പാക്കും.

🧪 ഉദാഹരണങ്ങൾ:

Microsoft Windows

Adobe Photoshop

macOS

MS Office Suite

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

1. കോഡെഴുതൽ

വിവരണം:

ഒരു പ്രോഗ്രാമർ JavaScript, Python, C പോലുള്ള ഒരു പ്രോഗ്രാമിംഗ് ഭാഷ ഉപയോഗിച്ച് ലജിക് എഴുതുന്നു. ഈ ലജിക് കമ്പ്യൂട്ടർ എങ്ങനെ പ്രവർത്തിക്കണമെന്നുള്ള നിർദ്ദേശങ്ങളാണ്.

📌 ഉദാഹരണം:

console.log("Hello World");

 2. കമ്പൈലേഷൻ (Compilation)
    
പരിഭാഷ: കമാൻഡുകൾ മെഷീൻ ഭാഷയിലേക്കുള്ള പരിഭാഷ

വിവരണം

കമ്പൈലർ എന്ന സോഫ്റ്റ്‌വെയർ പ്രോഗ്രാമിന്റെ മുഴുവൻ കോഡും വായിച്ച് അതിനെ ഒരേ സമയം മെഷീൻ ഭാഷയിലേക്കു (binary – 0, 1) മാറ്റുന്നു.

ഈ ഭാഗം വളരെ വേഗത്തിൽ പ്രവർത്തിക്കുന്നു, പക്ഷേ പ്രോഗ്രാമിൽ ചെറിയ പിശകുകൾ പോലും കമ്പൈലർ കാണിക്കും.

📌 കമ്പൈൽ ചെയ്യുന്ന ഭാഷകൾ: C, C++, Java (partial)

📌 ഉദാഹരണം:

    gcc program.c → program.exe

🌀 3. ഇന്റർപ്രിറ്റേഷൻ (Interpretation)

പരിഭാഷ: വരി വരിയായി കമാൻഡുകൾ വായിച്ച് പ്രവർത്തിപ്പിക്കൽ

വിവരണം:

ഇന്റർപ്രിറ്റർ ഓരോ കോഡ് വരിയും ഒന്നോടെ വായിച്ച് ഉടനെ അതിന്റെ ഫലങ്ങൾ പ്രവർത്തിപ്പിക്കുന്നു. ഈ രീതിയിൽ, കോഡ് എടുക്കുന്നത് എളുപ്പമാണ്, പക്ഷേ വേഗത കുറവാണ്.

📌 ഇന്റർപ്രിറ്റർ ഉപയോഗിക്കുന്ന ഭാഷകൾ: Python, JavaScript

📌 ഉദാഹരണം:

    python script.py

![Difference between compiler and interpreter](https://github.com/user-attachments/assets/d19f5cac-0cfa-44e3-8b37-f52777df3abf)



    

🧠 4. കർണൽ (Kernel)

പരിഭാഷ: ഓപ്പറേറ്റിംഗ് സിസ്റ്റത്തിന്റെ ഹൃദയം

വിവരണം:

കർണൽ കംപ്യൂട്ടറിലെ software-ൽ നിന്ന് hardware-ലേക്ക് നിയന്ത്രണം കൈമാറുന്ന പ്രധാന ഘടകമാണ്.

അതായത്, നമ്മുടെ കോഡ് RAM, CPU, HDD എന്നിവ ഉപയോഗിക്കണമെങ്കിൽ, കർണൽ മുഖേന അവയെ സമീപിക്കുന്നു.

📌 ജോലി:

Memory access

CPU scheduling

Input/output devices access


💻 5. ഓപ്പറേറ്റിംഗ് സിസ്റ്റം (Operating System - OS)

വിവരണം:

ഉപയോക്താവിനും കംപ്യൂട്ടറിനും ഇടയിൽ ഉള്ള വഴിയാണ് ഒഎസ്.

ഉദാ: Ubuntu, Windows, macOS

📌 ജോലി:

ഫയലുകൾ സേവ് ചെയ്യുക

നെറ്റ്‌വർക്ക് കൈകാര്യം ചെയ്യുക

പ്രോഗ്രാമുകൾ റൺ ചെയ്യാൻ സഹായിക്കുക
  

🔢 6. മെഷീൻ ഭാഷ (Machine Language)

വിവരണം:

എല്ലാ കമ്പൈൽ ചെയ്തും ഇന്റർപ്രിറ്റ് ചെയ്തും ഉള്ള കോഡുകൾ ഒടുവിൽ 0, 1 എന്നീ ബൈനറി കോഡുകളായി മാറും.

CPU ഈ ഭാഷ മാത്രമേ തിരിച്ചറിയുകയുള്ളൂ.

📌 ഉദാഹരണം:

MOV AX, 01 → 10110000 00000001

🧮 7. CPU (Central Processing Unit)

വിവരണം:

CPU അല്ലെങ്കിൽ പ്രോസസർ നമ്മുടെ കോഡ് റൺ ചെയ്യുന്നതിന് മുൻനിരയിലുള്ള ഘടകമാണ്.

ഇത് ബൈനറി ഇൻസ്ട്രക്ഷനുകൾ സ്വീകരിക്കുകയും അവ Fetch → Decode → Execute ചെയ്യുകയും ചെയ്യും.

📌 Output പിന്നീട്:

HDD-ലേക്ക് എഴുതും

Memory-ലേക്ക് പോക്കും

സ്‌ക്രീനിൽ കാണിക്കും

🧠 Kernel എന്താണ്?

Kernel എന്നത് Memory, CPU, Input/Output devices, Process management എന്നിവയെ നിയന്ത്രിക്കുന്ന പ്രധാന ഘടകമാണ്.
ഉപയോക്താവിന്റെ പ്രോഗ്രാമുകൾ ഈ ഘടകങ്ങൾ നേരിട്ട് സമീപിക്കാതെ Kernel മുഖേന മാത്രം പ്രവർത്തിക്കും.

1️⃣ Monolithic Kernel (മോണൊലിത്തിക് കർണൽ)

📌 വിവരണം:

Kernel-ലിന്റെ എല്ലാ ഘടകങ്ങളും (File system, Memory mgmt, Device drivers) ഒരു വലിയ യൂണിറ്റായാണ് പ്രവർത്തിക്കുന്നത്.

Performance വേഗത കൂടുതലാണ്, പക്ഷേ bug ഉണ്ടാകുമ്പോൾ മുഴുവൻ system crash ചെയ്യാം.

🧪 ഉദാഹരണം:

Linux Kernel

Unix

2️⃣ Microkernel (മൈക്രോകർണൽ)

📌 വിവരണം:

Kernel-ൽ അത്യാവശ്യ ഘടകങ്ങൾ മാത്രം ഉൾപ്പെടുത്തിയിരിക്കുന്നു (Scheduling, Memory).

File system, Drivers തുടങ്ങിയവയെ user-space-ൽ വേറെയായി സൂക്ഷിക്കുന്നു.

സുരക്ഷയും സ്ഥിരതയും കൂടുതലാണ്, പക്ഷേ performance കുറച്ച് 느slow.

🧪 ഉദാഹരണം:

QNX

Minix

HURD

3️⃣ Hybrid Kernel (ഹൈബ്രിഡ് കർണൽ)

📌 വിവരണം:

Monolithic + Microkernel തത്ത്വങ്ങൾ ചേർത്തതാണ്.

Core functionalities kernel-ൽ തന്നെയാണ്, ചില functionalities user-space-ൽ കൊണ്ടുവരുന്നു.

Performance & Stability തമ്മിൽ ഒരു ബാലൻസ്.

🧪 ഉദാഹരണം:

Windows NT Kernel (Windows 10/11)

XNU Kernel (macOS, iOS)

4️⃣ Nano Kernel (നാനോകർണൽ)


📌 വിവരണം:

അത്യന്തം ചെറിയ kernel ആണ്.

വളരെ താഴ്ന്ന ലെവലിൽ കുറച്ച് functionalities മാത്രം കൈകാര്യം ചെയ്യുന്നു (ഉദാ: Interrupts).

Kernel‌ ൽ ഇടപെടുന്ന functionalities വളരെ കുറവാണ്.

ഇത് പ്രധാനമായും basic hardware-level operations പോലുള്ള കാര്യങ്ങൾ മാത്രം കൈകാര്യം ചെയ്യുന്നു.

ഉദാഹരണങ്ങൾ:

Interrupt Handling

Context Switching

Basic Scheduling

Low-level I/O operations

🧪 ഉദാഹരണം: Minimal Embedded Systems

➤ Minimal Embedded Systems എന്താണ്?
ചുരുങ്ങിയ റിസോഴ്‌സുള്ള, task-specific systems.

Example: Microwave oven controllers, simple digital watches, basic IoT sensors.

ഇവയിൽ kernel‌ കൾ സാധാരണയായി super lightweight ആയിരിക്കും.

ചിലത് bare-metal programming (without OS) ഉപയോഗിച്ചേക്കാം, അല്ലെങ്കിൽ tiny real-time kernels പോലുള്ളവ ഉപയോഗിക്കും.
🖥️ Operating System Boot Process – Step by Step in Malayalam

✅ 1. Power ON → ROM പ്രവർത്തനം ആരംഭിക്കുന്നു

Computer power on ചെയ്ത ശേഷം, ROM (Read Only Memory) സിഗ്നൽ സ്വീകരിക്കുന്നു.

ROM-ലുള്ള BIOS (Basic Input Output System) പ്രവർത്തനം ആരംഭിക്കുന്നു.

✅ 2. BIOS പ്രക്രിയ – രണ്ട് പ്രധാന ഘടകങ്ങൾ

📌 a. POST (Power-On Self Test)

കമ്പ്യൂട്ടറിന്റെ ഹാർഡ്‌വെയർ ഘടകങ്ങൾ ശരിയാണോ എന്ന് പരിശോധിക്കുന്നു.

RAM

Keyboard

Disk

CPU

📌 b. BSL (Bootstrap Loader)

POST കഴിഞ്ഞ ശേഷം BSL പ്രവർത്തനം ആരംഭിക്കുന്നു.

Hard disk-ന്റെ primary sector-ലുള്ള MBR (Master Boot Record) ഈ ഘട്ടത്തിൽ ആക്സസ് ചെയ്യുന്നു.

✅ 3. MBR → Boot Loader

MBR (Master Boot Record) ഹാർഡ്ഡിസ്‌ക്കിന്റെ ആദ്യ 512 bytes-ൽ സ്ഥിതി ചെയ്യുന്നു.

അതിൽ ഉള്ളത്:

Boot Loader (ഉദാ: GRUB)

GRUB – GRand Unified Bootloader

Partition table

OS Loader pointer

📌 GRUB ബൂട്ട് ലോഡർ Linux OS, Windows OS, dual boot തുടങ്ങിയവയ്ക്ക് Support നൽകുന്നു.

✅ 4. GRUB → Kernel + initrd + init

GRUB Linux kernel, initrd (initial RAM disk), എന്നിവയുടെ സ്ഥാനം നോക്കി അവ memory-യിലേക്ക് ലോഡ് ചെയ്യും.

പിന്നീട്, init process (Linux-ന്റെ ആദ്യ പ്രക്രിയ) പ്രവർത്തനം ആരംഭിക്കുന്നു.

✅ 5. Init → Runlevel Selection

Init process പ്രവർത്തനമാരംഭിക്കുന്നത് /etc/inittab ഫയൽ അടിസ്ഥാനമാക്കിയാണ്.

ഇവിടെ runlevel നിർവചിച്ചിരിക്കുന്നു – ഏതൊരൊറ്റ mode-ൽ OS തുടങ്ങണം എന്ന്.

🧱 Linux Runlevels – 

മലയാളം വ്യാഖ്യാനവും കമാൻഡുകളും

Runlevel	Command	Purpose (ഉദ്ദേശ്യം)

| 🔢 **Runlevel** | 🖥️ **Command** | 📝 **Purpose (ഉദ്ദേശ്യം)**                                        |
| --------------- | --------------- | ----------------------------------------------------------------- |
| 0               | `init 0`        | Shutdown / Halt ചെയ്യുന്നു (കമ്പ്യൂട്ടർ ഓഫാക്കുന്നു)              |
| 1               | `init 1`        | Single user mode (root maintenance മാത്രം)                        |
| 2               | `init 2`        | Multi-user mode (നെറ്റ്വർക്ക് ഇല്ലാതെ)                            |
| 3               | `init 3`        | Multi-user mode + NFS (നെറ്റ്വർക്ക് പിന്തുണയോടെ)                  |
| 4               | `init 4`        | ഉപയോഗം ചെയ്യാത്തത് (ഡെവലപ്‌മെന്റിനായി കസ്റ്റമൈസ് ചെയ്യാവുന്നതാണ്) |
| 5               | `init 5`        | X11 Mode – Graphics Mode (GUI – Desktop)                          |
| 6               | `init 6`        | Reboot command – സിസ്റ്റം വീണ്ടും സ്റ്റാർട്ടാകും                  |




------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

🧠 Kernel എങ്ങനെ പ്രവർത്തിക്കുന്നു?

Kernel എന്നത് Linux Operating System-ന്റെ അധിഷ്ഠാന ഘടകമാണ്. ഇത്:

ഹാർഡ്വെയറിനും സോഫ്റ്റ്വെയറിനും ഇടയിൽ ഒരു പാലമായിട്ടാണ് പ്രവർത്തിക്കുന്നത്.

ഹാർഡ്വെയർ നിയന്ത്രണം, പ്രോസസ്സുകൾ, മെമ്മറി, ഫയൽ സിസ്റ്റം, നെറ്റ്വർക്ക് എന്നിവയെ നിയന്ത്രിക്കുന്നു.

🔁 Kernel പ്രവർത്തനം – ഘട്ടം ഘട്ടമായി

1. ✅ ബൂട്ടിംഗ് ഘട്ടം (Booting)
   
കമ്പ്യൂട്ടർ ഓൺ ചെയ്താൽ ആദ്യം BIOS/UEFI പ്രവർത്തിക്കും.

പിന്നീട് bootloader (ഉദാ: GRUB) kernel നെ memory-യിൽ ലോഡ് ചെയ്യും.

2. ⚙️ Kernel Initialization
   
Kernel സ്റ്റാർട്ടാകുമ്പോൾ ഹാർഡ്വെയർ initialize ചെയ്യും (CPU, RAM, Hard disk).

Device Drivers ഉപയോഗിച്ച് ഉപകരണങ്ങൾ തിരിച്ചറിയും.

Root filesystem (/) access ചെയ്യുന്നു.

പിന്നെ init process തുടങ്ങുന്നു (Linux-ൽ ആദ്യത്തെ process).

3. 👥 പ്രോസസ്സുകളുടെ നിയന്ത്രണം (Process Management)
   
ഓരോ ആപ്ലിക്കേഷനും ഒരു process ആകുന്നു.

Kernel process-കൾക്ക് CPU time വിഭജിക്കും, task switching നടത്തും.

4. 🧠 മെമ്മറി മാനേജ്മെന്റ് (Memory Management)
   
Kernel RAM എങ്ങനെ ഉപയോഗിക്കണം എന്ന് തീരുമാനിക്കുന്നു.

Virtual memory, swap memory എന്നിവ കൈകാര്യം ചെയ്യുന്നു.

5. 🔌 ഡിവൈസ് മാനേജ്മെന്റ് (Device Management)
   
Kernel device drivers ഉപയോഗിച്ച് USB, ഡിസ്‌ക് തുടങ്ങിയ ഹാർഡ്വെയറുമായി ആശയവിനിമയം നടത്തുന്നു.

7. 🧾 System Call Interface
   
ആപ്ലിക്കേഷനുകൾ kernel നെ നേരിട്ട് ആക്‌സസ് ചെയ്യില്ല.

അതിന്റെ പകരം system calls (ഉദാ: read(), write(), open()) ഉപയോഗിച്ച് kernel-നെ ആവശ്യപ്പെടുന്നു.

7. 📂 ഫയൽ സിസ്റ്റം നിയന്ത്രണം (File System Management)
   
ഫയലുകളും ഫോൾഡറുകളും kernel നിയന്ത്രിക്കുന്നു.

Permission, read/write, file system types എന്നിവയൊക്കെ kernel കൈകാര്യം ചെയ്യുന്നു.

8. 🌐 നെറ്റ്വർക്ക് മാനേജ്മെന്റ് (Networking)
   
Kernel IP routing, firewall rules, network devices എന്നിവയെ കൈകാര്യം ചെയ്യുന്നു.

🧭 ലളിതമായി പറയുകയാണെങ്കിൽ:
Kernel ഒരു ട്രാഫിക് പോലീസുപോലെയാണ്. ഹാർഡ്വെയറും സോഫ്റ്റ്വെയറും തമ്മിൽ കൃത്യതയോടെ പ്രവർത്തിക്കാൻ സഹായിക്കുന്നു.




Table Representation'
![Image1](https://github.com/user-attachments/assets/15c639b6-82d4-44a3-b3d2-19abfc08fbd9)

| Part               | Malayalam Explanation                                 |
| ------------------ | ----------------------------------------------------- |
| Booting            | Kernel memory-ലേക്ക് ലോഡാകുന്നു                       |
| Device Handling    | USB, HDD എന്നിവ ഡിറ്റക്റ്റ് ചെയ്യുന്നു                |
| Process Management | Application-കളെ process ആയി കൈകാര്യം ചെയ്യുന്നു       |
| Memory Management  | RAM ഉപയോഗം നിയന്ത്രിക്കുന്നു                          |
| File System        | ഫയൽ/ഫോൾഡർ access നടത്തുന്നു                           |
| System Calls       | App → Kernel Communication                            |
| Networking         | Internet access & network protocols handle ചെയ്യുന്നു |


