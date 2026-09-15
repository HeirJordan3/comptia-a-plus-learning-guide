# Windows Features

CompTIA A+ Core 2 — 220-1202  
Objective 1.3 — Microsoft Windows

## What You Need to Know

By the end of this lesson, you should understand:

- What Active Directory Domain Services is used for
- The difference between a workgroup and a domain
- What RDP client vs RDP service/host means
- RAM limits by Windows edition
- BitLocker vs EFS encryption
- Local Group Policy vs enterprise Group Policy management

## What Is It?

Windows includes enterprise features for managing many devices at once.

This lesson covers:

- Domain Services / Active Directory
- Remote Desktop Protocol (RDP)
- RAM support by edition
- Encryption with BitLocker and EFS
- Group Policy management

Large organizations may manage hundreds or thousands of Windows devices for installs, updates, security, and permissions — including laptops that leave the building with sensitive data.

## Why Does It Matter?

Help desk work depends on these features:

- Users authenticate against Active Directory
- Techs connect with Remote Desktop
- Lost laptops need disk encryption
- Admins lock down desktops with Group Policy

Knowing which features exist — and which editions support them — helps you troubleshoot faster.

## Real-World Analogy

Think of a company Windows network like a school campus:

- **Active Directory** = the main office roster of students, staff, and rooms
- **Workgroup** = each classroom keeping its own attendance sheet
- **RDP** = a camera/remote control so the help desk can operate a classroom PC from the office
- **BitLocker** = locking the whole filing cabinet
- **EFS** = locking selected folders inside the cabinet
- **Group Policy** = campus rules applied to every classroom the same way

## How It Works

### Active Directory Domain Services

In business networks, systems are commonly documented in a central database called **Active Directory Domain Services (AD DS)**.

It can store information about:

- Usernames and permissions
- Security settings
- Servers, printers, laptops, and other infrastructure objects

Central management benefits:

- Scale to many devices
- Manage very different systems from one place
- Distributed copies of the database across the network for scalability and redundancy

Home environments usually do **not** use Active Directory because there are only a few accounts to manage.

If you log on to a corporate network, connect to VPN, or access a network share, authentication is often based on Active Directory information.

### Workgroup vs Domain

| Model | Where | How management works |
| --- | --- | --- |
| Windows workgroup | Common at home | Each device managed as its own unit |
| Windows domain (Active Directory) | Common at work | Central authentication and management for thousands of devices |

### Standardized Desktops at Work

Corporate desktops are often locked down for consistency:

- Fixed background
- Limited language changes
- Restricted software install/remove

That makes systems easier to support — any tech can sit down and know where things are.

At home, users usually customize backgrounds, colors, fonts, and installed software freely.

### Remote Desktop Protocol (RDP)

**Remote Desktop** lets you view and control another computer’s desktop over the network.

Two parts:

| Piece | Role |
| --- | --- |
| RDP client | Software you use to connect to the remote PC |
| Remote Desktop service (host) | Service on the remote PC that accepts the connection |

RDP clients exist for Windows, macOS, Linux, Android, iOS, and more.

Remote Desktop **service/host** is available in:

- Windows 10 Pro and Enterprise
- Windows 11 Pro and Enterprise

It is **not** available in Windows 10/11 Home. On Home, support often means walking to the other room.

### RAM Support by Edition

| Edition / architecture | Max RAM (from lesson) |
| --- | --- |
| Windows 10/11 Home (64-bit) | 128 GB |
| Windows 10 Home (32-bit) | 4 GB |
| Windows 10 Pro / Enterprise (32-bit) | 4 GB |
| Windows 10/11 Pro (64-bit) | 2 TB |
| Windows 10/11 Enterprise (64-bit) | 6 TB |

Notes:

- Windows 11 has **no** 32-bit Home edition
- 4 GB is the 32-bit Windows memory ceiling

### Encryption: BitLocker and EFS

| Technology | Scope | Idea |
| --- | --- | --- |
| **EFS** (Encrypting File System) | Selected files/folders on NTFS | Encrypt specific resources |
| **BitLocker** | Full Disk Encryption (FDE) | Encrypt the whole volume — OS, data, everything |

If a laptop drive is removed, BitLocker-protected data remains unreadable without the keys.

Both technologies are used in business and home contexts. Edition details for BitLocker vs Home Device Encryption were also covered in [An Overview of Windows](an-overview-of-windows.md).

### Group Policy

Group Policy sets rules for how systems behave.

| Tool | When you use it |
| --- | --- |
| Local Group Policy Editor (`gpedit.msc`) | Single device without Active Directory |
| Group Policy Management Console (`gpmc.msc`) | Enterprise Active Directory policies across many systems |

At work, Group Policy is part of Active Directory and can apply settings across the whole organization.

## Key Terms

| Term | Meaning |
| --- | --- |
| Active Directory Domain Services | Central directory database for users, devices, and policies |
| Workgroup | Peer-style grouping without central AD management |
| Domain | Centralized Windows network management model |
| RDP | Remote Desktop Protocol |
| RDP client | App used to connect to a remote desktop |
| Remote Desktop service | Host service that accepts RDP connections |
| BitLocker | Full disk encryption |
| EFS | Encrypting File System for selected NTFS files/folders |
| FDE | Full Disk Encryption |
| gpedit.msc | Local Group Policy Editor |
| gpmc.msc | Group Policy Management Console |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Central business user/device database | Active Directory |
| Home PCs without central AD | Workgroup |
| Help desk controls another PC’s desktop | RDP |
| RDP host available | Pro / Enterprise (not Home) |
| Encrypt one folder | EFS |
| Encrypt entire drive | BitLocker / FDE |
| Edit policy on one standalone PC | gpedit.msc |
| Manage policies across the company | gpmc.msc / AD Group Policy |
| 2 TB RAM on Pro / 6 TB on Enterprise | 64-bit edition limits |

## Common Mix-Ups

### Workgroup vs domain

Workgroup = each PC on its own. Domain = central Active Directory control.

### RDP client vs RDP host

Almost any OS can run a client. Hosting Remote Desktop needs Pro/Enterprise.

### BitLocker vs EFS

BitLocker = whole volume. EFS = selected files/folders.

### gpedit vs gpmc

Local editor for one machine vs enterprise console for Active Directory policies.

## Quick Review

| Feature | Remember |
| --- | --- |
| Active Directory | Central enterprise directory |
| Workgroup | Home-style, per-device management |
| RDP | Remote control; host on Pro/Enterprise |
| RAM limits | Home 128 GB; Pro 2 TB; Enterprise 6 TB (64-bit) |
| EFS | File/folder encryption |
| BitLocker | Full disk encryption |
| Group Policy | gpedit.msc local; gpmc.msc enterprise |

---

## Continue Learning

- Previous Topic: [An Overview of Windows](an-overview-of-windows.md)
- Next Topic: [Task Manager](task-manager.md)
- Related: [File Systems](file-systems.md)
- Back to [Domain 1 — Operating Systems](README.md)
- Back to [Core 2](../README.md)
