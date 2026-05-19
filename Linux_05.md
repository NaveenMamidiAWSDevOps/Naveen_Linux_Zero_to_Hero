````md
# Linux Day 05

## 1. Copy Files and Preserve Permissions

### Command
```bash
cp -rp filename bkp_filename
```

### Explanation
- `cp` → Copy files or folders
- `-r` → Copy directories recursively
- `-p` → Preserve file permissions, ownership, and timestamps

### Interview Explanation
"I use the `cp -rp` command to create backup copies while preserving original permissions and timestamps. It is commonly used during configuration backups and migration activities."

---

## 2. Show Line Numbers in Vim

### Command
```vim
:set nu
```

### Explanation
Displays line numbers inside the Vim editor.

### Interview Explanation
"I use `:set nu` in Vim to enable line numbers, which helps during log analysis, script editing, and troubleshooting."

---

## 3. Compare Two Files

### Command
```bash
diff filename bkp_filename
```

### Explanation
Shows differences between two files line by line.

### Interview Explanation
"I use the `diff` command to compare configuration files, scripts, or backups to identify changes between versions."

---

## 4. Side-by-Side File Comparison

### Command
```bash
sdiff filename bkp_filename
```

### Explanation
Displays file differences side by side.

### Interview Explanation
"I use `sdiff` when I need a more readable side-by-side comparison between files during troubleshooting or validation."

---

## 5. Check Server Uptime

### Command
```bash
uptime
```

### Explanation
Shows:
- Current server time
- Server running duration
- Logged-in users
- Load average

### Interview Explanation
"I use the `uptime` command to check server availability, running duration, and system load during health monitoring."

---

## 6. Monitor System Performance

### Command
```bash
top
```

### Explanation
Displays:
- Running processes
- CPU usage
- Memory usage
- Process IDs

### Quit Command
```bash
q
```

or

```bash
Ctrl + C
```

### Interview Explanation
"I use the `top` command for real-time monitoring of CPU, memory, and running processes to identify performance bottlenecks."

---

## 7. Check CPU Information

### Command
```bash
lscpu
```

### Explanation
Displays CPU details such as:
- CPU architecture
- Number of cores
- Threads
- Processor model

### Interview Explanation
"I use `lscpu` to verify server hardware details like CPU cores and architecture during server validation and troubleshooting."

---

## 8. Check Memory Usage

### Commands
```bash
free
free -m
free -g
```

### Explanation
- `free` → Memory details
- `-m` → Shows memory in MB
- `-g` → Shows memory in GB

### Interview Explanation
"I use the `free` command to monitor RAM and swap memory utilization for performance analysis."

---

## 9. Remove Installed Package

### Command
```bash
yum remove packagename
```

### Example
```bash
yum remove git
```

### Explanation
Removes installed packages from the server.

### Interview Explanation
"I use `yum remove` to uninstall unnecessary or outdated packages from Linux servers."

---

## 10. Download Files from URL

### Command
```bash
wget <url_link>
```

### Example
```bash
wget https://example.com/file.zip
```

### Explanation
Downloads files directly from internet or repository links.

### Interview Explanation
"I use `wget` to download packages, scripts, and application files directly from repositories or URLs."

---

## 11. Create Zip File

### Command
```bash
zip -r name.zip <folder>
```

### Example
```bash
zip -r backup.zip project_folder
```

### Explanation
- `zip` → Compress files
- `-r` → Include subdirectories recursively

### Interview Explanation
"I use the `zip` command to compress application folders, logs, and backup files for storage or transfer."

---

## 12. Extract Zip File

### Command
```bash
unzip filename.zip
```

### Explanation
Extracts compressed zip files.

### Interview Explanation
"I use `unzip` to extract deployment packages, configuration backups, and shared project files."

---

## 13. Create Tar File

### Command
```bash
tar -cvf filename.tar <folder>
```

### Example
```bash
tar -cvf backup.tar myfolder
```

### Explanation
- `c` → Create archive
- `v` → Verbose output
- `f` → File name

### Interview Explanation
"I use the `tar -cvf` command to create archive backups of directories and application files."

---

## 14. Extract Tar File

### Command
```bash
tar -xvf filename.tar
```

### Explanation
- `x` → Extract archive
- `v` → Verbose mode
- `f` → File name

### Interview Explanation
"I use `tar -xvf` to extract archived files during deployments, migrations, and backup restoration."

---

## 15. Check Port Connectivity Using Telnet

### Command
```bash
telnet <hostname_or_ip> <port>
```

### Example
```bash
telnet google.com 80
```

### Explanation
Checks whether a server port is reachable or accessible.

### Install Telnet
```bash
yum install telnet -y
```

### Interview Explanation
"I use `telnet` for network troubleshooting to verify whether a specific server port is open and reachable from the system."

---

# Overall Interview Summary

"In Linux administration, I regularly use commands for system monitoring, file management, package handling, compression, and troubleshooting. Commands like `top`, `free`, and `lscpu` help in performance monitoring, while `diff`, `cp`, `tar`, and `zip` are useful for backup and file management. I also use networking tools like `telnet` to verify connectivity and port accessibility."
````
