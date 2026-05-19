
# Linux Day 05 - Commands with Real-Time Interview Scenarios

This document contains important Linux commands used for file backup, comparison, system monitoring, package management, compression, and network troubleshooting.

---

## 1. `cp -rp` - Copy Files with Permissions

### Command
```bash
cp -rp filename bkp_filename
````

### Real-Time Scenario

Before modifying a configuration file, I take a backup using `cp -rp`.

### Example

```bash
cp -rp httpd.conf httpd.conf_bkp
```

### Interview Answer

"In real-time, before changing any important configuration file, I take a backup using `cp -rp`. The `-p` option preserves permissions and timestamps, which is useful during rollback."

---

## 2. `:set nu` - Show Line Numbers in Vim

### Command

```vim
:set nu
```

### Real-Time Scenario

When editing scripts or configuration files, line numbers help me quickly identify errors.

### Interview Answer

"I use `:set nu` in Vim to enable line numbers. It helps when troubleshooting errors that mention a specific line number."

---

## 3. `diff` - Compare Two Files

### Command

```bash
diff filename bkp_filename
```

### Real-Time Scenario

After making changes to a file, I compare it with the backup file.

### Example

```bash
diff httpd.conf httpd.conf_bkp
```

### Interview Answer

"I use `diff` to compare two files and identify exact changes, especially before and after configuration updates."

---

## 4. `sdiff` - Side-by-Side File Comparison

### Command

```bash
sdiff filename bkp_filename
```

### Real-Time Scenario

When I want a side-by-side view of two files, I use `sdiff`.

### Interview Answer

"`sdiff` is useful when comparing large configuration files because it shows both files side by side."

---

## 5. `uptime` - Check Server Uptime

### Command

```bash
uptime
```

### Real-Time Scenario

When troubleshooting a server, I first check how long the server has been running.

### Interview Answer

"I use `uptime` to check server availability and load average. It helps me understand whether the server recently rebooted or is under heavy load."

---

## 6. `top` - Monitor Running Processes

### Command

```bash
top
```

### Exit

```bash
q
```

### Real-Time Scenario

If an application is slow, I use `top` to check CPU and memory usage.

### Interview Answer

"I use `top` for real-time process monitoring. It helps me identify high CPU or high memory consuming processes."

---

## 7. `lscpu` - Check CPU Information

### Command

```bash
lscpu
```

### Real-Time Scenario

Before installing or troubleshooting software, I check CPU details.

### Interview Answer

"`lscpu` gives CPU architecture, cores, sockets, and thread information. I use it during server validation."

---

## 8. `free` - Check Memory Usage

### Commands

```bash
free
free -m
free -g
```

### Real-Time Scenario

When a server is slow, I check memory usage using `free -m` or `free -g`.

### Interview Answer

"I use `free` to check RAM and swap memory. `free -m` shows memory in MB and `free -g` shows memory in GB."

---

## 9. `yum remove` - Remove Package

### Command

```bash
yum remove packagename
```

### Example

```bash
yum remove telnet
```

### Real-Time Scenario

When a package is no longer required, I remove it using `yum remove`.

### Interview Answer

"I use `yum remove` to uninstall unwanted packages from RHEL, CentOS, or Amazon Linux servers."

---

## 10. `wget` - Download Files

### Command

```bash
wget <url_link>
```

### Example

```bash
wget https://example.com/app.zip
```

### Real-Time Scenario

During application deployment, I use `wget` to download files directly on the server.

### Interview Answer

"`wget` is used to download files from URLs. In real-time, I use it to download packages, scripts, and deployment files."

---

## 11. `zip` - Compress Folder

### Command

```bash
zip -r name.zip foldername
```

### Example

```bash
zip -r logs_backup.zip /var/log
```

### Real-Time Scenario

Before sharing logs with another team, I compress them using zip.

### Interview Answer

"I use `zip -r` to compress folders recursively, especially for log backups and file transfers."

---

## 12. `unzip` - Extract Zip File

### Command

```bash
unzip filename.zip
```

### Example

```bash
unzip app.zip
```

### Real-Time Scenario

After downloading application files, I extract them using `unzip`.

### Interview Answer

"I use `unzip` to extract compressed application packages or backup files."

---

## 13. `tar -cvf` - Create Tar Archive

### Command

```bash
tar -cvf filename.tar foldername
```

### Example

```bash
tar -cvf app_backup.tar /opt/application
```

### Real-Time Scenario

Before migration or deployment, I create a tar archive of important folders.

### Interview Answer

"`tar -cvf` is used to create archive files. I use it for backups before deployments or migrations."

---

## 14. `tar -xvf` - Extract Tar Archive

### Command

```bash
tar -xvf filename.tar
```

### Example

```bash
tar -xvf app_backup.tar
```

### Real-Time Scenario

During restoration or deployment, I extract tar files using `tar -xvf`.

### Interview Answer

"`tar -xvf` extracts tar archive files. I use it when restoring backups or extracting deployment packages."

---

## 15. `telnet` - Check Port Connectivity

### Install Telnet

```bash
yum install telnet -y
```

### Command

```bash
telnet <hostname_or_ip> <port>
```

### Example

```bash
telnet 10.0.1.25 8080
```

### Real-Time Scenario

If an application cannot connect to another server, I check the port using telnet.

### Interview Answer

"I use `telnet` to verify whether a specific port is reachable. For example, if an application server cannot connect to a database server, I test the DB port using telnet."

---

# Real-Time Troubleshooting Example

## Scenario: Application is running slow

### Steps I Follow

```bash
uptime
top
free -m
lscpu
```

### Explanation

First, I check the server uptime and load average using `uptime`. Then I use `top` to identify high CPU or memory processes. After that, I check memory usage with `free -m` and CPU details using `lscpu`.

### Interview Answer

"If an application is slow, I first check the server health using `uptime`, `top`, and `free -m`. These commands help me identify whether the issue is related to CPU, memory, or system load."

---

# Final Interview Summary

"As part of Linux administration, I use commands like `cp -rp`, `diff`, `sdiff`, `top`, `uptime`, `free`, `lscpu`, `yum`, `wget`, `zip`, `tar`, and `telnet` in real-time scenarios. These commands help me with backups, file comparison, system monitoring, package management, file compression, and network troubleshooting."

```
```
