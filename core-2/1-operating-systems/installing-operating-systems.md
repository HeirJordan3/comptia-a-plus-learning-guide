# Installing Operating Systems

CompTIA A+ Core 2 — 220-1202  
Objective 1.2 — Installing Operating Systems

## What You Need to Know

By the end of this lesson, you should understand:

- Common boot methods for OS installs (USB, PXE, local drives, internet, ISO)
- Clean install vs in-place upgrade vs image / remote install
- What zero-touch deployment is
- GPT vs MBR partition styles
- Quick format vs full format

## What Is It?

Installing an OS creates a chicken-and-egg problem: how do you install an OS if none is on the computer yet?

The usual answer is to boot into a bare-bones installer from removable media, network, recovery, or an image — then choose how to install, partition, and format the disk.

## Why Does It Matter?

Help desk and field techs reinstall and deploy systems constantly:

- New laptop setup
- Broken OS repair
- Multi-boot Windows + Linux
- Company image rollout with no hands-on prompts

Knowing boot methods, install types, and partition/format choices prevents data loss and failed deployments.

## Real-World Analogy

Think of installing an OS like furnishing an empty house:

- **Boot method** = how you get into the house when the keys are missing
- **Clean install** = gut renovation
- **In-place upgrade** = remodel while keeping furniture
- **Image / zero-touch** = company-standard furniture package delivered and set up automatically
- **Partition / format** = dividing rooms and installing flooring before you move in

## How It Works

### Boot Methods

| Method | Idea |
| --- | --- |
| Bootable USB | Flash drive made bootable; motherboard must support USB boot |
| PXE (“pixie”) | Preboot Execution Environment — network boot to a PXE server |
| Internal / external SSD or HDD | Bootable drive holding install files |
| Internet install | Minimal download, then pull remaining files online (some Linux distros; macOS recovery; Windows update/install sources) |
| Optical / ISO | CD/DVD style installs; ISO is a disk image of that media |
| Local partition | Install files on one partition; install OS to another |

**PXE notes:** BIOS must support PXE. At startup, the system looks on the local network for a PXE server and boots the installer as if it were local media.

**ISO notes:** Common with virtualization. Some external drives can mount an ISO so it looks like a physical disk you can move between computers.

**Multi-boot:** More than one OS on the same device (for example Windows and Linux). Choose which OS to start at boot.

### Installation Options

| Option | Meaning |
| --- | --- |
| Clean install | Wipe the partition and reinstall from scratch; old files do not remain |
| In-place upgrade | Newer OS version while keeping apps and data |
| Image deployment | Build one configured system, capture an image, deploy that image to many PCs |
| Remote network install | Install files live on a network share/server — no local USB/DVD needed |
| Recovery partition | Hidden partition with OS install files for later repair/reinstall |
| Repair installation | Overwrite OS files but keep user files/documents; used when other fixes fail |

During install you may be prompted for **third-party drivers** (storage, network, etc.) so the installer can see the hardware it needs.

Image deployments can be fully automated end-to-end with no human clicks.

### Zero-Touch Deployment

**Zero-touch deployment** is an automated install with little or no user prompting.

It can apply company settings such as:

- Email server configuration
- Domain connections
- Other organization-specific setup

Typical flow: user opens a new laptop, turns it on, waits. Scripts configure the system so the user can work immediately — even if the device was shipped worldwide after reimaging.

### Disk Partitions and Volumes

A **disk partition** is a logical section of a drive set aside for data.

Notes from the lesson:

- Some OSes prefer multiple partitions; others use one large partition
- Recovery partitions are often created automatically and may be hidden
- Multi-boot setups commonly use separate partitions per OS
- In Windows docs, a **volume** is a formatted partition

### GPT vs MBR

When you format/initialize a disk, you choose a partition style.

#### GPT — GUID Partition Table

| Trait | Detail |
| --- | --- |
| Name | Globally Unique Identifier Partition Table |
| Typical use | Modern OS installs |
| BIOS need | UEFI BIOS |
| Partition count | Up to **128** partitions |
| Drive size support | Extremely large (lesson: over 9,000,000,000 TB capacity idea) |
| Windows GPT limit | Currently **256 TB** max GPT partition size (per lesson) |

GPT treats partitions more simply than MBR’s extended/logical model — up to 128 similar partitions.

#### MBR — Master Boot Record

Older style still found on legacy devices.

| Trait | Detail |
| --- | --- |
| Max partition size | **2 TB** |
| Primary partitions | Up to **4** per drive |
| Bootable partitions | Only **primary** partitions are bootable |
| Active partition | Only one marked active/bootable at a time |
| Extended partition | Optional; holds **logical** partitions (not bootable) |

If you need more than four partitions on MBR, use one extended partition and create logical partitions inside it. Bootable OSes still need primary partitions.

#### BIOS Compatibility Mode Warning

GPT needs UEFI. BIOS compatibility mode was common during the BIOS→UEFI transition, but enabling it **disables Secure Boot**, and many newer OSes will not work well in that mode.

### Quick Format vs Full Format

After creating a partition, format it before storing data.

| Format type | What it does | Trade-off |
| --- | --- | --- |
| Quick format | Creates a new file table; no full physical drive check | Fast; old data may still be recoverable |
| Full format | Writes zeros across the disk; erases prior contents more thoroughly | Much slower; more secure wipe |

Windows 10/11 setup defaults to **quick format**. Use **diskpart** if you need a full format during that process.

**Caution:** Creating or deleting partitions can destroy data. Be sure you selected the correct drive/partition.

## Key Terms

| Term | Meaning |
| --- | --- |
| PXE | Preboot Execution Environment; network boot |
| ISO | Disk image of optical install media |
| Clean install | Wipe and reinstall |
| In-place upgrade | Upgrade OS while keeping apps/data |
| Image deployment | Clone a prepared system image to many devices |
| Zero-touch deployment | Automated install with little/no user input |
| Recovery partition | Hidden partition with OS install files |
| Repair installation | Replace OS files; keep user data |
| Partition | Logical section of a disk |
| Volume | Formatted partition (Windows term) |
| GPT | Modern GUID partition table style |
| MBR | Older master boot record style |
| Primary / extended / logical | MBR partition types |
| Quick / full format | Fast file-table reset vs thorough zeroing |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Boot from network install server | PXE |
| USB flash OS installer | Bootable USB |
| Keep apps and files, newer Windows | In-place upgrade |
| Wipe everything and start over | Clean install |
| Same configured image on many PCs | Image deployment |
| User turns on laptop; scripts finish setup | Zero-touch |
| UEFI + up to 128 partitions | GPT |
| Max 4 primary / 2 TB limit | MBR |
| Logical partitions inside extended | MBR extended |
| Fast format, default in Win 10/11 setup | Quick format |
| Write zeros / more secure erase | Full format |

## Common Mix-Ups

### Clean install vs repair install

- Clean = start over; previous files gone
- Repair = replace OS files; user files usually stay

### GPT vs MBR

- GPT = modern, UEFI, many partitions, huge disks
- MBR = legacy, 2 TB limit, 4 primary max

### Extended vs primary (MBR)

Only primary is bootable. Extended holds non-bootable logical partitions.

### Quick vs full format

Quick is fast but not a secure wipe. Full is slower and more thorough.

## Quick Review

| Topic | Remember |
| --- | --- |
| Boot methods | USB, PXE, drive, internet, ISO, local partition |
| Install types | Clean, upgrade, image, remote, repair |
| Zero-touch | Automated company deployment |
| GPT | UEFI, up to 128 partitions |
| MBR | 2 TB, 4 primary, extended/logical |
| Formats | Quick = fast; full = zeros / more secure |

---

## Continue Learning

- Previous Topic: [File Systems](file-systems.md)
- Next Topic: [Upgrading Windows](upgrading-windows.md)
- Related: [An Overview of Windows](an-overview-of-windows.md)
- Back to [Domain 1 — Operating Systems](README.md)
- Back to [Core 2](../README.md)
