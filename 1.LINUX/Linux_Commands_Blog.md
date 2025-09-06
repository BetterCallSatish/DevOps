# 🐧 Ultimate Linux Commands Cheatsheet (100 Commands)

Welcome to the **Ultimate Linux Commands Blog** 🎉.
This guide covers the **Top 100 Linux commands** you’ll need, with:

* 🖥️ Examples
* 📖 Explanations
* 💡 Pro tips
* 🎨 Fun emojis for easy memorization

---

## 📂 File & Directory Management

### 1. `pwd` – Print Working Directory 💾

```bash
$ pwd
/home/satish
```

📖 **Explanation:**
Tells you your **current location** in the filesystem. Like a GPS 📍 for Linux.

💡 **Pro Tip:**
When lost in nested directories, run `pwd` to find your way back.

---

### 2. `ls` – List Files & Directories 📂

```bash
$ ls
Documents  Downloads  Music  Pictures
```

📖 **Explanation:**
Lists all files/folders. Similar to **File Explorer (Windows) 🪟** or **Finder (Mac) 🍏**.

✨ **Options:**

* `ls -l` → Show details (permissions 🔑, size 📏, date 🕒)
* `ls -a` → Show hidden files 👻

---

### 3. `cd` – Change Directory 🚪

```bash
$ cd Documents
$ pwd
/home/satish/Documents
```

📖 **Explanation:**
Moves you between directories.

💡 **Pro Tip:**

* `cd ..` → Go one step back ⬅️
* `cd ~` → Jump to home 🏠

---

### 4. `mkdir` – Make Directory 🏗️

```bash
$ mkdir blog
$ ls
blog  Documents  Downloads
```

📖 **Explanation:**
Creates a folder.

💡 **Pro Tip:** Use `mkdir -p a/b/c` to create nested directories in one go.

---

### 5. `rmdir` – Remove Empty Directory 🗑️

```bash
$ rmdir blog
```

📖 **Explanation:**
Deletes empty directories. Use `rm -r` for non-empty ones.

---

### 6. `touch` – Create Empty File 📝

```bash
$ touch notes.txt
$ ls
notes.txt
```

📖 **Explanation:**
Creates an empty file or updates its timestamp.

💡 Handy for quickly making config files!

---

### 7. `cat` – View File Contents 📖

```bash
$ cat notes.txt
Linux is powerful!
```

📖 **Explanation:**
Displays file contents.

💡 Combine with `| more` or `| less` for big files.

---

### 8. `less` – Scroll Through Files ⬇️⬆️

```bash
$ less notes.txt
```

📖 **Explanation:**
Lets you scroll page by page. Press `q` to quit.

---

### 9. `head` – First Few Lines ⬆️

```bash
$ head -n 5 notes.txt
Line1
Line2
Line3
Line4
Line5
```

📖 **Explanation:**
Shows top lines. Default = 10.

---

### 10. `tail` – Last Few Lines ⬇️

```bash
$ tail -n 3 notes.txt
Line8
Line9
Line10
```

📖 **Explanation:**
Shows bottom lines. Default = 10.

💡 `tail -f log.txt` = Live log monitoring 🔥

---

## 📝 File Editing & Processing

### 11. `nano` – Simple Editor ✏️

```bash
$ nano notes.txt
```

📖 **Explanation:**
Beginner-friendly terminal text editor.

---

### 12. `vim` – Power Editor ⚡

```bash
$ vim notes.txt
```

📖 **Explanation:**
Advanced editor with modes. Takes practice but extremely powerful.

---

### 13. `file` – Detect File Type 🔍

```bash
$ file notes.txt
notes.txt: ASCII text
```

📖 **Explanation:**
Tells whether a file is text, binary, executable, etc.

---

### 14. `wc` – Word Count 📊

```bash
$ wc notes.txt
  10   20   120 notes.txt
```

📖 **Explanation:**
Counts lines, words, characters.

---

### 15. `sort` – Sort Text 🔠

```bash
$ sort names.txt
Alice
Bob
Charlie
```

📖 **Explanation:**
Sorts file contents alphabetically.

---

### 16. `uniq` – Remove Duplicates 🚫

```bash
$ uniq names.txt
Alice
Bob
Charlie
```

📖 **Explanation:**
Removes repeated lines (often combined with `sort`).

---

### 17. `cut` – Extract Columns ✂️

```bash
$ cut -d":" -f1 /etc/passwd
root
daemon
satish
```

📖 **Explanation:**
Cuts text by delimiter. Useful for CSV/log parsing.

---

### 18. `grep` – Search in Files 🔎

```bash
$ grep "Linux" notes.txt
Linux is powerful!
```

📖 **Explanation:**
Finds matching patterns.

💡 Use `grep -i` for case-insensitive search.

---

### 19. `grep -r` – Recursive Search 🔥

```bash
$ grep -r "main" /home/satish/projects/
```

📖 **Explanation:**
Searches inside all files of a directory.

---

### 20. `diff` – Compare Files ⚖️

```bash
$ diff file1.txt file2.txt
```

📖 **Explanation:**
Shows line-by-line differences.

💡 Great for config or code changes.

---

## 👤 User & Permission Management

### 21. `whoami` – Current User 👤

```bash
$ whoami
satish
```

📖 **Explanation:**
Displays logged-in username.

---

### 22. `id` – User Identity Badge 🆔

```bash
$ id
uid=1000(satish) gid=1000(satish) groups=1000(satish),27(sudo)
```

📖 **Explanation:**
Shows UID, GID, and groups.

---

### 23. `adduser` – Add New User ➕

```bash
$ sudo adduser john
```

📖 **Explanation:**
Creates a new user with home directory.

---

### 24. `passwd` – Change Password 🔑

```bash
$ passwd john
```

📖 **Explanation:**
Sets or updates a user’s password.

---

### 25. `su` – Switch User 🔄

```bash
$ su john
```

📖 **Explanation:**
Switches to another user account.

---

### 26. `sudo` – Run as Admin 👑

```bash
$ sudo apt update
```

📖 **Explanation:**
Executes command with root privileges.

💡 Don’t abuse this power 😉.

---

### 27. `groups` – Show Groups 👥

```bash
$ groups satish
satish sudo
```

📖 **Explanation:**
Lists groups a user belongs to.

---

### 28. `chmod` – Change File Permissions 🔐

```bash
$ chmod 755 script.sh
```

📖 **Explanation:**
Sets read/write/execute permissions.

---

### 29. `chown` – Change Ownership 🏷️

```bash
$ sudo chown satish:users notes.txt
```

📖 **Explanation:**
Changes file owner and group.

---

### 30. `umask` – Default Permissions 🎭

```bash
$ umask
0022
```

📖 **Explanation:**
Controls default file permissions.

## ⚡ Process Management

### 31. `ps` – Show Processes 🧾

```bash
$ ps
  PID TTY          TIME CMD
 1234 pts/0    00:00:00 bash
 1240 pts/0    00:00:00 ps
```

📖 **Explanation:**
Lists processes for the current shell.

💡 Use `ps aux` for all processes with details.

---

### 32. `top` – Real-time Process Monitor 📊

```bash
$ top
```

📖 **Explanation:**
Live view of CPU, memory, and running processes.

💡 Press `q` to quit, `k` to kill process.

---

### 33. `htop` – Fancy Process Viewer 🎨

```bash
$ htop
```

📖 **Explanation:**
Better version of `top` with colors and navigation.

---

### 34. `jobs` – Background Jobs ⚙️

```bash
$ jobs
[1]+  Running   ping google.com &
```

📖 **Explanation:**
Shows background tasks in current shell.

---

### 35. `fg` – Bring Job to Foreground ⬆️

```bash
$ fg %1
```

📖 **Explanation:**
Brings a background job into the foreground.

---

### 36. `bg` – Resume Job in Background ⬇️

```bash
$ bg %1
```

📖 **Explanation:**
Resumes a paused job in background.

---

### 37. `kill` – Kill Process 💀

```bash
$ kill 1234
```

📖 **Explanation:**
Terminates a process by PID.

---

### 38. `killall` – Kill by Name ❌

```bash
$ killall firefox
```

📖 **Explanation:**
Kills all processes with a given name.

---

### 39. `pkill` – Pattern-based Kill 🎯

```bash
$ pkill -u satish
```

📖 **Explanation:**
Kills processes by user or pattern.

---

### 40. `uptime` – System Uptime ⏱️

```bash
$ uptime
12:34:56 up 5 days,  2:11,  2 users,  load average: 0.23, 0.12, 0.09
```

📖 **Explanation:**
Shows system uptime and load averages.

---

## 🌐 Networking

### 41. `ping` – Test Connectivity 🌍

```bash
$ ping google.com
64 bytes from 142.250.190.14: icmp_seq=1 ttl=117 time=15 ms
```

📖 **Explanation:**
Tests if a host is reachable.

---

### 42. `curl` – Fetch URLs 🌐

```bash
$ curl https://example.com
```

📖 **Explanation:**
Transfers data from/to URLs. Supports HTTP, FTP, APIs.

---

### 43. `wget` – Download Files ⬇️

```bash
$ wget https://example.com/file.zip
```

📖 **Explanation:**
Downloads files from the web.

---

### 44. `ifconfig` – Network Config (Legacy) 📡

```bash
$ ifconfig
eth0: inet 192.168.1.5
```

📖 **Explanation:**
Displays network interfaces (deprecated, use `ip`).

---

### 45. `ip a` – Modern Network Info 🌐

```bash
$ ip a
```

📖 **Explanation:**
Shows IP addresses and interfaces.

---

### 46. `netstat` – Network Statistics 📊

```bash
$ netstat -tuln
```

📖 **Explanation:**
Lists open ports and connections.

---

### 47. `ss` – Socket Stats 🔗

```bash
$ ss -tuln
```

📖 **Explanation:**
Modern replacement for `netstat`.

---

### 48. `traceroute` – Trace Route 🗺️

```bash
$ traceroute google.com
```

📖 **Explanation:**
Shows the path packets take to a host.

---

### 49. `nslookup` – DNS Lookup 📡

```bash
$ nslookup google.com
```

📖 **Explanation:**
Resolves domain names to IP addresses.

---

### 50. `dig` – DNS Query Expert 🔍

```bash
$ dig google.com
```

📖 **Explanation:**
Detailed DNS query results.

---

## 📦 File Compression & Archiving

### 51. `tar` – Archive Files 📦

```bash
$ tar -cvf archive.tar file1 file2
```

📖 **Explanation:**
Creates/extracts archives.

💡 `-xvf` to extract.

---

### 52. `gzip` – Compress File 🗜️

```bash
$ gzip notes.txt
```

📖 **Explanation:**
Compresses file (replaces original).

---

### 53. `gunzip` – Decompress File 📂

```bash
$ gunzip notes.txt.gz
```

📖 **Explanation:**
Decompresses `.gz` files.

---

### 54. `zip` – Create Zip Archive 📦

```bash
$ zip archive.zip file1 file2
```

📖 **Explanation:**
Compresses multiple files into `.zip`.

---

### 55. `unzip` – Extract Zip Archive 📂

```bash
$ unzip archive.zip
```

📖 **Explanation:**
Extracts `.zip` files.

---

### 56. `bzip2` – High Compression 🗜️

```bash
$ bzip2 file.txt
```

📖 **Explanation:**
Compresses with better ratio than gzip.

---

### 57. `bunzip2` – Decompress bzip2 📂

```bash
$ bunzip2 file.txt.bz2
```

📖 **Explanation:**
Decompresses `.bz2` files.

---

### 58. `xz` – Extreme Compression ⚡

```bash
$ xz file.txt
```

📖 **Explanation:**
Compresses files with `.xz`.

---

### 59. `unxz` – Decompress xz 📂

```bash
$ unxz file.txt.xz
```

📖 **Explanation:**
Decompresses `.xz` files.

---

### 60. `tar -xzvf` – Extract tar.gz 🎁

```bash
$ tar -xzvf archive.tar.gz
```

📖 **Explanation:**
Extracts `.tar.gz` compressed archives.

---

## 📊 Disk Management

### 61. `df` – Disk Free Space 💽

```bash
$ df -h
Filesystem   Size  Used  Avail  Use%  Mounted on
/dev/sda1    100G   60G   35G   65%   /
```

📖 **Explanation:**
Shows disk space usage. `-h` = human-readable.

---

### 62. `du` – Disk Usage 📏

```bash
$ du -sh Documents
1.5G Documents
```

📖 **Explanation:**
Displays folder size.

---

### 63. `lsblk` – List Block Devices 💿

```bash
$ lsblk
sda   100G
 ├─sda1  50G /
 └─sda2  50G /home
```

📖 **Explanation:**
Shows disks and partitions.

---

### 64. `mount` – Mount Device 🔗

```bash
$ sudo mount /dev/sdb1 /mnt
```

📖 **Explanation:**
Attaches a device/partition to filesystem.

---

### 65. `umount` – Unmount Device ❌

```bash
$ sudo umount /mnt
```

📖 **Explanation:**
Detaches mounted filesystem.

---

### 66. `blkid` – Block Device IDs 🆔

```bash
$ blkid
/dev/sda1: UUID="1234-5678" TYPE="ext4"
```

📖 **Explanation:**
Shows UUID and type of block devices.

---

### 67. `fdisk` – Disk Partitioning 🪓

```bash
$ sudo fdisk -l
```

📖 **Explanation:**
Lists and edits disk partitions.

---

### 68. `parted` – Partition Manager ⚙️

```bash
$ sudo parted /dev/sda
```

📖 **Explanation:**
Advanced disk partitioning tool.

---

### 69. `mkfs` – Create Filesystem 🏗️

```bash
$ sudo mkfs.ext4 /dev/sdb1
```

📖 **Explanation:**
Formats a partition with a filesystem.

---

### 70. `fsck` – Check Filesystem 🩺

```bash
$ sudo fsck /dev/sda1
```

📖 **Explanation:**
Repairs filesystem errors.

---

## 🔒 System Monitoring & Security

### 71. `uptime` – System Uptime ⏱️

(covered earlier, repeated for context)

---

### 72. `who` – Logged-in Users 👥

```bash
$ who
satish  tty7   Sep  7 09:32
```

📖 **Explanation:**
Lists users currently logged in.

---

### 73. `w` – Who + Activity 🧑‍💻

```bash
$ w
 09:33:11 up 1 day,  2:21,  2 users,  load average: 0.01, 0.05, 0.10
```

📖 **Explanation:**
Shows users + what they’re doing.

---

### 74. `last` – Login History 📜

```bash
$ last
satish tty7   :0    Sat Sep  7 09:32   still logged in
```

📖 **Explanation:**
Displays recent login history.

---

### 75. `whoami` – Current User Badge 🪪

(covered earlier)

---

### 76. `hostname` – Show Hostname 🖥️

```bash
$ hostname
ubuntu-pc
```

📖 **Explanation:**
Displays computer name.

---

### 77. `uname -a` – System Info ℹ️

```bash
$ uname -a
Linux ubuntu 5.15.0-46-generic x86_64 GNU/Linux
```

📖 **Explanation:**
Kernel + architecture + system details.

---

### 78. `dmesg` – Kernel Logs 📜

```bash
$ dmesg | tail
```

📖 **Explanation:**
Shows hardware/kernel boot messages.

---

### 79. `journalctl` – Systemd Logs 📰

```bash
$ journalctl -xe
```

📖 **Explanation:**
Displays logs from `systemd`.

---

### 80. `free` – Memory Usage 💾

```bash
$ free -h
              total        used        free
Mem:           16G         6G        10G
```

📖 **Explanation:**
Shows RAM usage.

---

## ⚙️ Performance & Hardware

### 81. `vmstat` – Virtual Memory Stats 📈

```bash
$ vmstat
```

📖 **Explanation:**
CPU, memory, and IO stats.

---

### 82. `iostat` – I/O Stats 💿

```bash
$ iostat
```

📖 **Explanation:**
CPU and disk IO usage.

---

### 83. `uptime` – Load Average ⏳

(already covered)

---

### 84. `sar` – System Activity Report 📊

```bash
$ sar 1 3
```

📖 **Explanation:**
Reports CPU/memory/network usage over time.

---

### 85. `lsusb` – USB Devices 🔌

```bash
$ lsusb
Bus 002 Device 003: ID 046d:c534 Logitech USB Receiver
```

📖 **Explanation:**
Lists connected USB devices.

---

### 86. `lspci` – PCI Devices 🎮

```bash
$ lspci
00:1f.3 Audio device: Intel Corporation Device a0c8
```

📖 **Explanation:**
Lists PCI hardware (GPU, sound, etc).

---

### 87. `neofetch` – Fancy System Info 🎨

```bash
$ neofetch
```

📖 **Explanation:**
Cool system summary with ASCII art.

---

### 88. `screenfetch` – Alternative Sys Info 📟

```bash
$ screenfetch
```

📖 **Explanation:**
Similar to `neofetch`, shows OS, kernel, DE.

---

### 89. `uptime -p` – Pretty Uptime 🕒

```bash
$ uptime -p
up 5 hours, 33 minutes
```

📖 **Explanation:**
Human-readable uptime.

---

### 90. `uptime -s` – Since Boot ⏲️

```bash
$ uptime -s
2025-09-02 10:33:00
```

📖 **Explanation:**
Shows exact boot time.

---

## 📦 Package Management

### 91. `apt update` – Refresh Repo 📡

```bash
$ sudo apt update
```

📖 **Explanation:**
Updates package index on Debian/Ubuntu.

---

### 92. `apt upgrade` – Upgrade Packages ⬆️

```bash
$ sudo apt upgrade
```

📖 **Explanation:**
Upgrades installed packages.

---

### 93. `apt install` – Install Package 📥

```bash
$ sudo apt install git
```

📖 **Explanation:**
Installs software.

---

### 94. `apt remove` – Remove Package 🗑️

```bash
$ sudo apt remove git
```

📖 **Explanation:**
Uninstalls software.

---

### 95. `yum install` – RHEL Install 📦

```bash
$ sudo yum install httpd
```

📖 **Explanation:**
Installs packages on RHEL/CentOS.

---

### 96. `dnf install` – Fedora Install 📦

```bash
$ sudo dnf install nginx
```

📖 **Explanation:**
Fedora’s package manager.

---

### 97. `pacman -S` – Arch Install 🏹

```bash
$ sudo pacman -S vim
```

📖 **Explanation:**
Installs software on Arch Linux.

---

### 98. `snap install` – Snap Packages 📦

```bash
$ sudo snap install code --classic
```

📖 **Explanation:**
Installs Snap apps.

---

### 99. `flatpak install` – Flatpak Apps 📦

```bash
$ flatpak install flathub org.gimp.GIMP
```

📖 **Explanation:**
Installs Flatpak apps.

---

### 100. `man` – Manual Pages 📚

```bash
$ man ls
```

📖 **Explanation:**
Shows detailed documentation for any command.

💡 The **man pages** are your best friend!

---

# 🎉 Conclusion

You just learned **100 Linux commands** 🐧 — with examples, explanations, and pro tips.


👉 Do you want me to now make this **as a polished `.md` file** (with all fancy emojis + formatting) so you can directly upload to GitHub?
