
# 🗂️ Linux File System – Detailed Notes

## 📌 1. What is a File System?

A **file system** organizes how data is stored and retrieved on a disk. In Linux, everything is a **file** — whether it’s a document, a directory, a hardware device, or a process.

## 📁 2. Linux Directory Structure Overview (`/`)

Linux uses a **hierarchical directory structure** — a tree with root (`/`) at the top.

```
/
├── bin/
├── boot/
├── dev/
├── etc/
├── home/
├── lib/
├── media/
├── mnt/
├── opt/
├── proc/
├── root/
├── run/
├── sbin/
├── srv/
├── sys/
├── tmp/
├── usr/
└── var/
```

## 📂 3. Important Linux Directories

| Directory | Description |
|-----------|-------------|
| `/` | Root directory. Starting point of entire file system. |
| `/bin` | Essential user binaries (e.g., `ls`, `cp`, `mv`) |
| `/sbin` | System binaries for root (e.g., `iptables`, `reboot`) |
| `/boot` | Boot loader files (e.g., `vmlinuz`, `initrd`) |
| `/dev` | Device files (e.g., `/dev/sda`, `/dev/null`) |
| `/etc` | Configuration files (e.g., `/etc/hostname`, `/etc/fstab`) |
| `/home` | User home directories (e.g., `/home/sonu`) |
| `/lib` | Essential shared libraries needed to boot and run the system |
| `/media` | Mount point for removable media (USB, CD-ROM) |
| `/mnt` | Temporary mount point (admin use) |
| `/opt` | Optional software and third-party apps |
| `/proc` | Virtual directory for process and kernel info |
| `/root` | Home directory for the root user |
| `/run` | Runtime variable data |
| `/srv` | Site-specific data served by the system (e.g., web, ftp) |
| `/sys` | Virtual system information |
| `/tmp` | Temporary files (auto deleted on reboot) |
| `/usr` | User programs, libraries (non-essential at boot) |
| `/var` | Variable data like logs, mail, print spool |

## 🧠 4. Virtual vs Physical Files

- **Virtual Files:** `/proc`, `/sys` — generated dynamically by the kernel.
- **Physical Files:** `/etc/passwd`, `/home/username`, real data stored on disk.

## 🛠️ 5. Common File System Types in Linux

| File System | Use |
|-------------|-----|
| `ext4` | Default in most distros (fast, stable) |
| `xfs` | Used in RHEL/CentOS 7+ |
| `btrfs` | Snapshot and RAID features |
| `vfat` / `ntfs` | Windows-compatible |
| `tmpfs` | Temporary RAM-based file system (used in `/tmp`, `/run`) |
| `nfs` | Network File System |
| `iso9660` | CD/DVD file systems |

## 📊 6. Useful Commands to Explore File System

| Command | Description |
|---------|-------------|
| `df -h` | Shows disk space usage |
| `du -sh /folder/` | Folder size |
| `mount` | Shows mounted file systems |
| `lsblk` | Lists block devices |
| `blkid` | Shows UUID and type of partitions |
| `file filename` | Shows file type |
| `stat filename` | Shows metadata of file |
| `find / -name filename` | Search file in entire system |

## 🛑 7. Permissions and Ownership

Each file has:

- **Owner**
- **Group**
- **Permission bits:** read (r), write (w), execute (x)

Check with:
```bash
ls -l
```

## 🔐 8. Important Config Files

| File | Use |
|------|-----|
| `/etc/fstab` | Auto-mount file systems at boot |
| `/etc/mtab` | Currently mounted systems |
| `/etc/passwd` | User accounts |
| `/etc/group` | Groups |
| `/etc/shadow` | Encrypted user passwords |

## 📦 9. Mounting File Systems

```bash
mount /dev/sdb1 /mnt/mydrive
umount /mnt/mydrive
```

To auto-mount on boot, add entry in `/etc/fstab`.

## 🧹 10. Temporary vs Persistent Storage

| Type | Example | Deletes on reboot? |
|------|---------|--------------------|
| Temporary | `/tmp`, `/run`, `tmpfs` | ✅ Yes |
| Persistent | `/home`, `/var`, `/opt` | ❌ No |

## 📘 11. File System Hierarchy Standard (FHS)

Linux follows FHS — a set of rules for what directory should contain what type of files.

🔗 [More Info](https://refspecs.linuxfoundation.org/FHS_3.0/fhs/index.html)

## 🧾 Example Interview Q&A

**Q1:** What is the purpose of `/proc` directory?  
**A:** It’s a virtual filesystem providing process and kernel info.

**Q2:** What is the difference between `/bin` and `/sbin`?  
**A:** `/bin` is for general user commands, `/sbin` is for system admin commands.

**Q3:** How do you check disk usage?  
**A:** Use `df -h` or `du -sh <folder>`.
