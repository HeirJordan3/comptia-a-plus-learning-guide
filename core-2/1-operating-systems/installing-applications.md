# Installing Applications

CompTIA A+ Core 2 — 220-1202  
Objective 1.10 — Given a scenario, install and configure applications

## What You Need to Know

By the end of this lesson, you should understand:

- OS and app **32-bit vs 64-bit** rules
- Memory, CPU, storage, and graphics requirements
- Licensing (keys vs hardware tokens)
- Distribution methods (app store, web, physical media, ISO, images)
- Trust and install sources
- Business risks and why **test before deploy**

## What Is It?

**Installing applications** means adding software to a bare OS so users can work — after checking that the PC’s OS version, CPU, RAM, storage, graphics, and license match what the app needs.

## Why Does It Matter?

Wrong bitness, too little RAM, or an untrusted installer causes broken installs, slow systems, or security incidents. In business, one bad app can hit shared files, workflows, and many users — so labs and sandboxes matter.

## Real-World Analogy

Installing an app is like parking a truck in a garage:

| Check | Meaning |
| --- | --- |
| Garage height/width | 32-bit vs 64-bit OS / drivers |
| Floor strength | Enough RAM and CPU |
| Space left | Free disk storage |
| Key vs valet token | License key vs USB hardware dongle |
| Where you bought the truck | Trusted publisher vs random third party |

## How It Works

### Plan Before You Install

Confirm:

- Correct **OS** and version  
- Enough **RAM**, **storage**, and other resources  
- Compatible **CPU** and **graphics**  
- Trusted **source** and valid **license**  

Sources: app store, vendor website, or (when needed) physical media.

### 32-bit vs 64-bit

| Idea | Detail |
| --- | --- |
| Based on | Processor / OS architecture |
| Modern default | Most systems are **64-bit**; Windows 11 is **64-bit only** (no 32-bit Win 11) |
| Memory addressing | 32-bit ≈ 2³² addresses ≈ **4 GB** address space; 64-bit ≈ 2⁶⁴ ≈ huge theoretical space (~17 billion GB) — real OS max is lower; check docs |
| Drivers | Must match OS bitness (32-bit driver on 32-bit OS; 64-bit on 64-bit) |
| Apps on 64-bit Windows | Can run **both** 64-bit and 32-bit apps |
| Apps on 32-bit Windows | **Cannot** run 64-bit apps |

**Where Windows stores apps:**

| App type | Typical folder |
| --- | --- |
| 32-bit | `Program Files (x86)` |
| 64-bit | `Program Files` |

**Check your PC:** Settings → **System → About** — memory, processor, and **system type** (e.g. 64-bit OS, x64-based processor).

### Graphics Requirements

| Type | Meaning |
| --- | --- |
| **Integrated graphics** | GPU on the same chip as the CPU — saves power/space |
| **Discrete graphics** | Separate dedicated GPU card — for 3D, video editing, heavy graphics |

Check the app’s graphics needs before install.

### Memory (RAM)

App docs list minimum/recommended RAM for the **app alone** — not counting the OS and other open programs.

- Too little RAM → poor performance or failure  
- Check **Task Manager** for free memory; upgrade if you’re near the max  

### CPU Speed

Often listed in **GHz** (gigahertz).

- 1 Hz = 1 cycle/second → 3.50 GHz ≈ 3.5 billion cycles/second  
- Speed is a broad measure; other CPU features also matter  
- Light apps (word processing) need less; video editing needs more  

### Licensing

| Method | How it works |
| --- | --- |
| License key | Type a key to unlock install/activation |
| Hardware token (dongle) | USB device must be present or the app won’t run — common for expensive niche software |

### Storage Space

Check free disk space against installer requirements. Large databases or data-heavy apps need extra attention.

### Distribution Methods

| Method | Notes |
| --- | --- |
| App store / vendor website | Preferred — trusted publisher |
| Avoid random third parties | You’re running someone else’s code |
| Optical media (CD/DVD) | Legacy physical install |
| USB drive | Common offline / air-gapped / data-center installs |
| Single executable installer | Typical for many apps |
| **ISO image** | Disk image (ISO 9660) with a full folder tree; mounting shows files/folders, not just one opaque file |
| Drive / OS **image** | Clone of OS + patches + apps + configs for fast redeploy |

**Imaging notes:**

- Identical hardware → smooth  
- Different hardware → may lack drivers  
- **VMs** often use identical virtual hardware → great for image deploy  
- Common recovery path: replace PC → apply image → back online quickly  

### Business Impact and Testing

Installed apps inherit the **logged-on user’s rights** (local files, network shares, other resources).

| Risk | Example |
| --- | --- |
| Untested app | Breaks other apps, slows system, overwrites documents |
| Network access | App can reach internal services the user can reach |
| Permissions | Wrong share rights → accidental deletes |
| UI / workflow change | One upgrade can disrupt hundreds of users |
| Failed upgrade | Full system failure → financial impact |

**Best practice:** Test in a **lab or sandbox** before production rollout.

## Side-by-Side Comparison

| Situation | What to verify |
| --- | --- |
| Old 32-bit app on new PC | 64-bit Windows can usually still run it (`Program Files (x86)`) |
| New 64-bit app on ancient 32-bit OS | Won’t run — need 64-bit OS |
| Video editor install | Discrete GPU? Enough RAM/CPU/storage? |
| High-cost niche CAD tool | Hardware license token? |
| Server with no internet | USB / offline media install |
| Deploy 50 identical VMs | Golden image |
| Company-wide upgrade | Lab test first |

## Key Terms

| Term | Meaning |
| --- | --- |
| 32-bit / 64-bit | Architecture of OS, drivers, and apps |
| Integrated graphics | GPU on the CPU package |
| Discrete graphics | Separate dedicated GPU |
| Hardware token | USB dongle required to run licensed software |
| ISO | Disk image file (ISO 9660 file system) |
| System image | Cloned OS + apps + config for mass deploy |
| Sandbox / test lab | Safe place to try apps before production |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Windows 11 bitness | 64-bit only |
| 32-bit app folder | Program Files (x86) |
| Driver must match OS | Same bitness as OS |
| App needs more RAM than free | Check Task Manager; upgrade |
| USB dongle required | Hardware license token |
| Mount ISO → see folders | Disk image, not a single opaque blob |
| Image on different hardware fails | Missing drivers |
| Bad install hit the file server | App runs with user permissions — test first |

## Common Mix-Ups

### App RAM requirement = total PC RAM needed

It’s for the app — OS and other programs still need their share.

### 32-bit OS can run 64-bit apps

No. Only 64-bit OS runs both (on Windows).

### Any download site is fine

Prefer vendor / official store — trust matters.

### Imaging always works on any PC

Hardware differences break drivers; VMs are the easy case.

## Quick Review

| Topic | Remember |
| --- | --- |
| Bitness | Drivers match OS; 64-bit OS runs 32- and 64-bit apps |
| Resources | RAM, CPU GHz, storage, integrated vs discrete GPU |
| License | Key or hardware token |
| Source | Vendor/store; USB/ISO when offline |
| ISO / image | Mountable disk image; clones for fast deploy |
| Business | User rights + test before production |

---

## Continue Learning

- Previous Topic: [Windows Settings](windows-settings.md)
- Next Topic: [Cloud Productivity Tools](cloud-productivity-tools.md)
- Related: [The Windows Control Panel](the-windows-control-panel.md)
- Related: [Operating Systems Overview](operating-systems-overview.md)
- Back to [Domain 1 — Operating Systems](README.md)
- Course Map: [Core 2 Study Path](../COURSE-MAP.md)
