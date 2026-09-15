# An Overview of Windows

CompTIA A+ Core 2 — 220-1202  
Objective 1.3 — Microsoft Windows

## What You Need to Know

By the end of this lesson, you should understand:

- Why CompTIA expects knowledge of both Windows 10 and Windows 11
- Key differences between Home, Pro, Pro for Workstations, and Enterprise editions
- Which features require Pro/Enterprise (domain join, BitLocker, RDP host, Group Policy)
- Windows 11 changes such as 64-bit only and UI updates
- What Windows N editions are used for in Europe

## What Is It?

For Core 2, focus on **Windows 10** and **Windows 11**.

CompTIA’s objectives treat in-support Windows versions as exam-relevant. Microsoft has commonly supported Windows for about five years after release. CompTIA specifically expects familiarity with both Windows 10 and Windows 11.

Good news: the two versions are very similar. If you know Windows 10, Windows 11 feels familiar. There is no Windows 9 — Microsoft went from Windows 8 to Windows 10.

## Why Does It Matter?

Help desk techs must know which edition a user has:

- “Why can’t I join the domain?”
- “BitLocker isn’t available.”
- “Can this PC be an RDP host?”
- “Is this Home or Pro?”

Edition choice controls management, security, and enterprise features.

## Real-World Analogy

Think of Windows editions like phone plans:

- **Home** = consumer plan with basics
- **Pro** = business plan with remote work and security extras
- **Pro for Workstations / Enterprise** = heavy-duty business plans with more capacity and admin controls

Same phone family — different feature unlocks.

## How It Works

### Windows 10 Snapshot

Windows 10 was designed as a broad platform across many devices. Across its life cycle there were more than 15 released versions, ending with **21H2** (November 2021).

Microsoft stated that Windows 10 Home and Pro support ends on **October 14, 2025**. Organizations may still run Windows 10 after that date, even without official support.

#### Windows 10 Home

Built for home / retail PCs.

Includes:

- Microsoft account integration
- OneDrive backup integration
- Windows Defender antivirus / anti-malware
- Cortana voice interaction

#### Windows 10 Pro

Built for business.

Adds features not in Home, including:

- Remote Desktop **host** support (others can connect in)
- Full Disk Encryption with **BitLocker**
- Windows **domain join**

#### Windows 10 Pro for Workstations

High-end workstation edition.

Supports:

- Up to **four** physical CPUs
- Up to **6 TB** RAM
- **ReFS** (Resilient File System), also used in Windows Server

#### Windows 10 Enterprise

For large organizations with volume licensing.

Includes advanced management features such as:

- **AppLocker** — allow/block specific applications
- **BranchCache** — cache data at remote sites to reduce WAN use
- Granular **UX control** — control what users see on the desktop

### Windows 10 Feature Comparison

| Feature | Home | Pro | Pro for Workstations | Enterprise |
| --- | --- | --- | --- | --- |
| Domain join | No | Yes | Yes | Yes |
| BitLocker | No | Yes | Yes | Yes |
| Remote Desktop | Client only | Client + host | Client + host | Client + host |
| Group Policy management | No | Yes | Yes | Yes |
| Max RAM (32-bit) | 4 GB | 4 GB | 4 GB | 4 GB |
| Max RAM (64-bit idea from lesson) | 128 GB | 2 TB | 6 TB | 6 TB |

### Windows 11 Snapshot

Windows 11 released in **October 2021**.

Major changes from the lesson:

- **No 32-bit CPU support** — 64-bit only
- New UI: Start menu and taskbar widgets
- Microsoft Teams integration
- New snap layouts
- Better tablet / touch integration
- Windows Copilot AI integration

#### Windows 11 Home

Consumer edition.

- Microsoft account or local account
- Limited management (no typical AD home environment)
- **Device Encryption** for consumers (BitLocker-like)
  - Recovery info stored in the user’s **Microsoft account**
  - Enterprise BitLocker recovery is commonly stored in Active Directory instead

#### Windows 11 Pro

Office / organization edition.

- Active Directory integration / central management
- BitLocker full disk encryption
- Hyper-V virtualization
- Remote Desktop as client **and** host

#### Windows 11 Enterprise

Volume-licensed large-org edition.

- Extra management via **MDM** and **MAM**
- Supports **ReFS** (unlike other Windows 11 editions in the lesson)

### Windows 11 Feature Comparison

| Feature | Home | Pro | Enterprise |
| --- | --- | --- | --- |
| Domain join | No | Yes | Yes |
| BitLocker | No (Device Encryption instead) | Yes | Yes |
| Remote Desktop | Client only | Client + host | Client + host |
| Group Policy management | No | Yes | Yes |
| 32-bit version | None | None | None |
| Max RAM (from lesson) | 128 GB | 2 TB | 6 TB |
| ReFS | No | No | Yes |

### Windows N Editions (Europe)

**Windows N** editions ship **without media player / multimedia utilities**.

- No Windows Media Player
- No other built-in multimedia utilities in the N edition

You can add them later with the **Media Feature Pack for N edition**:

**Settings → Apps → Optional Features → Add an optional feature → Media Feature Pack**

## Key Terms

| Term | Meaning |
| --- | --- |
| Windows 10 / 11 | Core 2 exam Windows versions |
| Home / Pro / Enterprise | Common Windows edition levels |
| Pro for Workstations | High-CPU / high-RAM Windows 10 edition |
| BitLocker | Microsoft full disk encryption |
| Device Encryption | Consumer encryption in Windows 11 Home |
| Domain join | Connect PC to a Windows domain |
| RDP host | Allow inbound Remote Desktop connections |
| AppLocker | Control which apps can run (Enterprise) |
| BranchCache | Remote-site caching to reduce WAN traffic |
| ReFS | Resilient File System |
| Windows N | Europe editions without media features |
| Media Feature Pack | Optional pack that restores N-edition media features |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Exam Windows versions | Windows 10 and Windows 11 |
| Retail home PC edition | Home |
| Domain join / BitLocker / RDP host | Pro or higher |
| Four CPUs / 6 TB RAM / ReFS on Win 10 | Pro for Workstations |
| AppLocker / BranchCache / UX control | Enterprise |
| No 32-bit Windows 11 | 64-bit only |
| Win 11 Home encryption | Device Encryption + Microsoft account recovery |
| Europe edition without media player | Windows N |
| Add media features to N edition | Media Feature Pack |

## Common Mix-Ups

### Home vs Pro

Home cannot join a domain and lacks BitLocker / RDP host / Group Policy management.

### Device Encryption vs BitLocker

Similar consumer vs enterprise encryption approaches. Recovery location differs (Microsoft account vs typically Active Directory).

### Windows 10 vs Windows 11 architecture

Windows 11 drops 32-bit CPU support entirely.

### “Windows N is a different OS”

N is an edition without media features — not a separate product line.

## Quick Review

| Edition idea | Remember |
| --- | --- |
| Home | Consumer; limited enterprise features |
| Pro | Domain, BitLocker, RDP host, Group Policy |
| Pro for Workstations | High hardware limits + ReFS (Win 10) |
| Enterprise | Volume licensing + advanced management |
| Windows 11 | 64-bit only; new UI / Teams / Copilot |
| Windows N | No media features until Media Feature Pack |

---

## Continue Learning

- Previous Topic: [Upgrading Windows](upgrading-windows.md)
- Next Topic: [Windows Features](windows-features.md)
- Related: [File Systems](file-systems.md)
- Back to [Domain 1 — Operating Systems](README.md)
- Back to [Core 2](../README.md)
