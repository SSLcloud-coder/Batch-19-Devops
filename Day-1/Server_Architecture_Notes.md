# Server Architecture Notes

## 1. BIOS (Basic Input/Output System)

**What is BIOS?**  
BIOS is low-level software embedded on a chip on the motherboard. It is the first code that runs when the server is powered on and is responsible for initializing and testing hardware components before handing over control to the OS.

### Key Functions:
- Performs POST (Power-On Self-Test)
- Detects and initializes hardware peripherals
- Loads the bootloader of the OS
- Stores configuration settings in CMOS

### Role in Servers:
- Manages boot priority (e.g., PXE boot)
- Provides configuration for RAID setup, virtualization, secure boot
- Integrated with remote management features

---

## 2. Firmware

**What is Firmware?**  
Firmware is permanent software programmed into hardware components. It acts as an interface between hardware and higher-level software.

### Examples:
- NIC firmware
- RAID controller firmware
- BMC firmware

### Key Functions:
- Controls low-level operations of hardware
- Stored in non-volatile memory (Flash)
- Can be updated for performance or security

### Role in Servers:
- Manages network/storage controller operations
- Enables remote monitoring & power management

---

## 3. Kernel

**What is Kernel?**  
The kernel is the core of the OS, managing hardware resources and enabling communication between software and hardware.

### Responsibilities:
- Process and memory management
- File system control
- System calls
- Device driver interaction

### Types of Kernels:
- Monolithic (e.g., Linux)
- Microkernel

### Server Role:
- Manages hardware utilization
- Optimized for performance, tuning, security

---

## 4. Operating System (OS)

**What is an OS?**  
System software that manages server hardware, runs applications, and provides services to users and programs.

### Examples:
- Linux (Red Hat, Ubuntu Server)
- Windows Server
- Unix variants (AIX, Solaris)

### Key Functions:
- User and file management
- Service handling
- Automation, monitoring, security

### Server Role:
- Runs apps/services
- Supports virtualization and cloud

---

## 5. Server Hardware Components

| Component         | Description                         | Server Role                                      |
|------------------|-------------------------------------|-------------------------------------------------|
| CPU              | Processor with multiple cores       | Handles tasks, virtualization                   |
| RAM              | Volatile memory                     | Buffers, caches, temporary data                 |
| Storage          | HDD/SSD/NVMe                        | Stores data, OS, and applications               |
| Motherboard      | Main circuit board                  | Connects all server components                  |
| NIC              | Network interface                   | Data transfer across network                    |
| RAID Controller  | Disk management                     | Ensures speed/redundancy                        |
| Power Supply     | Converts power                      | Stable voltage supply                           |
| Cooling System   | Fans, heat sinks, liquid cooling    | Maintains optimal temp                          |
| BMC              | Embedded controller                 | Remote management (out-of-band)

---

## Remote Server Management Tools (Firmware-based)

| Tool  | Vendor | Purpose                                 |
|-------|--------|------------------------------------------|
| iLO   | HP     | Remote access, power, monitoring         |
| iDRAC | Dell   | BIOS control, remote console             |
| IPMI  | Generic| Command-line remote management           |

---

## Summary Table

| Layer           | Role                                 | Where It Runs From     | How It's Updated              |
|----------------|--------------------------------------|------------------------|-------------------------------|
| BIOS           | Initializes hardware                 | ROM/EEPROM             | BIOS firmware update          |
| Firmware       | Controls hardware behavior           | Flash Memory           | Vendor-specific tools         |
| Kernel         | Interfaces hardware & OS             | RAM (loaded by OS)     | OS update or custom build     |
| Operating System | Hosts apps and services             | Disk (HDD/SSD)         | Manual or automatic updates   |

---

## Architecture Diagram

*(You can insert your image or diagram here if needed)*