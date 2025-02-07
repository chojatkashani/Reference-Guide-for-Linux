# Reference-Guide-for-Linux


---

## **Table of Contents**  
1. [Navigate the File System](#navigate-the-file-system)  
2. [Read Files](#read-files)  
3. [Manage the File System](#manage-the-file-system)  
4. [Filter Content](#filter-content)  
5. [Manage Users and Their Permissions](#manage-users-and-their-permissions)  
6. [Get Help in Linux](#get-help-in-linux)  

---

## **Navigate the File System**  

The following Linux commands help navigate the file system.  

### **cd** *(Change Directory)*  
| Command | Description |
|---------|------------|
| `cd reports` | Navigates to the **reports** subdirectory. |
| `cd /home/analyst/reports` | Navigates to the reports directory (full path needed if not a subdirectory). |
| `cd ..` | Moves **one level up** in the directory tree. |  

### **ls** *(List Files & Directories)*  
| Command | Description |
|---------|------------|
| `ls` | Lists **files & directories** in the current directory. |
| `ls /home/analyst/reports` | Lists **contents of the reports directory**. |
| `ls -a` | Lists **all files, including hidden files**. |
| `ls -l` | Lists **detailed file info (permissions, owner, size, timestamp)**. |
| `ls -la` | Combines **hidden files (-a) and details (-l)**. |  

### **pwd** *(Print Working Directory)*  
| Command | Description |
|---------|------------|
| `pwd` | Displays the **full path of the current directory**. |  

### **whoami** *(Current User Information)*  
| Command | Description |
|---------|------------|
| `whoami` | Returns **current user’s username**. |  

---

## **Read Files**  

### **cat** *(Display File Contents)*  
| Command | Description |
|---------|------------|
| `cat updates.txt` | Displays **contents of updates.txt**. |  

### **head** *(Show Beginning of a File)*  
| Command | Description |
|---------|------------|
| `head updates.txt` | Displays **first 10 lines** of the file. |
| `head -n 5 updates.txt` | Displays **first 5 lines**. |  

### **less** *(View File One Page at a Time)*  
| Command | Description |
|---------|------------|
| `less updates.txt` | Allows **scrolling** through file content. |  

### **tail** *(Show End of a File)*  
| Command | Description |
|---------|------------|
| `tail updates.txt` | Displays **last 10 lines**. |
| `tail -n 5 updates.txt` | Displays **last 5 lines**. |  

---

## **Manage the File System**  

### **cp** *(Copy Files & Directories)*  
| Command | Description |
|---------|------------|
| `cp permissions.txt /home/analyst/logs` | Copies file to a **new location**. |  

### **mkdir** *(Create Directory)*  
| Command | Description |
|---------|------------|
| `mkdir network` | Creates a **new directory** named `network`. |  

### **mv** *(Move or Rename Files)*  
| Command | Description |
|---------|------------|
| `mv permissions.txt /home/analyst/logs` | Moves file to **new location**. |
| `mv permissions.txt perm.txt` | Renames `permissions.txt` to `perm.txt`. |  

### **nano** *(Edit Files)*  
| Command | Description |
|---------|------------|
| `nano permissions.txt` | Opens `permissions.txt` in the **Nano text editor**. |  

### **rm** *(Delete Files & Directories)*  
| Command | Description |
|---------|------------|
| `rm permissions.txt` | Deletes the file. |
| `rmdir network` | Deletes an **empty directory**. |  

### **touch** *(Create an Empty File)*  
| Command | Description |
|---------|------------|
| `touch permissions.txt` | Creates a **new file**. |  

---

## **Filter Content**  

### **find** *(Search for Files & Directories)*  
| Command | Description |
|---------|------------|
| `find /home/analyst/projects -name "*log*"` | Finds files with "log" in their name. |  
| `find /home/analyst/projects -mtime -3` | Finds files **modified in the last 3 days**. |  

### **grep** *(Search for Specific Content in Files)*  
| Command | Description |
|---------|------------|
| `grep OS updates.txt` | Searches for the word **"OS"** in `updates.txt`. |  

### **Piping (|)** *(Chain Commands Together)*  
| Command | Description |
|---------|------------|
| `ls /home/analyst/reports | grep users` | Filters results for files containing "users". |  

---

## **Manage Users and Their Permissions**  

### **chmod** *(Change File Permissions)*  
| Command | Description |
|---------|------------|
| `chmod u+rwx,g+rwx,o+rwx login_sessions.txt` | Grants **read, write, and execute** permissions. |  

### **chown** *(Change File Owner/Group)*  
| Command | Description |
|---------|------------|
| `sudo chown fgarcia access.txt` | Changes **file owner to `fgarcia`**. |  
| `sudo chown :security access.txt` | Changes **group ownership to `security`**. |  

### **groupdel** *(Delete a User Group)*  
| Command | Description |
|---------|------------|
| `sudo groupdel accounting` | Deletes **accounting group**. |  

### **useradd** *(Add a New User)*  
| Command | Description |
|---------|------------|
| `sudo useradd fgarcia` | Adds a new user **fgarcia**. |  
| `sudo useradd -g security fgarcia` | Adds `fgarcia` with **primary group security**. |  

### **userdel** *(Delete a User Account)*  
| Command | Description |
|---------|------------|
| `sudo userdel -r fgarcia` | Deletes user `fgarcia` **and their home directory**. |  

### **usermod** *(Modify Existing Users)*  
| Command | Description |
|---------|------------|
| `sudo usermod -a -G marketing fgarcia` | Adds `fgarcia` to **marketing group**. |  
| `sudo usermod -L fgarcia` | **Locks** the user account. |  

---

## **Get Help in Linux**  

### **apropos** *(Find Commands Related to a Keyword)*  
| Command | Description |
|---------|------------|
| `apropos password` | Searches for commands related to **password management**. |  

### **man** *(Display Command Manual Pages)*  
| Command | Description |
|---------|------------|
| `man chown` | Shows **manual page for `chown`**. |  

### **whatis** *(Show a Brief Command Description)*  
| Command | Description |
|---------|------------|
| `whatis nano` | Displays a **one-line description** of the `nano` command. |  

---

## **Summary**  

This **Linux reference guide** provides essential **commands** for:  
✅ **Navigating the file system**  
✅ **Managing files & directories**  
✅ **Filtering content**  
✅ **Handling user permissions**  
✅ **Getting help in Linux**  

Use this guide as a **quick reference** to perform essential **system administration tasks** efficiently. 🚀  
