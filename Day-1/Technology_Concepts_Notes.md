# Technology Concepts Notes

## 1. Difference between UEFI and BIOS

| Feature        | BIOS (Basic Input Output System)             | UEFI (Unified Extensible Firmware Interface)      |
|---------------|----------------------------------------------|--------------------------------------------------|
| Definition     | A legacy firmware used to initialize hardware during booting. | A modern firmware interface that replaces BIOS. |
| User Interface | Text-based interface with keyboard-only support. | Graphical interface with mouse and keyboard support. |
| Storage Support| Supports drives up to 2.2 TB using MBR.     | Supports drives > 2 TB using GPT.                |
| Boot Speed     | Slower boot time.                           | Faster boot time.                                |
| Security       | Less secure.                                | Supports Secure Boot.                            |
| Architecture   | 16-bit mode.                                | 32-bit or 64-bit mode.                           |
| Extensibility  | Difficult to update and limited features.   | Easier to update and supports more features.     |
| Compatibility  | Compatible with older hardware.             | Requires modern hardware.                        |

**In short:** UEFI is the newer, more secure, and faster replacement for BIOS.

---

## 2. Difference between App and Software

| Feature       | App (Application)                            | Software                                          |
|---------------|----------------------------------------------|--------------------------------------------------|
| Definition     | A specific program designed to perform a particular function. | A broad term including all types of computer programs. |
| Scope          | Subset of software.                         | Includes OS, drivers, utilities, and applications. |
| Usage          | Usually user-interactive.                   | Can be system or application software.            |
| Installation   | Lightweight and easy to install.            | May require complex installation.                |
| Examples       | Instagram, Zoom, Chrome                     | Windows OS, Antivirus, Office                    |

**In short:** All apps are software, but not all software is an app.

---

## 3. Difference between Private Cloud and Public Cloud

| Feature      | Private Cloud                                 | Public Cloud                                     |
|--------------|-----------------------------------------------|--------------------------------------------------|
| Ownership     | Owned by one organization.                   | Provided by third-party providers.               |
| Access        | Limited to organization’s employees.         | Available to public or many organizations.       |
| Cost          | High initial cost, more control.             | Pay-as-you-go, cost-efficient.                   |
| Security      | High — dedicated & customizable.             | Lower — shared environment.                      |
| Customization | Fully customizable.                          | Limited customization.                           |
| Example       | Own infrastructure in data center.           | AWS, Azure, Google Cloud                         |

**In short:**  
Private Cloud = more control & security  
Public Cloud = more flexibility & affordability

---

## 4. What is a Data Center?

A **Data Center** is a facility used to house computer systems and related components, such as storage systems, networking devices, and backup power supplies.  
It is the heart of IT operations.

### Key Components:

- **Servers** – Machines that process and store data.  
- **Storage Systems** – Hard drives, SSDs, SAN, NAS, etc.  
- **Networking Equipment** – Routers, switches, firewalls.  
- **Cooling Systems** – Maintain optimal temperatures.  
- **Power Supply** – Generators, UPS, batteries.  
- **Security Systems** – CCTV, guards, firewalls, antivirus.  

---

## 5. Types of Data Centers

| Type                     | Description                        | Example Use              |
|--------------------------|------------------------------------|---------------------------|
| Enterprise Data Center   | Owned and operated by one organization. | Banks, MNCs              |
| Colocation Data Center   | Shared space in a third-party facility. | Startups, SMBs           |
| Managed Services Data Center | Outsourced infrastructure management. | IT outsourcing clients   |
| Cloud Data Center        | Hosted by cloud providers, accessed remotely. | AWS, Azure, Google Cloud |
| Edge Data Center         | Small centers close to users for low latency. | IoT, smart cities        |