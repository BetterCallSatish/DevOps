# 🐧 Top 100 Linux Commands with Examples & Explanations

Linux is one of the most powerful operating systems, and mastering its commands is essential for developers, sysadmins, and power users.  
This blog covers the **Top 100 Linux Commands** with **examples, outputs, and explanations**.  

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

(...content continues until command 100...)  

# 🎉 Conclusion  


