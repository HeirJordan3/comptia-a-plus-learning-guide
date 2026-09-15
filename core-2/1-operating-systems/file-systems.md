# File Systems

CompTIA A+ Core 2 — 220-1202  
Objective 1.1 — Operating Systems

## What You Need to Know

By the end of this lesson, you should understand:

- Why partitions must be formatted with a file system
- What NTFS and ReFS are used for
- FAT / FAT32 and exFAT limits and use cases
- Where ext4 and XFS appear (Linux / Android / data centers)
- What APFS is and where Apple uses it

## What Is It?

A **file system** is the structure an operating system uses to read and write data on a partition.

When you install an OS, you usually:

1. Create a partition
2. Format that partition with a file system

Different OSes often use different file systems. Some file systems work across platforms — for example **FAT32**, **NTFS**, and **exFAT** can be used with Windows, Linux, and macOS.

## Why Does It Matter?

Help desk technicians deal with file system choices when:

- Installing or reinstalling an OS
- Preparing USB flash drives
- Moving files between Windows, macOS, and Linux
- Supporting large server storage volumes

Choosing the wrong file system can mean size limits, missing features, or read/write problems.

## Real-World Analogy

Think of a partition like an empty warehouse.

- Creating the partition = building the warehouse shell
- Formatting with a file system = installing the shelving, labels, and inventory system

Without that system, you cannot store and find packages reliably.

## How It Works

### NTFS — NT File System

On Windows, the common file system is **NTFS**.

It was effectively an upgrade from **FAT32** and adds features such as:

- Compression
- File encryption
- Quotas
- Other management features

Because Windows is so popular, many other OSes can work with NTFS. Some can read but not write NTFS. Modern Linux and macOS often can read and write NTFS partitions.

### ReFS — Resilient File System

**ReFS** is Microsoft’s next-generation file system and an upgrade path beyond NTFS ideas.

Notes from the lesson:

- Available with certain integration in **Server 2012 and later**
- Modern Windows desktops may have **limited** ReFS support
- Built for large data arrays / huge partitions
- Emphasizes resiliency: self-checking and self-repair
- Reduces the need to run Check Disk-style tools for integrity
- Includes RAID-type functionality for redundant storage

ReFS is **not widely installed** yet, and Microsoft continues updating it.

### FAT / FAT32

**FAT** (File Allocation Table) is an older cross-platform file system. Systems still using it today are usually on **FAT32**.

FAT32 limits from the lesson:

| Limit | Value |
| --- | --- |
| Max volume size | 2 TB |
| Max file size | 4 GB |

Larger modern storage often needs a different file system than FAT32.

### exFAT — Extended File Allocation Table

**exFAT** was created by Microsoft for **flash drive** storage.

Common use: plug in a USB drive, copy files, remove it, and use it on another computer.

Advantages:

- Supports files larger than FAT32’s 4 GB limit
- Works across many OSes (Windows, Linux, macOS)

### ext4

**ext4** is the fourth extended file system, common on:

- Linux
- Android devices

If you are using an Android phone, you are probably using ext4.

### XFS

**XFS** is a high-performance Linux file system used in many data centers.

Designed for:

- Very large data workloads
- High-speed processing
- Efficient storage of massive amounts of data

Extra strengths from the lesson:

- **Journaling** to help reduce corruption if reads/writes are interrupted
- Low fragmentation for better spinning-HDD performance

### APFS — Apple File System

**APFS** is Apple’s file system.

Available since macOS **10.12.4**, and also used on **iOS** and **iPadOS**.

Designed to optimize SSDs and includes:

- Built-in encryption
- Fast snapshot save/restore
- Increased data integrity features

## File System Snapshot

| File system | Common home | Remember |
| --- | --- | --- |
| NTFS | Windows | Feature-rich; widely readable |
| ReFS | Windows Server / limited desktop | Resilient, large volumes |
| FAT32 | Older / cross-platform | 2 TB volume / 4 GB file limits |
| exFAT | USB flash drives | Larger files; cross-OS friendly |
| ext4 | Linux / Android | Common extended Linux FS |
| XFS | Linux servers / data centers | High performance + journaling |
| APFS | macOS / iOS / iPadOS | SSD-focused Apple FS |

## Key Terms

| Term | Meaning |
| --- | --- |
| Partition | Disk section prepared for storage |
| Format | Applies a file system to a partition |
| NTFS | Common Windows file system |
| ReFS | Microsoft resilient next-gen file system |
| FAT / FAT32 | Older File Allocation Table systems |
| exFAT | Extended FAT for flash media |
| ext4 | Common Linux/Android extended file system |
| XFS | High-performance Linux file system |
| APFS | Apple File System |
| Journaling | Helps recover cleanly after interrupted writes |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Default modern Windows file system | NTFS |
| Compression, encryption, quotas on Windows | NTFS |
| Self-healing / large resilient Windows volumes | ReFS |
| USB flash drive for many OSes / big files | exFAT |
| 4 GB max file size limit | FAT32 |
| Android / common Linux FS | ext4 |
| High-performance Linux data center FS | XFS |
| macOS / iPhone / iPad file system | APFS |

## Common Mix-Ups

### FAT32 vs exFAT

- FAT32 = older limits (4 GB max file)
- exFAT = better for modern flash drives and larger files

### NTFS vs ReFS

- NTFS = standard Windows choice today
- ReFS = newer resilient option, especially server-oriented, not widely deployed yet

### ext4 vs XFS

Both are Linux-side options. ext4 is common/general; XFS targets high-performance large-data use.

### Cross-OS compatibility

FAT32, NTFS, and exFAT are the cross-platform examples from the lesson — but feature support can still differ by OS.

## Quick Review

| FS | Remember |
| --- | --- |
| NTFS | Windows standard + features |
| ReFS | Resilient / large / self-checking |
| FAT32 | Old, limited sizes |
| exFAT | Flash drives, big files, portable |
| ext4 | Linux / Android |
| XFS | Fast Linux / big data |
| APFS | Apple SSD-optimized |

---

## Continue Learning

- Previous Topic: [Operating Systems Overview](operating-systems-overview.md)
- Next Topic: [Installing Operating Systems](installing-operating-systems.md)
- Back to [Domain 1 — Operating Systems](README.md)
- Back to [Core 2](../README.md)
