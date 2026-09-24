# File Systems

CompTIA A+ Core 2 — 220-1202  
Objective 1.1 — Explain common operating system (OS) types and their purposes

## What You Need to Know

By the end of this lesson, you should understand:

- Partition → **format** → file system
- Windows: **NTFS**, **ReFS**, **FAT32**, **exFAT**
- Linux/Android: **ext4**, **XFS**
- Apple: **APFS**
- Which file systems work well across OSes (especially USB)

## What Is It?

A **file system** is the structure an OS uses to store and find data on a partition. You create a partition, then **format** it with a file system before you can save files.

## Why Does It Matter?

Wrong file system = wrong limits (file size, volume size), missing features (encryption, snapshots), or a USB stick that won’t write on another computer. Help desk techs pick formats for drives constantly.

## Real-World Analogy

A partition is an empty warehouse. Formatting chooses the **shelving system**:

| File system | Shelving style |
| --- | --- |
| FAT32 | Old, simple shelves — small item limit |
| exFAT | Modern portable shelves for flash drives |
| NTFS | Full Windows warehouse (security, quotas…) |
| ReFS | Self-checking, huge server warehouse |
| ext4 | Default Linux / Android shelving |
| XFS | High-speed data-center shelving |
| APFS | Apple SSD-optimized shelving |

## How It Works

### Partition Then Format

1. Create a **partition** (space for data)  
2. **Format** it with a file system  
3. OS reads/writes using that structure  

Some file systems work across Windows, Linux, and macOS (examples from the video: FAT32, NTFS, exFAT — with read/write caveats depending on OS and tools).

### Windows — NTFS

**NTFS** (NT File System) is the usual Windows system/data file system — an upgrade over FAT32.

| Feature | Benefit |
| --- | --- |
| Compression | Save space |
| Encryption | Protect files |
| Quotas | Limit how much users can store |
| Other management features | Built into the FS |

Widely used because Windows is popular. Other OSes often **read** NTFS; write support varies by OS/version/tools. Modern Linux/macOS can often read and write NTFS (per transcript), but expect environment-specific limits in the real world.

### Windows — ReFS (Resilient File System)

Microsoft’s next-generation FS — positioned as an upgrade path from NTFS.

| Trait | Detail |
| --- | --- |
| Where | Server 2012+ integration; limited support on modern Windows desktops |
| Scale | Very large data arrays / huge partitions |
| Resiliency | Self-repair / integrity checking — less need for Check Disk-style checks |
| Extra | Some RAID-like redundancy concepts built in |
| Reality | Not widely installed yet; still evolving |

Designed for desktop **and** server, with emphasis on integrity and large storage.

### FAT / FAT32

**FAT** (File Allocation Table) is old and cross-platform. Today you’ll usually see **FAT32**.

| Limit | Value |
| --- | --- |
| Max volume (typical teaching figure) | ~2 TB |
| Max file size | **4 GB** |

Modern drives often exceed 2 TB, so FAT32 is a poor choice for large system disks — fine for small/compatible needs.

### exFAT (Extended FAT)

Built by Microsoft for **flash / USB** storage.

| Advantage | Detail |
| --- | --- |
| Large files | Bigger than FAT32’s 4 GB limit |
| Cross-OS | Save on Windows; open on Linux or macOS |
| Use case | Plug-in USB drives |

### Linux / Android — ext4

**ext4** = fourth extended file system — common on **Linux** and **Android** phones.

### Linux — XFS

High-performance Linux file system for data centers and heavy workloads.

| Strength | Why it matters |
| --- | --- |
| Large file system size | Massive data stores |
| Journaling | Less corruption if a write is interrupted |
| Low fragmentation | Better performance on spinning disks |
| Efficient storage | Large data / high-speed processing |

### Apple — APFS

**APFS** (Apple File System) — macOS (from about 10.12.4) plus **iOS** and **iPadOS**.

| Strength | Detail |
| --- | --- |
| SSD-optimized | Built for solid-state storage |
| Encryption | Built in |
| Snapshots | Fast save/restore |
| Integrity | Stronger data integrity features |

## Side-by-Side Comparison

| File system | Typical home | Remember |
| --- | --- | --- |
| NTFS | Windows | Features: compression, encryption, quotas |
| ReFS | Windows Server / limited desktop | Resilient, huge volumes, not everywhere yet |
| FAT32 | Legacy / small media | 4 GB max file |
| exFAT | USB flash drives | Large files + cross-OS |
| ext4 | Linux, Android | Everyday Linux/Android default |
| XFS | Linux servers | Performance + journaling + scale |
| APFS | Apple (Mac + mobile) | SSD, encryption, snapshots |

## Key Terms

| Term | Meaning |
| --- | --- |
| Partition | Slice of disk set aside for data |
| Format | Apply a file system to a partition |
| NTFS | Standard modern Windows file system |
| ReFS | Resilient File System (Microsoft) |
| FAT32 | Older FAT variant; 4 GB file limit |
| exFAT | Extended FAT for flash media |
| ext4 | Common Linux/Android file system |
| XFS | High-performance Linux FS |
| APFS | Apple File System |
| Journaling | Logs writes to reduce corruption on interrupt |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Format after creating a partition | Choosing a file system |
| Windows system drive | NTFS |
| USB stick for Windows + Mac, big video file | exFAT (not FAT32) |
| File won’t copy — over 4 GB — on FAT32 | Hit FAT32 limit → use exFAT/NTFS |
| Self-healing large Windows storage | ReFS |
| Android phone storage FS | Often ext4 |
| Linux high-performance/large data | XFS |
| Mac SSD with snapshots/encryption | APFS |

## Common Mix-Ups

### FAT32 and exFAT are the same

exFAT removes the harsh **4 GB** file limit and targets flash drives.

### ReFS has replaced NTFS everywhere

Still not widely installed; NTFS remains the everyday Windows choice.

### APFS is only for Macs

Also used on **iOS** and **iPadOS**.

### Any OS fully writes every FS the same way

Cross-read is more common than identical full feature write support — know the common portable choices (**exFAT**, sometimes FAT32).

## Quick Review

| Topic | Remember |
| --- | --- |
| Order | Partition → format → file system |
| Windows daily | NTFS |
| Windows future/large resilient | ReFS |
| USB portable | exFAT |
| Old/small limit | FAT32 (4 GB files) |
| Linux phone/desktop | ext4 |
| Linux performance | XFS |
| Apple | APFS |

---

## Continue Learning

- Previous Topic: [Operating Systems Overview](operating-systems-overview.md)
- Next Topic: [Installing Operating Systems](installing-operating-systems.md)
- Back to [Domain 1 — Operating Systems](README.md)
- Course Map: [Core 2 Study Path](../COURSE-MAP.md)
