
# Linux File System - Interview Notes

## Interview Answer

Linux follows a hierarchical file system structure that starts from the root directory `/`. Unlike Windows, Linux does not use drive letters like `C:` or `D:`. Everything in Linux is organized under `/`, including files, directories, devices, processes, and mounted file systems.

As a Linux administrator or DevOps engineer, I commonly work with directories like `/etc` for configuration files, `/var/log` for logs, `/home` for user data, `/opt` for third-party applications, `/boot` for boot-related files, and `/tmp` for temporary files.

Linux also represents many system resources as files. For example, hardware devices are represented under `/dev`, process information is available under `/proc`, and kernel or hardware-related information is exposed under `/sys`.

---

## Linux Directory Structure and Purpose

| Directory | Purpose |
|---|---|
| `/` | Root directory. It is the starting point of the entire Linux file system. |
| `/bin` | Contains essential user commands like `ls`, `cp`, `mv`, `cat`, and `mkdir`. In modern Linux systems, it may be a symbolic link to `/usr/bin`. |
| `/sbin` | Contains essential system administration commands like `reboot`, `fdisk`, `ip`, and `shutdown`. It may be linked to `/usr/sbin`. |
| `/boot` | Contains boot-related files such as the Linux kernel, initramfs, and GRUB bootloader files. |
| `/dev` | Contains device files. Examples include hard disks, terminals, USB devices, and other hardware devices. |
| `/etc` | Contains system and application configuration files. Examples include `/etc/passwd`, `/etc/fstab`, `/etc/ssh/sshd_config`, and `/etc/hostname`. |
| `/home` | Contains home directories for normal users. Example: `/home/naveen`. |
| `/root` | Home directory of the root user. It is different from `/`, which is the root of the entire file system. |
| `/lib` | Contains shared library files required by essential commands and system programs. It may be linked to `/usr/lib`. |
| `/lib64` | Contains 64-bit shared libraries. It may be linked to `/usr/lib64`. |
| `/usr` | Contains user-level binaries, libraries, documentation, and applications. Important subdirectories include `/usr/bin`, `/usr/sbin`, and `/usr/lib`. |
| `/var` | Contains variable data that changes frequently, such as logs, cache, spool files, and application data. |
| `/var/log` | Stores system and application log files. Common logs include `/var/log/messages`, `/var/log/secure`, and `/var/log/boot.log`. |
| `/tmp` | Stores temporary files. It usually has sticky bit permission, meaning users can create files but cannot delete other users’ files. |
| `/opt` | Used for optional or third-party software installations. Example: `/opt/tomcat`, `/opt/application`. |
| `/mnt` | Temporary mount point used by administrators to manually mount file systems. |
| `/media` | Used for automatically mounted removable media such as USB drives, CDs, or DVDs. |
| `/proc` | Virtual file system that provides information about running processes and kernel parameters. Example: `/proc/cpuinfo`, `/proc/meminfo`. |
| `/sys` | Virtual file system that provides information about kernel, devices, and hardware. |
| `/run` | Stores runtime data created after system boot, such as process IDs and service information. |
| `/srv` | Contains data served by system services such as web, FTP, or other server applications. |

---

## Important Difference: `/` vs `/root`

| Path | Meaning |
|---|---|
| `/` | Root of the entire Linux file system. |
| `/root` | Home directory of the root user. |

Example:

```bash
cd /  ===> This takes you to the root of the file system.

```bash
cd /root === > This takes you to the root user's home directory.

---

## Symbolic Links in Root Directory

In many modern Linux distributions, some directories are symbolic links.

Examples:

```bash
/bin -> /usr/bin
/sbin -> /usr/sbin
/lib -> /usr/lib
/lib64 -> /usr/lib64
```

This means `/bin` is not a separate physical directory. It points to `/usr/bin`.

---

## Permissions Example

Example output:

```bash
drwxr-xr-x  root root  etc
```

Explanation:

| Part        | Meaning                                        |
| ----------- | ---------------------------------------------- |
| `d`         | Directory                                      |
| `rwx`       | Owner has read, write, and execute permissions |
| `r-x`       | Group has read and execute permissions         |
| `r-x`       | Others have read and execute permissions       |
| `root root` | Owner and group are root                       |
| `etc`       | Directory name                                 |

---

## `/tmp` Sticky Bit

Example:

```bash
drwxrwxrwt  root root  tmp
```

The `t` at the end means sticky bit is enabled.

This allows all users to create files inside `/tmp`, but users cannot delete files created by other users.

---

## Real-Time Usage as a Linux/DevOps Engineer

In real-time administration, I commonly use these directories:

| Directory  | Real-Time Use                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------- |
| `/etc`     | Editing service configuration files, SSH settings, hostname, fstab, and network configuration. |
| `/var/log` | Troubleshooting system and application issues by checking logs.                                |
| `/home`    | Managing user files and user-specific configurations.                                          |
| `/opt`     | Installing third-party applications like Tomcat, Java apps, or monitoring agents.              |
| `/tmp`     | Checking temporary files when troubleshooting space issues.                                    |
| `/boot`    | Checking kernel and bootloader files during boot-related troubleshooting.                      |
| `/dev`     | Identifying disk and device files.                                                             |
| `/proc`    | Checking CPU, memory, and process-related information.                                         |
| `/mnt`     | Mounting temporary disks or network file systems.                                              |

---

## Useful Commands

### Check current directory

```bash
pwd
```

### List files and directories

```bash
ls -l
```

or

```bash
ll
```

### Check disk usage

```bash
df -h
```

### Check inode usage

```bash
df -i
```

### Check directory size

```bash
du -sh /var/log/*
```

### Check block devices

```bash
lsblk
```

### Check mounted file systems

```bash
mount
```

### Check persistent mounts

```bash
cat /etc/fstab
```

---

## Interview-Ready Final Answer

Linux file system is a hierarchical structure that starts from the root directory `/`. Everything in Linux is organized under this root directory, including files, directories, devices, and mounted file systems.

The important directories I commonly work with are `/etc` for configuration files, `/var/log` for logs, `/home` for user data, `/root` for the root user’s home directory, `/opt` for third-party applications, `/tmp` for temporary files, `/boot` for kernel and bootloader files, `/dev` for device files, `/proc` for process and kernel information, and `/sys` for hardware and kernel-related information.

From an administration perspective, I use commands like `df -h`, `du -sh`, `lsblk`, `mount`, and `cat /etc/fstab` to check disk usage, mounted file systems, and storage-related issues. I also check permissions, ownership, inode usage, and logs while troubleshooting file system issues.

````


