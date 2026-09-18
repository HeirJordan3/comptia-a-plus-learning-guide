# Expansion Cards

CompTIA A+ Core 1 — 220-1201  
Objective 3.5 — Motherboards, CPUs, and Add-on Cards

## What You Need to Know

By the end of this lesson, you should understand:

- What expansion cards are and why PCs use them
- Sound cards and common audio ports
- Integrated vs discrete graphics (GPU)
- Capture cards and why they often use PCIe
- Network interface cards (NICs), including multi-port cards
- How to choose a compatible adapter
- Driver install order and update best practices
- Using Device Manager to check driver status

## What Is It?

**Expansion cards** (adapter cards) add hardware features that are missing — or not strong enough — on the motherboard.

Modern PCs are modular: start with a general board, then customize with cards for:

- Sound
- High-end graphics
- Video capture
- Wired networking

Most cards install into motherboard expansion slots (commonly **PCIe**). Users can usually install them without returning the PC to the manufacturer.

## Why Does It Matter?

Techs install expansion cards when:

- Onboard audio is not good enough for music or home theater
- Gaming, video editing, or 3D work needs a discrete GPU
- A streamer or studio needs HDMI/SDI video **input**
- A board has no Ethernet jack, a dead NIC, or needs more ports
- A server needs multiple network connections

Exam questions often describe the card type by its job (audio outs, GPU, capture input, Ethernet ports) or ask about drivers.

## Real-World Analogy

Think of the motherboard as a basic workshop bench.

Expansion cards are **tool attachments**:

- Sound card = better speakers / studio inputs
- GPU = heavy-duty graphics engine
- Capture card = camera/feed input station
- NIC = extra network hookups

You bolt on what the job needs.

## How It Works

### Typical Install Flow

1. Power down and open the case
2. Seat the card in a compatible slot
3. Secure the card to the case
4. Connect any required cables / power
5. Boot the OS
6. Install or verify **device drivers**

Often Windows detects the card and installs a basic driver. Always follow the card’s documentation for the correct order.

### Sound Cards

A **sound card** improves or expands audio beyond basic onboard sound.

It may provide:

- Higher-quality audio hardware
- More outputs for multi-speaker / subwoofer home theater setups
- Extra inputs for instruments, mics, or multiple audio sources

Example ports you might see:

| Port idea | Role |
| --- | --- |
| Left / right audio out | Speaker output |
| Headphone | Personal listening |
| Line in | External audio source |
| Digital audio out | Digital connection to another device |

### Video Adapters (GPUs)

Many CPUs include **integrated graphics**. Video ports for that may sit on the motherboard I/O (VGA, DVI, HDMI, etc.).

A **discrete graphics card** / **GPU**:

- Is separate from the CPU
- Adds its own graphics processing and memory
- Uses its own video outputs on the card
- Fits in a motherboard slot (typically PCIe x16)

Choose discrete graphics for high-end gaming, video editing, or heavy graphics work.

### Capture Cards

A **capture card** brings **video into** the computer (opposite of a GPU’s main job of outputting display).

Sources may include:

- Cameras
- Other computers / consoles
- Studio video feeds

Because video moves a lot of data, capture cards usually need high throughput and often connect over **PCIe**.

Example inputs: **HDMI**, **SDI** (serialized professional video).

### Network Interface Cards (NICs)

A **NIC** adds wired Ethernet when:

- The motherboard has no Ethernet jack
- The onboard NIC failed
- You need more Ethernet ports (servers, security appliances, multi-homed systems)

Install process matches other adapter cards: open slot → install → drivers.

A **multi-port Ethernet card** can provide several Ethernet connections in one slot (example: four ports).

### Choosing the Right Card

Before buying or installing:

1. Check **motherboard documentation** — slot type and availability
2. Check the **adapter manufacturer** — minimum hardware/software requirements
3. Review the manufacturer **knowledge base** for known issues
4. Ask other users when helpful

### Driver Best Practices

| Practice | Why |
| --- | --- |
| Read the card’s docs for install order | Some need driver **before** hardware; others **after** |
| Prefer the latest driver from the manufacturer | Fixes bugs and improves compatibility |
| Uninstall old drivers if required before upgrading | Avoid conflicts |
| Use Device Manager | Install/update drivers and check status |

After boot, open **Device Manager** to confirm the device is present and the driver is working.

## Side-by-Side Comparison

| Card | Main job | Exam clue |
| --- | --- | --- |
| Sound card | Better / more audio I/O | Speakers, mics, line in, digital out |
| Discrete GPU | High-end video **output** / graphics | Gaming, editing, own HDMI/DP on card |
| Capture card | Video **input** into the PC | HDMI/SDI in, streaming, recording |
| NIC | Wired Ethernet | RJ-45 ports; multi-port for servers |

| Graphics type | Where video ports often are |
| --- | --- |
| Integrated | Motherboard rear I/O |
| Discrete GPU | On the graphics card bracket |

## Key Terms

| Term | Meaning |
| --- | --- |
| Expansion / adapter card | Add-on board that extends PC features |
| Sound card | Expansion card for audio input/output |
| Integrated graphics | GPU features built into the CPU/board path |
| Discrete GPU | Separate graphics card with its own resources |
| Capture card | Card that receives video into the computer |
| NIC | Network interface card — wired networking adapter |
| Multi-port NIC | One card with multiple Ethernet ports |
| Device driver | Software that lets the OS use the hardware |
| Device Manager | Windows tool to view/manage devices and drivers |
| PCIe | Common modern expansion bus for these cards |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Better audio / many speaker outs | Sound card |
| Gaming / editing needs more GPU power | Discrete graphics card |
| Motherboard VGA/DVI/HDMI only | Likely integrated graphics outputs |
| Need to record HDMI from another device | Capture card |
| No Ethernet / dead onboard NIC / more ports | NIC / multi-port NIC |
| Card not working after install | Check drivers / Device Manager |
| “Install driver first” in manual | Follow manufacturer order |
| High-bandwidth video capture | Often PCIe |

## Common Mix-Ups

### GPU vs capture card

- **GPU** mainly **displays** graphics out
- **Capture card** mainly **brings video in**

### Integrated vs discrete graphics

Integrated uses CPU/board resources and motherboard ports. Discrete is a separate card with its own outputs and performance.

### NIC vs Wi-Fi only

A NIC here usually means a wired Ethernet adapter card (Wi-Fi can also be an adapter, but this lesson’s exam focus is the expansion-card networking story — especially Ethernet ports).

### Plug-and-play means “no drivers forever”

Windows may install a basic driver, but manufacturer drivers are often better — and sometimes required for full features.

### Wrong install order

Ignoring “driver before hardware” instructions is a common cause of failed installs.

## Quick Review

| Topic | Remember |
| --- | --- |
| Expansion cards | Add features the board does not provide well enough |
| Sound | Quality audio + extra I/O |
| GPU | Discrete card for heavy graphics; own outputs |
| Capture | Video **in**; often PCIe |
| NIC | Wired Ethernet; multi-port for more links |
| Compatibility | Check motherboard + card requirements |
| Drivers | Follow docs; update from manufacturer; verify in Device Manager |

---

## Continue Learning

- Previous Topic: [CPU Features](cpu-features.md)
- Next Topic: [Cooling](cooling.md)
- Related: [Motherboard Expansion Slots](motherboard-expansion-slots.md)
- Back to [Domain 3 — Hardware](README.md)
