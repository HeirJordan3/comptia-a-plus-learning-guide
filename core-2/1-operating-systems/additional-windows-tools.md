# Additional Windows Tools

CompTIA A+ Core 2 — 220-1202  
Objective 1.4 — Given a scenario, use the appropriate Microsoft Windows 10/11 features and tools

## What You Need to Know

By the end of this lesson, you should understand:

- **System Information** (`msinfo32.exe`) — a read-only overview of the PC
- **Resource Monitor** (`resmon.exe`) — live detail for CPU, memory, disk, and network
- **System Configuration** (`msconfig.exe`) — how Windows starts
- **Disk Cleanup** (`cleanmgr.exe`) — safe removal of temporary files
- **Defrag** — for spinning hard drives, not SSDs
- **Registry Editor** (`regedit.exe`) — view and edit Windows settings, and back up first

## What Is It?

These are extra Windows troubleshooting utilities. Some only **report** what is on the computer. Others **change** startup behavior, free disk space, or edit the registry.

## Why Does It Matter?

You often sit down at a PC you have never seen. These tools answer:

- What hardware and software are installed?
- Which app is using CPU, disk, or the network right now?
- Can I change how Windows boots, including Safe Boot?
- What junk files can I delete?
- Should I defragment this drive?
- Where does Windows store deep configuration — and how do I undo a registry edit?

## Real-World Analogy

| Tool | Like |
| --- | --- |
| System Information | A spec sheet you can read but not edit |
| Resource Monitor | A live dashboard with more gauges than Task Manager |
| System Configuration | The startup checklist |
| Disk Cleanup | Emptying the trash and temp folders on purpose |
| Defrag | Putting scattered pages of a book back in order on a spinning disk |
| Registry Editor | The master settings cabinet — copy a drawer before you change it |

## How It Works

### System Information (`msinfo32.exe`)

A fast overview of a machine you do not know yet. You **cannot change** settings here. You only look.

**System summary** shows OS name and version, processor, BIOS, boot device, available memory, and free file space.

| Category | What you find |
| --- | --- |
| **Hardware resources** | Memory, DMA, IRQs (interrupts), I/O, conflicts or sharing problems |
| **Components** | Display, sound, network (adapter, protocol, Winsock), storage (drives, disks, IDE/SATA) |
| **Software environment** | System drivers, print jobs, services, program groups, running tasks |

Use it when you want one place instead of opening many separate utilities.

### Resource Monitor (`resmon.exe`)

Sits between two tools you already know:

| Tool | View |
| --- | --- |
| Task Manager | Short, real-time summary |
| Performance Monitor | Long-term history |
| **Resource Monitor** | Real-time view **plus** detailed stats |

Overview breaks down **CPU**, **memory**, **disk**, and **network**, including services in each area. Tabs give a closer look at each category. Use it when you need to see what **one application** is doing with a specific resource.

Open it from Search or by running `resmon.exe`.

### System Configuration (`msconfig.exe`)

Controls what happens behind the Windows splash screen and login prompt.

| Tab | What it does |
| --- | --- |
| **General** | Normal startup, diagnostic startup, or a selective startup |
| **Boot** | Which OS starts if more than one is installed; **Safe boot** and the Safe boot type; hide the GUI, create a boot log, other boot options |
| **Services** | Which services start with the computer |
| **Startup** | Used to list login apps; that list now lives in **Task Manager** |
| **Tools** | Launch Event Viewer, Internet Options, Task Manager, Resource Monitor, and other utilities |

Search for System Configuration or run `msconfig.exe`.

### Disk Cleanup (`cleanmgr.exe`)

Groups files you can delete safely when a drive is full. Common categories:

- Downloaded program files
- Temporary internet files
- Windows error reports
- Recycle Bin
- Temporary files

Selecting a category updates how much space you will free. Confirm before Windows permanently deletes the files.

### Disk Defragmentation

On a spinning hard drive, one file can be stored in many scattered pieces. **Defrag** pulls those pieces into one contiguous layout so reads and writes are faster.

| Drive type | Defrag? |
| --- | --- |
| Spinning hard drive (HDD) | Yes — fragmentation slows the moving disk |
| Solid-state drive (SSD) | No — the drive reaches any fragment without waiting for a spinning platter |

Open it from the drive’s properties (Optimize / defragment), or use the **defrag** command and name the volume. The tool can analyze first. A drive that is already about **98%** efficient usually does not need an optimize pass. Windows can also analyze and optimize on a schedule (often weekly). You can change that schedule in the utility.

### Registry Editor (`regedit.exe`)

Windows stores a huge amount of configuration in the **registry**: kernel settings, services, application options, and more.

User Account Control asks for confirmation because registry edits can seriously change the system. Say yes only when you mean to edit.

The window starts with folders on the left. Each top folder begins with **HKEY** (handle to registry key):

| Key | Short name |
| --- | --- |
| `HKEY_CLASSES_ROOT` | Classes root |
| `HKEY_CURRENT_USER` | Current user |
| `HKEY_LOCAL_MACHINE` | This computer (a common place for software settings) |
| `HKEY_USERS` | Users |
| `HKEY_CURRENT_CONFIG` | Current config |

Entries have a **name**, a **type**, and **data**. Example path: `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion`. Changing a value often needs a restart before Windows uses it.

**Back up before you edit.** File → Export saves a key or a section (a **hive**), or the whole registry, to a file on this PC or another drive. To put it back, run that saved registry file so it writes the old data back.

## Side-by-Side Comparison

| Need | Tool |
| --- | --- |
| Specs of an unfamiliar PC | System Information |
| Which process is hitting the disk right now | Resource Monitor |
| Boot into Safe Mode next time | System Configuration → Boot |
| Stop a program from starting at login | Task Manager Startup (not the old msconfig list) |
| Delete temp files and empty the Recycle Bin | Disk Cleanup |
| Speed up a fragmented HDD | Defrag / Optimize |
| Speed up an SSD the same way | Do not defrag it |
| Change a deep Windows setting | Registry Editor — export first |

## Key Terms

| Term | Meaning |
| --- | --- |
| msinfo32 | System Information |
| DMA | Direct Memory Access |
| IRQ | Interrupt request line for hardware |
| resmon | Resource Monitor |
| msconfig | System Configuration |
| Safe boot | A limited Windows startup used for troubleshooting |
| cleanmgr | Disk Cleanup |
| Defragmentation | Rewriting scattered file pieces into one block on an HDD |
| SSD | Solid-state drive — no spinning disk, so no defrag benefit |
| regedit | Registry Editor |
| HKEY | Handle to a registry key (a top-level registry folder) |
| Hive | A section of the registry you can export and restore |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Read-only hardware, components, and software list | `msinfo32` |
| Live CPU, disk, network, and memory detail | `resmon` |
| Choose Safe boot or diagnostic startup | `msconfig` |
| Startup apps moved out of System Configuration | Task Manager → Startup |
| Free space from temp files | `cleanmgr` |
| “Defrag the SSD” | Do not — defrag is for HDDs |
| Edit configuration stored by Windows | `regedit` — export/backup first |
| HKEY_LOCAL_MACHINE | Registry key for this computer |

## Common Mix-Ups

### System Information is where you change drivers

It is view-only. Change drivers in Device Manager.

### Resource Monitor replaces Performance Monitor

Resource Monitor is detailed and live. Performance Monitor is for long-term history and alerts.

### Always defragment every drive

Defrag helps **spinning hard drives**. SSDs do not need it.

### The registry is safe to click through and edit

A wrong change can break Windows. Export the key or hive before you edit, and know exactly what you are changing.

## Quick Review

| Topic | Remember |
| --- | --- |
| System Information | `msinfo32` — summary, hardware, components, software; no edits |
| Resource Monitor | `resmon` — live CPU, memory, disk, network detail |
| System Configuration | `msconfig` — startup type, Safe boot, services; Startup tab points to Task Manager |
| Disk Cleanup | `cleanmgr` — delete temps and similar files on purpose |
| Defrag | HDDs only; analyze first; SSDs skip it |
| Registry | `regedit` — HKEY folders; export a hive before changes |

---

## Continue Learning

- Previous Topic: [The Microsoft Management Console](the-microsoft-management-console.md)
- Next Topic: [Windows Command Line Tools](windows-command-line-tools.md)
- Related: [Task Manager](task-manager.md)
- Back to [Domain 1 — Operating Systems](README.md)
- Course Map: [Core 2 Study Path](../COURSE-MAP.md)
