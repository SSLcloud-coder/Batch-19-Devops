# Linux Class Notes - Day 1

## 1. Linux History

- **Created By**: Linus Torvalds in 1991 while studying at the University of Helsinki.
- **Inspiration**: Inspired by MINIX (a small UNIX clone used for teaching).
- **Goal**: To create a free and open-source UNIX-like operating system.
- **Growth**: Supported by a global community of developers; now forms the backbone of cloud computing, servers, and embedded systems.

## 2. Linux vs Windows

| Feature             | Linux                                 | Windows                       |
| ------------------- | ------------------------------------- | ----------------------------- |
| Source Code         | Open-source                           | Closed-source                 |
| Cost                | Free or minimal cost                  | Paid license                  |
| Customization       | Highly customizable                   | Limited customization         |
| Security            | More secure (less targeted)           | Frequent target of malware    |
| Performance         | Lightweight, better on older hardware | Heavier, needs more resources |
| File System Support | Ext4, XFS, Btrfs, etc.                | NTFS, FAT32, exFAT            |
| User Interface      | CLI + GUI (GNOME, KDE, etc.)          | Mostly GUI                    |
| Use Case            | Servers, DevOps, Cloud, Security      | Desktop, Gaming, Business     |

## 2.1 Why Linux is Better than Windows and Other OS

- **Open Source & Free**: Linux is free to use and modify, unlike Windows or macOS which are proprietary.
- **Performance**: It runs efficiently on old and low-spec hardware, making it ideal for servers.
- **Security**: Better security architecture with user permissions and less virus threat.
- **Customization**: Every component (desktop, tools, kernel) can be modified.
- **Command-line Power**: Rich command-line tools for automation and scripting.
- **Community Support**: Vast support from forums, documentation, and communities.
- **Privacy**: No forced telemetry or tracking like Windows.
- **Stability**: Linux systems can run for years without reboots (ideal for servers).
- **Package Management**: Tools like APT, YUM, DNF make installing software easy and scriptable.

## 3. Linux File System Hierarchy

- `/` — Root directory (starting point of all paths)
- `/bin` — Essential binaries
- `/boot` — Boot loader files (e.g., GRUB, kernel)
- `/etc` — Configuration files
- `/home` — User home directories
- `/lib` — Shared libraries
- `/media` — Mounted external drives
- `/mnt` — Temporarily mounted filesystems
- `/opt` — Optional/additional software
- `/tmp` — Temporary files
- `/usr` — User programs and data
- `/var` — Variable data (logs, mail, etc.)

## 4. Types of Users in Linux

- **Root User**: Superuser with full permissions
- **System Users**: Created by OS/services (e.g., `apache`, `mysql`)
- **Regular Users**: Created by admin for human users

## 5. Linux Distributions (Distros)

- **Definition**: A collection of Linux kernel + software + package manager
- **Popular Distros**:
  - Ubuntu
  - Debian
  - Red Hat Enterprise Linux (RHEL)
  - CentOS (now replaced by CentOS Stream)
  - Fedora
  - Arch Linux
  - Kali Linux

## 6. RHEL (Red Hat Enterprise Linux)

- **Enterprise-level** Linux distro developed by Red Hat Inc.
- **Features**:
  - Paid subscription-based
  - Long-term support and security updates
  - Certified for hardware and software
  - Used in enterprises, banking, cloud, telecom

## 7. RHEL Versions Overview

| Version | Released | Notes                                   |
| ------- | -------- | --------------------------------------- |
| RHEL 6  | 2010     | Legacy, nearing end of support          |
| RHEL 7  | 2014     | systemd introduced, improved networking |
| RHEL 8  | 2019     | AppStream, DNF, modularity introduced   |
| RHEL 9  | 2022     | Kernel 5.x, Wayland, cloud-native focus |

## 8. Open Source vs Enterprise Linux

| Feature          | Open Source Linux  | Enterprise Linux (e.g., RHEL)      |
| ---------------- | ------------------ | ---------------------------------- |
| Cost             | Free               | Paid (subscription/license)        |
| Support          | Community-based    | Professional support (SLA)         |
| Stability        | Can vary by distro | Highly stable and tested           |
| Security Patches | Manual or delayed  | Regular, automated, certified      |
| Certification    | No                 | Certified for cloud, apps, vendors |

---
**Next Topics:** Linux commands, User management, Package Management, File Permissions

*Prepared for classroom use by [Your Name/Institute]*
