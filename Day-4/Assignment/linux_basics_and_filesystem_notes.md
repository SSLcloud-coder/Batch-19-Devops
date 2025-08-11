# Linux Basics + File System – Study & Interview Notes

## Part 1 – Linux Basic Commands

| Command   | Description | Example | Output/Explanation |
|-----------|-------------|---------|--------------------|
| **`ls`**  | Lists files & directories in the current location | `ls` | Shows file & folder names |
|           | Show with details | `ls -l` | Long listing format |
|           | Show hidden files | `ls -a` | Includes `.hidden` files |
| **`date`** | Displays current system date & time | `date` | e.g., `Mon Aug 11 11:05:00 IST 2025` |
|           | Custom format | `date "+%d-%m-%Y"` | `11-08-2025` |
| **`cal`** | Shows calendar of the current month | `cal` | Calendar output |
|           | Show full year calendar | `cal 2025` | 12-month view |
| **`pwd`** | Shows **Present Working Directory** | `pwd` | e.g., `/home/user` |
| **`cd`**  | Change directory | `cd /etc` | Moves to `/etc` |
|           | Go to home directory | `cd` | Home folder |
|           | Go one step back | `cd ..` | Parent directory |
| **`whoami`** | Displays the current logged-in username | `whoami` | e.g., `root` |
| **`last`**   | Shows the last logged-in users with date & time | `last` | Login history from `/var/log/wtmp` |
|             | Show specific user’s login history | `last username` | Filtered login history |
| **`top`**    | Displays real-time system resource usage | `top` | CPU, memory, process usage |
|             | Show full command name in top output | Press `c` inside `top` | Full command path |

---

## Absolute Path in Linux

- **Definition:** A full path starting from root `/`.
- Always starts with `/`.
- Works from any location.

**Example:**
```bash
cd /var/log
pwd
# Output: /var/log
```

---

## Linux Command Structure

```bash
command  [argument]  [value]
```
- **Command** → Main action (`ls`, `cd`, `whoami`)
- **Argument** → Option (`-l`, `-a`, `-n`)
- **Value** → Target (`/etc`, `username`)

**Example:**
```bash
ls -l /home
# command: ls
# argument: -l
# value: /home
```

---

## Help Commands in Linux

| Command | Purpose | Example | Output |
|---------|---------|---------|--------|
| **`man`** | Shows detailed manual page of a command | `man ls` | Opens full documentation |
| **`--help`** | Displays quick help & options | `ls --help` | List of flags & usage |
| **`info`** | Shows detailed info page | `info ls` | GNU info format |
| **`whatis`** | One-line description | `whatis pwd` | Short definition |
| **`apropos`** | Search commands related to keyword | `apropos calendar` | Related commands list |

---

## Using the `man` Command

**Syntax:**
```bash
man [section] command
```

**Sections in `man` pages**:
1 → User commands  
2 → System calls  
3 → Library functions  
4 → Special files  
5 → File formats  
6 → Games  
7 → Miscellaneous  
8 → System administration commands  

**Examples:**
```bash
man ls        # Show manual for ls
man 5 passwd  # Show /etc/passwd file format
```

**Navigation inside `man`:**
- **Space** → Scroll down
- **b** → Scroll up
- **q** → Quit

---

## Part 2 – Linux File System Detailed Notes

Linux file system follows a **tree-like structure** starting from `/` (root).

### Common Directories and Their Purpose

| Directory | Purpose | Example Usage |
|-----------|---------|---------------|
| `/` | Root directory (starting point of file system) | `cd /` |
| `/bin` | Essential user commands | `/bin/ls`, `/bin/cp` |
| `/sbin` | System administration commands | `/sbin/reboot` |
| `/boot` | Boot loader files (kernel, initrd) | `/boot/vmlinuz` |
| `/dev` | Device files | `/dev/sda`, `/dev/null` |
| `/etc` | Configuration files | `/etc/hostname` |
| `/home` | User home directories | `/home/user1` |
| `/lib`, `/lib64` | Shared libraries needed by binaries | `/lib/systemd/systemd` |
| `/media` | Mount point for removable devices | `/media/usb` |
| `/mnt` | Temporary mount point | `/mnt/test` |
| `/opt` | Optional software packages | `/opt/software` |
| `/proc` | Virtual file system for process info | `/proc/cpuinfo` |
| `/root` | Home directory for root user | `/root` |
| `/run` | Temporary runtime data | `/run/systemd` |
| `/srv` | Data for services | `/srv/ftp` |
| `/tmp` | Temporary files | `/tmp/temp.txt` |
| `/usr` | User programs and data | `/usr/bin`, `/usr/lib` |
| `/var` | Variable data (logs, spool) | `/var/log/messages` |

---

## Part 3 – Assignment Questions

### Practical Tasks
1. List all files including hidden ones in `/etc`.
2. Show calendar of the year 2027.
3. Find your current working directory.
4. Change to `/var/log` and display its contents in long format.
5. Find the username of the current user.
6. Show last 5 login attempts.
7. Display top 10 processes consuming most CPU.
8. Show manual page for the `passwd` file format.
9. Navigate to `/tmp` and create a file `test.txt`.
10. Find the absolute path of `/etc/hosts`.

### Theory Questions
1. What is an absolute path? Give an example.
2. Difference between `/bin` and `/sbin`.
3. What is stored in `/var/log`?
4. Purpose of `/etc/passwd` file.
5. Difference between `/media` and `/mnt`.

---

## Part 4 – Interview Questions

1. Explain the Linux file system hierarchy.
2. What is the difference between absolute path and relative path?
3. How does `pwd` command work?
4. Difference between `ls -l` and `ls -a`.
5. Purpose of `/etc/fstab` file.
6. What is `/proc` and why is it important?
7. Difference between `/lib` and `/lib64`.
8. How do you find your username in Linux?
9. Difference between `man` and `--help`.
10. How to check last login details of a user?
11. What is the function of `/boot` directory?
12. Difference between `/tmp` and `/var/tmp`.
13. How to see real-time CPU and memory usage?
14. Why is `/root` different from `/`?
15. How would you mount a USB drive in Linux?
