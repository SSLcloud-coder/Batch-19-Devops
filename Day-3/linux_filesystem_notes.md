
# Linux File System Structure (Detailed Notes with Examples)

Linux follows a **hierarchical directory structure**, starting from the root directory `/`.
Each directory has a specific purpose and stores certain types of files.

Below is the detailed explanation of the main directories in a Linux system.

---

## `/` – Root Directory
- The top-most directory in the Linux file system.
- All other files and directories are placed under this root.

**Example:**
```bash
ls /
```
Shows all top-level directories.

---

## `/bin` – Essential User Binaries
- Contains essential command binaries (executables) needed for system booting and repair.
- Common user commands are stored here.

**Example:**
```bash
ls /bin
```
Check commands like `ls`, `cp`, `mv`, `cat`, `date`.

---

## `/boot` – Boot Loader Files
- Contains files required for the system to boot, including the Linux kernel.

**Example:**
```bash
ls /boot
```
You may see `vmlinuz` (kernel file) and `initrd.img`.

---

## `/dev` – Device Files
- Contains device files representing hardware like disks, USBs, etc.

**Example:**
```bash
ls /dev | head
```
You will see device names like `sda`, `tty`, `null`.

---

## `/etc` – Configuration Files
- Stores system-wide configuration files.

**Example:**
```bash
cat /etc/passwd
```
Displays user account information.

---

## `/home` – User Home Directories
- Each user has a personal directory inside `/home`.

**Example:**
```bash
cd /home/username
```

---

## `/lib` – Essential Shared Libraries
- Contains shared libraries needed by binaries in `/bin` and `/sbin`.

**Example:**
```bash
ls /lib
```

---

## `/lib64` – 64-bit Libraries
- Stores 64-bit versions of essential libraries.

**Example:**
```bash
ls /lib64
```

---

## `/media` – Removable Media
- Mount point for removable devices like USB drives, CDs.

**Example:**
```bash
ls /media
```

---

## `/mnt` – Temporary Mount Point
- Used for temporarily mounting filesystems.

**Example:**
```bash
sudo mount /dev/sdb1 /mnt
```

---

## `/opt` – Optional Packages
- Stores optional software packages.

**Example:**
```bash
ls /opt
```

---

## `/proc` – Process Information
- Virtual filesystem providing process and kernel information.

**Example:**
```bash
cat /proc/cpuinfo
```

---

## `/root` – Root User’s Home
- Home directory for the root user.

**Example:**
```bash
cd /root
```

---

## `/run` – Runtime Variable Data
- Stores runtime data since the last boot.

**Example:**
```bash
ls /run
```

---

## `/sbin` – System Binaries
- Contains system administration commands.

**Example:**
```bash
ls /sbin
```

---

## `/srv` – Service Data
- Stores data for system services.

**Example:**
```bash
ls /srv
```

---

## `/tmp` – Temporary Files
- Stores temporary files; cleared on reboot.

**Example:**
```bash
touch /tmp/testfile
ls /tmp
```

---

## `/usr` – User Programs
- Contains installed software, documentation, libraries.

**Example:**
```bash
ls /usr/bin
```

---

## `/var` – Variable Data
- Contains files that change frequently (logs, spool files).

**Example:**
```bash
ls /var/log
```

---

## Summary Table

| Directory | Purpose | Example Command |
|-----------|---------|----------------|
| `/` | Root directory | `ls /` |
| `/bin` | Essential binaries | `ls /bin` |
| `/boot` | Boot files | `ls /boot` |
| `/dev` | Device files | `ls /dev` |
| `/etc` | Config files | `cat /etc/passwd` |
| `/home` | User home dirs | `cd /home/username` |
| `/lib` | Libraries | `ls /lib` |
| `/lib64` | 64-bit libs | `ls /lib64` |
| `/media` | Removable media | `ls /media` |
| `/mnt` | Temp mount point | `mount /dev/sdb1 /mnt` |
| `/opt` | Optional software | `ls /opt` |
| `/proc` | Process info | `cat /proc/cpuinfo` |
| `/root` | Root's home | `cd /root` |
| `/run` | Runtime data | `ls /run` |
| `/sbin` | System binaries | `ls /sbin` |
| `/srv` | Service data | `ls /srv` |
| `/tmp` | Temp files | `ls /tmp` |
| `/usr` | User programs | `ls /usr/bin` |
| `/var` | Variable data | `ls /var/log` |

---
