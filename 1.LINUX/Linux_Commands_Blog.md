# 🐧 Top 100 Linux Commands with Examples & Explanations

Linux is a powerful operating system, and mastering its commands helps you work faster and smarter.
Here are the **Top 100 Linux Commands** with **examples, outputs, and explanations**.

---

## 📂 File & Directory Management

### 1. `pwd` – Print Working Directory

```bash
$ pwd
/home/satish
```

**Explanation:** Shows the full path of your current directory.

---

### 2. `ls` – List Files & Directories

```bash
$ ls
Documents  Downloads  Music  Pictures
```

**Explanation:** Lists files and folders in the current directory.

---

### 3. `ls -l` – Long Listing

```bash
$ ls -l
-rw-r--r--  1 satish users  1024 Sep  7  notes.txt
drwxr-xr-x  2 satish users  4096 Sep  6  projects
```

**Explanation:** Shows permissions, ownership, file size, and modification date.

---

### 4. `ls -a` – Show Hidden Files

```bash
$ ls -a
.  ..  .bashrc  Documents  Downloads
```

**Explanation:** Displays hidden files (those starting with `.`).

---

### 5. `cd` – Change Directory

```bash
$ cd Documents
$ pwd
/home/satish/Documents
```

**Explanation:** Moves you into another directory. Use `cd ..` to go back one level.

---

### 6. `mkdir` – Make Directory

```bash
$ mkdir blog
$ ls
blog  Documents  Downloads
```

**Explanation:** Creates a new directory. Use `mkdir -p a/b/c` to create nested directories.

---

### 7. `rmdir` – Remove Empty Directory

```bash
$ rmdir blog
```

**Explanation:** Deletes an empty directory.

---

### 8. `touch` – Create File

```bash
$ touch notes.txt
$ ls
notes.txt
```

**Explanation:** Creates an empty file or updates the timestamp of an existing one.

---

### 9. `cat` – View File Contents

```bash
$ cat notes.txt
Linux is powerful!
```

**Explanation:** Prints file contents directly to the terminal.

---

### 10. `less` – View File Page by Page

```bash
$ less notes.txt
Linux is powerful!
Linux is everywhere!
```

**Explanation:** Allows scrolling through large files one page at a time.

---

### 11. `more` – View File (Old Pager)

```bash
$ more notes.txt
Linux is powerful!
```

**Explanation:** Similar to `less` but with fewer navigation options.

---

### 12. `head` – View Beginning of File

```bash
$ head -n 5 notes.txt
Line1
Line2
Line3
Line4
Line5
```

**Explanation:** Displays the first N lines of a file. Default is 10.

---

### 13. `tail` – View End of File

```bash
$ tail -n 3 notes.txt
Line8
Line9
Line10
```

**Explanation:** Displays the last N lines of a file. Default is 10.

---

### 14. `tail -f` – Live Log Monitoring

```bash
$ tail -f /var/log/syslog
Sep 7 00:15 systemd[1]: Starting Service...
```

**Explanation:** Continuously displays new lines added to a log file.

---

### 15. `cp` – Copy File

```bash
$ cp notes.txt backup.txt
```

**Explanation:** Copies files or directories. Use `cp -r dir1 dir2` for directories.

---

### 16. `mv` – Move/Rename File

```bash
$ mv notes.txt docs.txt
```

**Explanation:** Moves or renames files and directories.

---

### 17. `rm` – Remove File

```bash
$ rm notes.txt
```

**Explanation:** Deletes files. Use `rm -r dir` to remove directories recursively.

---

### 18. `find` – Search for Files

```bash
$ find . -name "notes.txt"
./notes.txt
```

**Explanation:** Searches for files and directories.

---

### 19. `locate` – Quick File Search

```bash
$ locate notes.txt
/home/satish/notes.txt
```

**Explanation:** Searches using a database. Requires `updatedb`.

---

### 20. `tree` – Show Directory Tree

```bash
$ tree
.
├── Documents
│   └── notes.txt
└── Downloads
```

**Explanation:** Displays a folder structure visually.

---

## 📑 File Viewing & Editing

### 21. `nano` – Simple Text Editor

```bash
$ nano notes.txt
```

**Explanation:** Opens a lightweight text editor in the terminal.

---

### 22. `vi` / `vim` – Advanced Editor

```bash
$ vi notes.txt
```

**Explanation:** Opens files in Vim editor. Powerful but requires practice.

---

### 23. `gedit` – GUI Text Editor

```bash
$ gedit notes.txt
```

**Explanation:** Opens files in a graphical text editor (if installed).

---

### 24. `file` – Show File Type

```bash
$ file notes.txt
notes.txt: ASCII text
```

**Explanation:** Displays the file type (text, binary, executable, etc.).

---

### 25. `wc` – Word Count

```bash
$ wc notes.txt
  10   20   120 notes.txt
```

**Explanation:** Shows line, word, and character count.

---

### 26. `sort` – Sort File Content

```bash
$ sort names.txt
Alice
Bob
Charlie
```

**Explanation:** Sorts lines in a file alphabetically.

---

### 27. `uniq` – Remove Duplicates

```bash
$ uniq names.txt
Alice
Bob
Charlie
```

**Explanation:** Filters duplicate lines (best used with `sort`).

---

### 28. `cut` – Extract Columns

```bash
$ cut -d":" -f1 /etc/passwd
root
daemon
satish
```

**Explanation:** Extracts parts of lines using a delimiter.

---

### 29. `grep` – Search Inside Files

```bash
$ grep "Linux" notes.txt
Linux is powerful!
```

**Explanation:** Finds lines containing a pattern.

---

### 30. `grep -r` – Recursive Search

```bash
$ grep -r "main" /home/satish/projects/
```

**Explanation:** Searches inside all files in a directory.

---

## 📦 File Compression & Archiving

### 31. `tar -cvf` – Create Archive

```bash
$ tar -cvf archive.tar Documents/
```

**Explanation:** Creates an archive file.

---

### 32. `tar -xvf` – Extract Archive

```bash
$ tar -xvf archive.tar
```

**Explanation:** Extracts files from an archive.

---

### 33. `gzip` – Compress File

```bash
$ gzip notes.txt
```

**Explanation:** Compresses a single file.

---

### 34. `gunzip` – Decompress File

```bash
$ gunzip notes.txt.gz
```

**Explanation:** Decompresses a `.gz` file.

---

### 35. `zip` – Create Zip File

```bash
$ zip archive.zip notes.txt
```

**Explanation:** Compresses files into `.zip`.

---

### 36. `unzip` – Extract Zip File

```bash
$ unzip archive.zip
```

**Explanation:** Extracts `.zip` files.

---

## 👥 User Management

### 37. `whoami` – Show Current User

```bash
$ whoami
satish
```

**Explanation:** Prints the username of the current session.

---

### 38. `id` – Show UID and GID

```bash
$ id
uid=1000(satish) gid=1000(satish) groups=1000(satish),27(sudo)
```

**Explanation:** Displays user ID, group ID, and groups.

---

### 39. `who` – Show Logged-In Users

```bash
$ who
satish   tty7   2025-09-07  00:10 (:0)
```

**Explanation:** Shows all logged-in users.

---

### 40. `w` – Show User Activity

```bash
$ w
 00:10:00 up  2:00,  2 users,  load average: 0.08, 0.15, 0.10
USER     TTY   FROM   LOGIN@   IDLE   JCPU   PCPU WHAT
satish   tty7  :0     00:00    2:00   0.00s  0.01s gnome-shell
```

**Explanation:** Displays who is logged in and their activity.

---

### 41. `users` – Show Usernames

```bash
$ users
satish guest
```

**Explanation:** Lists currently logged-in usernames.

---

### 42. `adduser` – Add New User

```bash
$ sudo adduser john
```

**Explanation:** Creates a new user account.

---

### 43. `passwd` – Change Password

```bash
$ passwd
Changing password for satish.
```

**Explanation:** Updates user password.

---

### 44. `su` – Switch User

```bash
$ su john
Password:
```

**Explanation:** Switches to another user account.

---

### 45. `sudo` – Run as Superuser

```bash
$ sudo apt update
```

**Explanation:** Executes commands with root privileges.

---

### 46. `groups` – Show Groups

```bash
$ groups
satish sudo users
```

**Explanation:** Shows groups the user belongs to.

---

## 🔒 Permissions & Ownership

### 47. `chmod` – Change Permissions

```bash
$ chmod 755 script.sh
```

**Explanation:** Changes file permissions.

---

### 48. `chown` – Change Owner

```bash
$ sudo chown john:john notes.txt
```

**Explanation:** Changes file ownership.

---

### 49. `chgrp` – Change Group

```bash
$ sudo chgrp developers notes.txt
```

**Explanation:** Changes group ownership.

---

### 50. `umask` – Default Permissions

```bash
$ umask
0022
```

**Explanation:** Shows or sets default file permissions.

---

## ⚙️ Process Management

### 51. `ps` – Show Processes

```bash
$ ps
  PID TTY          TIME CMD
 2550 pts/0    00:00:00 bash
 2670 pts/0    00:00:00 ps
```

**Explanation:** Lists running processes.

---

### 52. `ps aux` – All Processes

```bash
$ ps aux | grep bash
satish   2550  0.0  0.1  10000  2000 ? S   00:00   0:00 bash
```

**Explanation:** Displays all processes with details.

---

### 53. `top` – Real-Time Process Monitor

```bash
$ top
top - 00:15:23 up 1:10,  2 users,  load average: 0.10, 0.15, 0.05
```

**Explanation:** Interactive process monitoring.

---

### 54. `htop` – Advanced Process Viewer

```bash
$ htop
```

**Explanation:** Colorful, interactive process manager (if installed).

---

### 55. `kill` – Kill Process by PID

```bash
$ kill 1234
```

**Explanation:** Terminates a process.

---

### 56. `killall` – Kill by Name

```bash
$ killall firefox
```

**Explanation:** Kills all processes with a specific name.

---

### 57. `jobs` – Show Background Jobs

```bash
$ jobs
[1]+  Running  ping google.com &
```

**Explanation:** Lists jobs started in the background.

---

### 58. `fg` – Foreground Job

```bash
$ fg %1
```

**Explanation:** Brings a background job to the foreground.

---

### 59. `bg` – Resume Job in Background

```bash
$ bg %1
```

**Explanation:** Resumes a stopped job in the background.

---

## 💽 Disk Management

### 60. `df -h` – Show Disk Usage

```bash
$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda1        50G   20G   28G  42% /
```

**Explanation:** Displays disk space in human-readable format.

---

### 61. `du -sh` – Folder Size

```bash
$ du -sh Downloads
1.2G    Downloads
```

**Explanation:** Shows the size of a directory.

---

### 62. `mount` – Mount Device

```bash
$ sudo mount /dev/sdb1 /mnt
```

**Explanation:** Mounts a device or partition.

---

### 63. `umount` – Unmount Device

```bash
$ sudo umount /mnt
```

**Explanation:** Safely unmounts a device.

---

### 64. `lsblk` – Block Devices

```bash
$ lsblk
sda   8:0   0  50G  0 disk
└─sda1 8:1  0  50G  0 part /
```

**Explanation:** Lists all storage devices and partitions.

---

### 65. `fdisk -l` – Partition Table

```bash
$ sudo fdisk -l
```

**Explanation:** Shows disk partitions.

---

### 66. `blkid` – Show UUID

```bash
$ sudo blkid
/dev/sda1: UUID="1234-5678" TYPE="ext4"
```

**Explanation:** Displays UUID and type of partitions.

---

## 🌐 Networking

### 67. `ping` – Test Connectivity

```bash
$ ping google.com
64 bytes from 142.250.183.238: icmp_seq=1 ttl=116 time=35.6 ms
```

**Explanation:** Sends ICMP packets to test network.

---

### 68. `ifconfig` – Show Interfaces

```bash
$ ifconfig
```

**Explanation:** Displays network interfaces (deprecated, use `ip`).

---

### 69. `ip a` – Show IP Address

```bash
$ ip a
2: eth0: inet 192.168.1.10/24
```

**Explanation:** Shows network interface details.

---

### 70. `curl` – Fetch Web Content

```bash
$ curl https://example.com
<!doctype html>
<html>
<head><title>Example Domain</title></head>
```

**Explanation:** Transfers data from or to a server.

---

### 71. `wget` – Download File

```bash
$ wget https://example.com/file.zip
```

**Explanation:** Downloads files from the web.

---

### 72. `scp` – Secure Copy

```bash
$ scp file.txt user@192.168.1.10:/home/user/
```

**Explanation:** Copies files between systems over SSH.

---

### 73. `ssh` – Connect to Remote Server

```bash
$ ssh user@192.168.1.10
```

**Explanation:** Connects securely to another machine.

---

### 74. `netstat -tulnp` – Show Ports

```bash
$ netstat -tulnp
```

**Explanation:** Shows active network connections.

---

### 75. `ss -tulnp` – Modern Netstat

```bash
$ ss -tulnp
```

**Explanation:** Displays open ports and connections.

---

### 76. `traceroute` – Trace Route

```bash
$ traceroute google.com
```

**Explanation:** Shows path packets take to a destination.

---

### 77. `dig` – DNS Lookup

```bash
$ dig google.com
```

**Explanation:** Queries DNS servers.

---

### 78. `nslookup` – DNS Query

```bash
$ nslookup google.com
```

**Explanation:** Looks up DNS records.

---

### 79. `arp` – Show ARP Table

```bash
$ arp -a
```

**Explanation:** Displays IP-to-MAC address mappings.

---

### 80. `ftp` – File Transfer Protocol

```bash
$ ftp 192.168.1.10
```

**Explanation:** Connects to an FTP server.

---

## 🖥️ System Information

### 81. `uname -a` – Kernel Info

```bash
$ uname -a
Linux satish 5.15.0-72-generic #79-Ubuntu SMP x86_64 GNU/Linux
```

**Explanation:** Shows system and kernel details.

---

### 82. `hostname` – Show Hostname

```bash
$ hostname
satish-PC
```

**Explanation:** Prints system hostname.

---

### 83. `uptime` – Show Uptime

```bash
$ uptime
 00:15:00 up  2:10,  2 users,  load average: 0.10, 0.12, 0.08
```

**Explanation:** Shows how long the system has been running.

---

### 84. `dmesg` – Kernel Logs

```bash
$ dmesg | tail
```

**Explanation:** Displays kernel boot messages.

---

### 85. `free -h` – Show Memory Usage

```bash
$ free -h
              total        used        free      shared  buff/cache   available
Mem:           8.0G        3.2G        2.5G        300M        2.3G        4.4G
```

**Explanation:** Displays RAM usage.

---

### 86. `vmstat` – Performance Stats

```bash
$ vmstat 1 5
```


**Explanation:** Shows CPU, memory, and I/O stats.

---

### 87. `iostat` – I/O Stats

```bash
$ iostat
```

**Explanation:** Displays CPU and disk I/O stats.

---

### 88. `lsusb` – USB Devices

```bash
$ lsusb
Bus 002 Device 003: ID 046d:c534 Logitech USB Receiver
```

**Explanation:** Lists connected USB devices.

---

### 89. `lspci` – PCI Devices

```bash
$ lspci
00:1f.3 Audio device: Intel Corporation Device a0c8
```

**Explanation:** Lists PCI devices like sound, network, and graphics cards.

---

### 90. `neofetch` – Fancy System Info

```bash
$ neofetch
```

**Explanation:** Displays system info with ASCII art (if installed).

---

## ⚡ Package Management

### 91. `apt update` – Update Package List (Debian/Ubuntu)

```bash
$ sudo apt update
```

**Explanation:** Refreshes package index.

---

### 92. `apt upgrade` – Upgrade Packages

```bash
$ sudo apt upgrade
```

**Explanation:** Installs available package updates.

---

### 93. `apt install` – Install Package

```bash
$ sudo apt install git
```

**Explanation:** Installs software.

---

### 94. `apt remove` – Remove Package

```bash
$ sudo apt remove git
```

**Explanation:** Removes installed software.

---

### 95. `yum install` – Install (RHEL/CentOS)

```bash
$ sudo yum install httpd
```

**Explanation:** Installs packages on RHEL/CentOS.

---

### 96. `dnf install` – Install (Fedora)

```bash
$ sudo dnf install nginx
```

**Explanation:** Installs software using `dnf`.

---

### 97. `pacman -S` – Install (Arch Linux)

```bash
$ sudo pacman -S vim
```

**Explanation:** Installs software on Arch Linux.

---

### 98. `snap install` – Install Snap Package

```bash
$ sudo snap install code --classic
```

**Explanation:** Installs Snap applications.

---

### 99. `flatpak install` – Install Flatpak

```bash
$ flatpak install flathub org.gimp.GIMP
```

**Explanation:** Installs apps via Flatpak.

---

### 100. `man` – Manual Pages

```bash
$ man ls
```

**Explanation:** Shows detailed documentation for any command.
