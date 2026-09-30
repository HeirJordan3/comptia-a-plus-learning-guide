# The Microsoft Management Console

CompTIA A+ Core 2 — 220-1202  
Objective 1.4 — Given a scenario, use the appropriate Microsoft Windows 10/11 features and tools

## What You Need to Know

By the end of this lesson, you should understand:

- What the **Microsoft Management Console (MMC)** is and how snap-ins work
- How to build and save a custom console
- **Event Viewer**, **Disk Management**, and **Task Scheduler**
- **Device Manager**, **Certificate Manager**, and **Local Users and Groups**
- **Performance Monitor** for problems that already happened
- **Local Group Policy Editor** vs domain Group Policy

## What Is It?

The **Microsoft Management Console** is an empty framework (`mmc.exe`) you fill with Windows admin tools called **snap-ins**. One saved console can hold Event Viewer, Disk Management, Device Manager, and other tools so you do not hunt for each one separately.

## Why Does It Matter?

Troubleshooting often jumps between logs, disks, drivers, users, and performance history. MMC lets you:

- Put the tools you use most on one screen
- Open the same toolkit later
- Manage the local computer — or, for some snap-ins, another computer on the network

Many of these tools also launch on their own with a `.msc` command.

## Real-World Analogy

Think of MMC like an empty toolbox:

| Piece | Meaning |
| --- | --- |
| Empty console | The toolbox before you add anything |
| Snap-in | One tool you drop in (Event Viewer, Disk Management, and so on) |
| Saved console | Your labeled toolbox, ready the next time you open it |
| `.msc` file | Opening one tool by itself, outside the toolbox |

## How It Works

### Building a Console

1. Run **mmc** (or `mmc.exe`)
2. Approve the prompt if Windows asks to make changes
3. **File → Add/Remove Snap-in**
4. Add tools such as Computer Management, Device Manager, or Disk Management
5. When asked, choose **this computer** or another computer on the network
6. **File → Save** so you can reopen that layout later

Click a snap-in on the left to use that tool.

### Useful Launch Commands

| Tool | Command |
| --- | --- |
| Event Viewer | `eventvwr.msc` |
| Disk Management | `diskmgmt.msc` |
| Task Scheduler | `taskschd.msc` |
| Device Manager | `devmgmt.msc` |
| Certificate Manager | `certmgr.msc` |
| Performance Monitor | `perfmon.msc` |
| Local Group Policy Editor | `gpedit.msc` |
| Group Policy Management (domain) | `gpmc.msc` |

### Event Viewer

Event Viewer is the Windows log viewer. Common Windows logs:

| Log | Typical contents |
| --- | --- |
| Application | App messages |
| Security | Logons and audits |
| Setup | Install and setup activity |
| System | Windows and driver/service events |

Event levels include informational, warning, error, critical, successful audit, and failure audit.

Logs can contain thousands of entries. **Filter** the current log by level, source, keywords, user, or computer so you do not page through everything. Example: an Application log entry from **VSS** (Volume Shadow Copy Service) can show an error and details about that service.

### Disk Management

Disk Management shows installed drives, how they are partitioned, and which file systems they use.

A typical Windows disk may show:

| Partition | What you often see |
| --- | --- |
| Recovery | No drive letter — used for recovery |
| EFI system | No drive letter — used during startup |
| C: | Main OS volume — often **NTFS**, may be **BitLocker** encrypted, marked healthy, boot, page file, crash dumps |

Right-click a volume to change the drive letter or path, **shrink** the volume, **extend** it if free space exists, or **mirror** data across physical drives.

**Backup first.** Changes here can delete data.

### Task Scheduler

Task Scheduler runs a program at a date and time, or on a repeating schedule. Windows already includes many predefined tasks. You can organize tasks in folders.

The main view shows tasks that ran in the last 24 hours. You can widen that to 7 or 30 days. The Task Scheduler Library lists configured tasks (for example, a daily Microsoft update task).

A task is built from:

| Part | Meaning |
| --- | --- |
| Triggers | When it runs |
| Actions | What it runs |
| Conditions | Extra requirements before it runs |
| Settings | Extra behavior for that task |

Create a task from the right-side menu: name, program, day/time, conditions, and settings.

### Device Manager

Device Manager shows how Windows talks to hardware through **device drivers**. Drivers are usually written for the OS you are running (Windows 10 drivers for Windows 10, Windows 11 drivers for Windows 11). Some drivers support more than one OS, but most installs are OS-specific.

Hardware is grouped (printers, display adapters, keyboards, monitors, and so on). Open a device to see:

- Driver name and details
- Recent events
- Resources the hardware uses

Right-click a device to **update**, **disable**, or **uninstall** the driver. Many devices also have their own installer.

### Certificate Manager

Certificates identify a computer or support encryption. Certificate Manager lets you add, remove, or view installed certificates.

A common check: **Trusted Root Certification Authorities → Certificates**. Open a certificate to read its details. Browsers use these trusted CAs when deciding whether a site certificate is trusted.

### Local Users and Groups

Windows can have many users, including people who connect over the network. Local Users and Groups sets rights by user and by group.

| Built-in idea | Meaning |
| --- | --- |
| Administrator | Full local admin account |
| Guest | Limited built-in guest account |
| Regular user | A normal local account |
| Groups | Administrators, Users, Backup Operators, Power Users, and others |

You can add users and groups. Right-click and choose **New User** to create another local account.

This tool is for **local** accounts on this computer, not the full Active Directory directory.

### Performance Monitor

Task Manager’s Performance tab is a short, live view (about the last minute). **Performance Monitor** collects metrics over hours, days, or weeks so you can study a problem after it is gone.

You can track hundreds of counters (disk, memory, CPU, and more), set alerts when a level is crossed, store the data, and build reports.

Default views often include memory, network, physical disk, and processor. Add counters with the plus sign — for example, under **Processor**, add the counters you need. Do not add every counter at once. Leave collection running, then return to the history when the problem happens again.

### Group Policy

Group Policy controls what users and computers are allowed to do.

| Tool | When you use it |
| --- | --- |
| **Local Group Policy Editor** (`gpedit.msc`) | Policies on this one computer |
| **Group Policy Management Console** (`gpmc.msc`) | Central policies in an Active Directory domain |

Local Computer Policy splits into **Computer Configuration** and **User Configuration**. Under User Configuration → Administrative Templates, desktop settings can hide or disable desktop items so a user logs on to an empty desktop.

## Side-by-Side Comparison

| Need | Tool |
| --- | --- |
| One screen with several admin tools | MMC + snap-ins |
| “What failed yesterday?” | Event Viewer (filter the log) |
| See partitions and file systems | Disk Management |
| Run a job every morning | Task Scheduler |
| Bad or missing driver | Device Manager |
| Which CAs does this PC trust? | Certificate Manager |
| Add a local user or group | Local Users and Groups |
| CPU was high last night | Performance Monitor |
| Lock down one PC’s desktop | `gpedit.msc` |
| Lock down many domain PCs | `gpmc.msc` |

## Key Terms

| Term | Meaning |
| --- | --- |
| MMC | Microsoft Management Console — a shell for admin tools |
| Snap-in | A tool you add into an MMC console |
| Event Viewer | Windows log viewer |
| VSS | Volume Shadow Copy Service |
| Disk Management | View and change disks and partitions |
| BitLocker | Full-disk encryption |
| Task Scheduler | Runs programs on a schedule |
| Device Manager | Hardware and driver status |
| Certificate Manager | View and manage certificates |
| Local Users and Groups | Local accounts and groups on this PC |
| Performance Monitor | Long-term resource graphs and alerts |
| gpedit / gpmc | Local policy editor vs domain Group Policy console |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Build a custom admin toolkit | `mmc` and add snap-ins |
| Application log shows an error | Event Viewer — filter it |
| EFI and recovery partitions have no drive letter | Normal — OS startup/recovery partitions |
| Shrink or extend C: | Disk Management — back up first |
| Run a cleanup every night | Task Scheduler |
| Update or disable a driver | Device Manager |
| Trusted root CAs | Certificate Manager |
| Problem already ended | Performance Monitor, not only Task Manager |
| Policy for this PC only | Local Group Policy Editor |
| Policy for the whole domain | Group Policy Management Console |

## Common Mix-Ups

### MMC is one of the tools, like Event Viewer

MMC is the **container**. Event Viewer, Disk Management, and the others are snap-ins you add.

### Task Manager and Performance Monitor do the same job

Task Manager is a short live view. Performance Monitor keeps history so you can study a problem after it ends.

### Local Users and Groups edits Active Directory

It edits **local** accounts. Domain-wide identity and policy use Active Directory and Group Policy Management.

### Every partition should have a drive letter

Recovery and EFI partitions are often hidden on purpose.

## Quick Review

| Topic | Remember |
| --- | --- |
| MMC | Empty console; add snap-ins; save it |
| Logs | Event Viewer — filter Application, Security, Setup, System |
| Disks | Disk Management — backup before you change partitions |
| Schedule | Task Scheduler — triggers, actions, conditions |
| Drivers | Device Manager — usually OS-specific |
| Certificates | Certificate Manager — trusted root CAs |
| Accounts | Local users and groups |
| History | Performance Monitor for long-term counters and alerts |
| Policy | `gpedit.msc` local; `gpmc.msc` domain |

---

## Continue Learning

- Previous Topic: [Task Manager](task-manager.md)
- Next Topic: [Additional Windows Tools](additional-windows-tools.md)
- Related: [The Windows Control Panel](the-windows-control-panel.md)
- Back to [Domain 1 — Operating Systems](README.md)
- Course Map: [Core 2 Study Path](../COURSE-MAP.md)
