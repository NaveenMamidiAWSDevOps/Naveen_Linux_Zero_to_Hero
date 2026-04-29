# Linux Day 02

Today, I practiced basic Linux commands related to user management, hostname configuration, file and directory operations, navigation, and package installation.

## Commands Practiced with Examples

### 1. `whoami`
Displays the current logged-in user.

**Example:**
```bash
whoami
````

**Output:**

```bash
ec2-user
```

---

### 2. `hostnamectl set-hostname linuxserv`

Changes the system hostname.

**Example:**

```bash
sudo hostnamectl set-hostname linuxserv
```

**Check hostname:**

```bash
hostname
```

**Output:**

```bash
linuxserv
```

> Note: This command requires root or sudo privileges.

---

### 3. `sudo su -`

Switches from a normal user to the root user.

**Example:**

```bash
sudo su -
```

**Check current user:**

```bash
whoami
```

**Output:**

```bash
root
```

---

### 4. `history`

Displays previously executed commands.

**Example:**

```bash
history
```

**Output:**

```bash
1  whoami
2  pwd
3  ls
4  history
```

---

### 5. `hostname`

Displays the current system hostname.

**Example:**

```bash
hostname
```

**Output:**

```bash
linuxserv
```

---

### 6. `touch`

Creates empty files.

**Example:**

```bash
touch file1 file2
```

**Check files:**

```bash
ls
```

**Output:**

```bash
file1  file2
```

---

### 7. `mkdir`

Creates directories.

**Example:**

```bash
mkdir dir1 dir2
```

**Check directories:**

```bash
ls
```

**Output:**

```bash
dir1  dir2
```

---

### 8. `ls`

Lists files and directories in the current location.

**Example:**

```bash
ls
```

**Output:**

```bash
dir1  dir2  file1  file2
```

---

### 9. `ll`

Shows a detailed list of files and directories.

**Example:**

```bash
ll
```

**Output:**

```bash
drwxr-xr-x 2 root root 6 Apr 28 10:00 dir1
drwxr-xr-x 2 root root 6 Apr 28 10:00 dir2
-rw-r--r-- 1 root root 0 Apr 28 10:00 file1
-rw-r--r-- 1 root root 0 Apr 28 10:00 file2
```

---

### 10. `ls -la`

Lists all files, including hidden files, in long format.

**Example:**

```bash
ls -la
```

**Output:**

```bash
drwx------ 3 root root 100 Apr 28 10:00 .
drwxr-xr-x 3 root root  20 Apr 28 09:50 ..
-rw------- 1 root root 500 Apr 28 09:55 .bash_history
-rw-r--r-- 1 root root   0 Apr 28 10:00 file1
```

---

### 11. `ls -lrth`

Lists files in long format, sorted by time, with human-readable sizes.

**Example:**

```bash
ls -lrth
```

**Output:**

```bash
-rw-r--r-- 1 root root 0 Apr 28 10:00 file1
-rw-r--r-- 1 root root 0 Apr 28 10:01 file2
drwxr-xr-x 2 root root 6 Apr 28 10:02 dir1
```

---

### 12. `pwd`

Prints the current working directory.

**Example:**

```bash
pwd
```

**Output:**

```bash
/root
```

---

### 13. `cd`

Changes directory.

**Example:**

```bash
cd dir1
pwd
```

**Output:**

```bash
/root/dir1
```

---

### 14. `cd ..`

Moves one level back to the parent directory.

**Example:**

```bash
cd ..
pwd
```

**Output:**

```bash
/root
```

---

### 15. `cat`

Displays the content of a file.

**Example:**

```bash
cat file1
```

**Output:**

```bash
Hello Linux
```

> If the file is empty, no output will be shown.

---

### 16. `vim`

Opens a file in the Vim editor to view or edit content.

**Example:**

```bash
vim file1
```

**Inside Vim:**

* Press `i` to enter insert mode
* Type some text
* Press `Esc`
* Type `:wq`
* Press `Enter`

**Check file content:**

```bash
cat file1
```

**Output:**

```bash
Hello Linux
```

---

### 17. `yum install git`

Installs Git using the YUM package manager.

**Example:**

```bash
yum install git -y
```

**Check version:**

```bash
git --version
```

**Output:**

```bash
git version 2.40.1
```

---

### 18. `git --version`

Displays the installed Git version.

**Example:**

```bash
git --version
```

**Output:**

```bash
git version 2.40.1
```

---

### 19. `yum install java -y`

Installs Java without asking for confirmation.

**Example:**

```bash
yum install java -y
```

**Check version:**

```bash
java --version
```

**Output:**

```bash
openjdk 17.0.10 2024-01-16
OpenJDK Runtime Environment
OpenJDK 64-Bit Server VM
```

---

### 20. `java --version`

Displays the installed Java version.

**Example:**

```bash
java --version
```

**Output:**

```bash
openjdk 17.0.10 2024-01-16
```

---

## Key Learnings

* Changing the hostname requires root or sudo privileges
* `cd` works only with directories, not files
* `ls -la` is useful for viewing hidden files
* `ls -lrth` helps display files in a detailed and time-sorted format
* `yum` is used as a package manager to install software
* `history` is useful for reviewing previously executed commands

## Conclusion

Day 02 helped me strengthen my understanding of basic Linux commands and system operations. I practiced working with users, files, directories, navigation, and package installation, which are essential skills for daily Linux administration.

````

## One important correction
For `cat file1`, your file will only show output like `Hello Linux` **if you added content first** using `vim file1` or `echo`.

Example:
```bash
echo "Hello Linux" > file1
cat file1
````

If you want, I can now make this into a **clean professional GitHub README final version** with better formatting and no extra explanation outside the file.



