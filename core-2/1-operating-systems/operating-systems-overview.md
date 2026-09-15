# Operating Systems Overview

CompTIA A+ Core 2 — 220-1202  
Objective 1.1 — Operating Systems

## What You Need to Know

By the end of this lesson, you should understand:

- What an operating system does
- Common OS responsibilities shared across platforms
- Strengths and trade-offs of Windows, Linux, and macOS
- What Chrome OS is designed for
- Differences between Apple iOS / iPadOS and Google Android
- End-of-life, updates, and cross-OS compatibility basics

## What Is It?

An **operating system (OS)** is the software link between hardware and applications.

It controls how the device:

- Moves data between storage and memory
- Interacts with the CPU
- Handles input and output (keyboard, display, and more)

Applications are written for a specific OS. The OS is also the platform humans use to put information in, process it, and get output back.

## Why Does It Matter?

Help desk technicians support many OS platforms every day:

- Windows desktops and laptops
- macOS machines
- Linux systems
- Chromebooks
- iPhones, iPads, and Android phones/tablets

Knowing what each OS is good at — and where the limits are — helps you choose, support, and troubleshoot the right platform.

## Real-World Analogy

Think of the OS like a restaurant kitchen manager:

- Hardware = stoves, fridges, and tools
- Applications = recipes/orders
- The OS = the manager who coordinates tools, staff, and workflow so orders get completed

Different restaurants (Windows, macOS, Linux, mobile OSes) have different kitchens and rules, even if they all serve food.

## How It Works

### Common OS Jobs

Across operating systems, you usually find:

| Responsibility | Meaning |
| --- | --- |
| File management | Store, change, and remove files on storage |
| Application support | Run apps and manage memory / swap as needed |
| Input / output | Keyboards, mice, displays, printers, drives |
| OS utilities | Tools that help keep the system running well |

### Microsoft Windows

Windows has a huge market presence and is used in nearly every organization.

Versions you may see:

- Windows 10
- Windows 11
- Windows Server
- Newer Windows releases over time

Strengths:

- Large industry support
- Many OS options for home, business, and servers
- Huge software catalog for business, entertainment, and utilities

Trade-offs:

- Big target for attackers because it is so popular
- Hardware makers must write drivers; quality varies
- Long-term hardware support can be uneven across manufacturers

Windows desktops commonly show app icons, a taskbar, status info, and a recycle bin.

### Linux

Linux is **free** and **open source**, maintained by thousands of people worldwide.

Unlike one fixed Windows 11 image, Linux has many **distributions** (distros) for specific tasks or general use. Pick the distro that fits your needs.

Strengths:

- No purchase cost / no monthly OS fee
- Works on a wide range of hardware
- Large community support

Trade-offs:

- Newer hardware may not be fully compatible yet
- Drivers can be harder to find
- No single “Linux company” help desk — support is community-based

Linux desktops often look familiar: icons, a taskbar (sometimes on the side), search, and buttons similar to Windows/macOS.

### Apple macOS

**macOS** runs on **Apple hardware only**.

Strengths:

- Strong ease of use / polished interface
- Apple builds the hardware and OS together → high compatibility
- Security-focused design; often fewer security concerns than Windows/Linux in the lesson’s framing

Trade-offs:

- Cannot install on non-Apple PCs
- Smaller user base than Windows → less industry support volume
- Higher initial hardware cost

The macOS desktop still feels familiar: workspace, dock/bar for apps, icons, and buttons.

### Google Chrome OS

**Chrome OS** is from Google. It is based on the Linux kernel but feels different from traditional Linux desktops.

Design goals:

- Browser-centered (Google Chrome)
- Most apps run inside the browser
- Lightweight, lower overhead
- Common on laptop-style hardware from many manufacturers

Important limit:

- Heavy dependence on network/cloud connectivity
- Without connectivity, many cloud apps will not work

### Apple iPadOS and iOS

Apple tablet and phone platforms are **closed source** and run only on Apple hardware.

**iPadOS** (tablets) includes features such as:

- Desktop-style Safari browser (different from iPhone Safari)
- Sidecar for a second monitor
- Keyboard support
- Multitasking and other tablet-focused features

**iOS** runs on iPhones. It looks related, but it is a different OS from iPadOS.

App development notes from the lesson:

- Build apps with Apple’s Software Development Kit on macOS
- Apps must be tested and approved by Apple before App Store release

### Google Android

**Android** is maintained through the Open Handset Alliance and is **open source**, based on Linux.

Strengths:

- Runs on hardware from many manufacturers
- Wide device variety
- Apps can be built on Windows, macOS, or Linux with the Android SDK
- Apps can ship via Google Play and some third-party stores

### Updates, End of Life, and Compatibility

Different vendors set different **end-of-life** timelines (Apple vs Microsoft, for example).

Across OSes, you still need regular updates for:

- Performance
- Security patches

Data compatibility:

- Documents, spreadsheets, media, and many standard files can move between OSes
- A Windows **executable** will not run on Linux (or other OSes) unless written for that OS
- Many apps are now web-based and can run in a browser on almost any OS

## Key Terms

| Term | Meaning |
| --- | --- |
| Operating system (OS) | Software that manages hardware and runs applications |
| Windows | Popular Microsoft OS family for PCs and servers |
| Linux | Free open-source OS with many distributions |
| Distribution (distro) | A packaged version of Linux for specific needs |
| macOS | Apple desktop/laptop OS; Apple hardware only |
| Chrome OS | Google OS centered on the Chrome browser / cloud apps |
| iOS | Apple iPhone operating system |
| iPadOS | Apple iPad operating system |
| Android | Google open-source mobile OS based on Linux |
| Closed source | Source code not publicly available |
| Open source | Source code available; community can maintain/modify |
| End of life | Vendor support/update period ends |
| Executable | App binary built for a specific OS |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Link between hardware and apps | Operating system |
| Free open-source PC OS with distros | Linux |
| Huge business market share / many apps | Windows |
| Apple desktop OS only on Apple hardware | macOS |
| Browser/cloud-first laptop OS | Chrome OS |
| iPhone OS / iPad OS | iOS / iPadOS |
| Open-source mobile OS on many brands | Android |
| Windows .exe on Linux | Will not run |
| Docs/media across platforms | Often compatible via standard formats / web apps |

## Common Mix-Ups

### Linux vs Chrome OS

Chrome OS uses a Linux kernel but is built around the browser experience, not a traditional Linux desktop.

### iOS vs iPadOS

Related Apple mobile platforms, but not the same OS.

### Open source vs closed source

- Linux / Android = open source
- Apple OS family = closed source

### Cross-platform files vs cross-platform apps

Files often move. Native executables usually do not.

## Quick Review

| OS | Remember |
| --- | --- |
| Windows | Popular, huge support/software, big attack target |
| Linux | Free, distros, community support |
| macOS | Apple hardware only, polished, pricier hardware |
| Chrome OS | Browser/cloud focused, needs connectivity |
| iOS / iPadOS | Apple mobile; closed source; App Store approval |
| Android | Open source; many manufacturers |

---

## Continue Learning

- Next Topic: [File Systems](file-systems.md)
- Back to [Domain 1 — Operating Systems](README.md)
- Back to [Core 2](../README.md)
