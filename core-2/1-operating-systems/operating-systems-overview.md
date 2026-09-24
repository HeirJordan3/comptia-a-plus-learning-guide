# Operating Systems Overview

CompTIA A+ Core 2 — 220-1202  
Objective 1.1 — Explain common operating system (OS) types and their purposes

## What You Need to Know

By the end of this lesson, you should understand:

- What an OS does between hardware and applications
- Common jobs every OS shares (files, apps, I/O, utilities)
- **Windows**, **Linux**, **macOS**, and **Chrome OS** strengths and tradeoffs
- **iOS / iPadOS** vs **Android**
- End-of-life, updates, and cross-OS compatibility limits

## What Is It?

An **operating system (OS)** is the software that sits between your hardware and your apps. It moves data between storage and memory, works with the CPU, handles keyboard/display I/O, and is the platform apps are written for.

## Why Does It Matter?

Every computing device you support — PC, laptop, tablet, phone — needs an OS. Help desk work means knowing:

- Which OS family you’re on
- What that OS is good (and bad) at
- What can move between OSes (documents) vs what cannot (executables)

## Real-World Analogy

Think of hardware as a stage and apps as performers:

| Piece | Role |
| --- | --- |
| Hardware | Stage, lights, sound system |
| Operating system | Stage manager — cues everything |
| Applications | Performers who only know *this* stage’s rules |

A Windows “performer” (`.exe`) cannot simply walk onto a Linux stage.

## How It Works

### What Every OS Handles

| Job | Examples |
| --- | --- |
| File management | Store, remove, change files on disk |
| Application support | Memory use, swap/paging to disk |
| Input / output | Keyboard, mouse, display, printer, external drives |
| System utilities | Tools that keep the OS running efficiently |

Humans put data in → OS processes it → output comes back out.

### Microsoft Windows

| Strength | Challenge |
| --- | --- |
| Huge market presence in orgs | Big target for attackers |
| Strong industry support (hardware, software, help) | Driver quality varies by manufacturer |
| Many versions (Windows 10/11, Windows Server, etc.) for different needs | Supporting diverse hardware long-term |
| Huge app ecosystem (business, entertainment, utilities) | Must balance with large security industry protecting it |

Desktop feel (e.g. Windows 11): app icons, taskbar, status info, Recycle Bin — patterns you’ll recognize on other OSes too.

### Linux

| Strength | Challenge |
| --- | --- |
| **Free / open source** — community maintained | No single “Linux company” for support — community-based |
| Many **distributions** (task-specific or general) | New hardware/drivers may lag |
| Runs on almost any hardware | Pick the distro that fits your need |
| No OS license purchase / monthly OS fee | Support quality depends on community knowledge |

Desktop looks familiar (icons, taskbar — often on the side, movable).

**Windows vs Linux install idea:** Every Windows 11 install is the same product family; Linux comes in different distros for different purposes.

### Apple macOS

| Strength | Challenge |
| --- | --- |
| Ease of use / strong UI | Runs **only on Apple hardware** |
| Apple builds hardware + OS → high compatibility | Higher initial hardware cost |
| Security-minded design; often fewer mainstream concerns than Windows | Smaller user base → less industry support than Windows |

Desktop layout is still familiar: workspace, dock/bar for apps, icons/buttons.

### Google Chrome OS

| Trait | Detail |
| --- | --- |
| Basis | Built by Google; based on the **Linux kernel**, different look/feel from traditional Linux |
| Focus | OS revolves around the **Chrome browser** — most apps run in the browser |
| Design | Straightforward, low overhead; many Chromebook-style laptops |
| Requirement | Needs **network / cloud connectivity** for most cloud apps — limited without a connection |

### Apple iPadOS and iOS

| OS | Hardware | Notes |
| --- | --- | --- |
| **iPadOS** | iPad | Desktop-class browser (Safari variant), Sidecar (second monitor), keyboard, multitasking |
| **iOS** | iPhone | Related look, **different OS** from iPadOS |

Apple OSes are **closed source** and run only on Apple hardware.

| App development | Detail |
| --- | --- |
| SDK | Apple’s Software Developer Kit runs on **macOS** |
| Distribution | Apps tested/approved by Apple → App Store |

### Google Android

| Trait | Detail |
| --- | --- |
| Maintainers | Open Handset Alliance consortium |
| Model | **Open source**, Linux-based |
| Hardware | Many manufacturers and device types |
| Development | Android SDK on Windows, macOS, or Linux |
| Distribution | Google Play and third-party stores |

### Lifecycle, Updates, and Compatibility

| Topic | Remember |
| --- | --- |
| **End of life (EOL)** | Vendors set different EOL rules (Apple ≠ Microsoft timelines) |
| **Updates** | Keep OS current for efficiency **and** security patches |
| **Data compatibility** | Documents, spreadsheets, media often move across OSes |
| **App compatibility** | Executables are OS-specific (Windows app ≠ Linux app) |
| **Workarounds** | Shared file formats; many apps are **web-based** (any browser) |

## Side-by-Side Comparison

| OS | Best known for | Watch-outs |
| --- | --- | --- |
| Windows | Ubiquity, apps, support | Attack target; driver variance |
| Linux | Free, flexible distros | Community support; driver lag |
| macOS | Usability; Apple HW+OS fit | Apple-only; cost; smaller market |
| Chrome OS | Browser/cloud simplicity | Needs connectivity |
| iOS / iPadOS | Apple mobile ecosystem | Closed; Apple HW; App Store rules |
| Android | Many devices; open | Fragmentation across OEMs |

## Key Terms

| Term | Meaning |
| --- | --- |
| Operating system | Software linking hardware and applications |
| Distribution (distro) | A packaged flavor of Linux |
| Open source | Source available; community-maintained (e.g. Linux, Android) |
| Closed source | Source not publicly available (e.g. Apple OSes, Windows) |
| Chrome OS | Google OS centered on the Chrome browser |
| Sidecar | iPadOS feature for using a second display |
| EOL | End of life — vendor stops supporting the product |
| Executable | OS-specific runnable program file |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Software between hardware and apps | Operating system |
| Free OS with many flavors | Linux distributions |
| OS only on Apple Macs | macOS |
| Mostly browser apps; needs internet | Chrome OS |
| iPhone OS vs iPad OS | iOS vs iPadOS (related, not identical) |
| Many phone brands, Linux-based | Android |
| Can’t run `.exe` on Linux | Apps are OS-specific |
| Docs open on Mac and Windows | Data formats can cross OS; apps may not |
| Vendor stops patches | End of life |

## Common Mix-Ups

### Linux = one single OS install like Windows 11

Linux is many **distributions**.

### iOS and iPadOS are the same OS

Similar family, **different** OS per device class.

### Chrome OS is “just Linux desktop”

Linux kernel underneath; UX is browser-first Chrome OS.

### Any app runs anywhere if you copy the file

**Data** often moves; **executables** usually do not.

## Quick Review

| Topic | Remember |
| --- | --- |
| OS job | Hardware ↔ apps; files, memory, I/O, utilities |
| Windows | Popular, supported, targeted |
| Linux | Free, distros, community support |
| macOS | Apple hardware only; polished UI |
| Chrome OS | Browser/cloud; needs network |
| Mobile | iOS/iPadOS closed Apple; Android open multi-OEM |
| Lifecycle | Updates + vendor EOL |
| Compatibility | Data yes; native executables no |

---

## Continue Learning

- Next Topic: [File Systems](file-systems.md)
- Related: [Domain 4 — Operational Procedures](../4-operational-procedures/README.md)
- Back to [Domain 1 — Operating Systems](README.md)
- Course Map: [Core 2 Study Path](../COURSE-MAP.md)
