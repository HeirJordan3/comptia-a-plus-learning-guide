# Troubleshooting Networks

CompTIA A+ Core 1 — 220-1201  
Objective 5.5 — Given a scenario, troubleshoot common network problems

## What You Need to Know

By the end of this lesson, you should understand how to approach:

- Baseline connectivity checks (link light → loopback → local IP → gateway → remote)
- Intermittent wireless (channel, signal, antennas, multipath, AP placement)
- “Slow network” that may not be the network
- Limited / no connectivity and APIPA
- High jitter and poor VoIP / real-time quality
- Port flapping
- High latency
- Wireless interference and SNR
- Authentication / permission failures
- Intermittent issues and third-party / SLA work

## What Is It?

**Network troubleshooting** finds where communication breaks — cable, IP stack, local LAN, gateway, wireless RF, congestion, or authentication — then proves whether the problem is really the network or something else (CPU, app, server).

## Why Does It Matter?

Users say “the network is down” for almost every delay. Your job is to:

- Prove Layer 1 / Layer 3 basics quickly
- Separate RF problems from IP problems
- Measure jitter and latency for real-time apps
- Catch physical flapping and APIPA
- Document intermittent issues when they happen

## Real-World Analogy

Think of network troubleshooting like checking a delivery route:

- Link light = truck left the dock
- Ping loopback = your own radio works
- Ping local IP = your address is real
- Ping gateway = you can reach the neighborhood exit
- Ping Quad 8 / 9 / 1 = you can reach the highway
- Jitter = packages arrive in uneven clumps (bad for live calls)
- Port flapping = the dock door keeps opening and closing
- SNR = how loud your Wi-Fi is compared to the noise around it

## How It Works

### Connectivity Baseline (Wired First Steps)

Work from closest to farthest:

| Step | What you check | Pass means |
| --- | --- | --- |
| 1. Link light | Ethernet NIC / switch port LED | Physical signal to the other end |
| 2. Ping `127.0.0.1` | Loopback | Local IP stack is healthy |
| 3. Ping your own IP | DHCP or static address | Local interface responds |
| 4. Ping default gateway | Local router / L3 device | LAN path works |
| 5. Ping remote (e.g. Quad 8, Quad 9, Quad 1) | Outside the LAN | Routing / Internet path works |

No link light → bad cable, bad port, or no connection. Fail at a hop → focus troubleshooting there.

### Intermittent Wireless

| Cause / idea | What to try |
| --- | --- |
| Channel / band interference | Change AP channel or frequency |
| Weak signal | Move closer to the AP |
| Coverage | Try different / external antennas; relocate AP centrally |
| Congestion | Let AP auto-select channel, or set channel manually and test |
| Multipath | Reflections off flat surfaces; reposition AP |
| Distance | AP too far — central placement helps everyone |

### Is It Really Slow Network?

“Slow network” is often:

- Local CPU / memory
- Application or database server

Prove the network:

- Ping end-to-end and watch response times
- Run a **speed test** — good Internet numbers often rule out a major link problem
- Check each hop: utilization, errors, throughput
- Review firewall / ACL filtering
- Capture packets at multiple points to see where delay appears

### Limited or No Connectivity

Windows may show **limited or no connectivity** or **no Internet access**.

| Finding | Meaning |
| --- | --- |
| Valid DHCP / static IP | Should reach beyond the subnet if routing works |
| **APIPA** address | DHCP failed — local subnet only, no Internet |
| Gateway ping fails | Local path or gateway problem |
| Remote ping fails after gateway works | Problem past the LAN |

Work outward until pings fail — that hop is where you dig.

### Jitter and Real-Time Quality (VoIP / Video)

Real-time audio/video cannot “rewind” lost moments. Missed data is gone.

**Jitter** = variation in time between frames/packets.

| Pattern | Result |
| --- | --- |
| Steady intervals, low jitter | Smooth call / video |
| Bursts then long gaps, high jitter | Freezing video, choppy audio |

Also watch **latency** — real-time apps need low delay.

Tools:

- Speed test (enough bandwidth?)
- Upgrade aging routers/switches if they cannot keep up
- Packet capture for traffic volume vs timing issues

### Port Flapping

Link light goes **up → down → up → down** repeatedly.

| Likely cause | Test |
| --- | --- |
| Bad cable / connector | Replace cable or re-terminate |
| Bad switch port | Move cable to another port — does the problem follow the cable? |

Patch cables are easy swaps; long runs may need a new cable pull.

### Latency

**Latency** = delay between request and response (microseconds to seconds or worse).

Some delay is normal (send → process → reply). Measure:

- Latency per hop
- Packet captures to split **network delay** vs **application delay**

### Wireless Interference and SNR

Unexpected interferers:

- Fluorescent lights
- Microwave ovens
- Cordless phones
- Other high-power RF / neighbor Wi-Fi

You may not control neighbors’ gear. Measure **signal-to-noise ratio (SNR)**:

| Goal | Meaning |
| --- | --- |
| High SNR | Lots of signal, little noise — good experience |
| Near 1:1 | Signal ≈ noise — poor Wi-Fi |

OS tools / graphs can show SNR over time.

### Authentication and Permissions

Failure may not be cables or RF:

- Need username / password / MFA
- Session timed out — re-authenticate
- Background service credentials failed (little or no UI error)

Packet capture showing immediate **access denied** points to auth / permissions.

### Intermittent Problems

Hardest issues: works sometimes, fails sometimes.

| Approach | Why |
| --- | --- |
| Continuous ping | Catch drops as they happen |
| Traceroute | See where path changes |
| Occasional speed tests | Spot performance swings |
| Third-party coordination | When the path leaves your network |
| Check **SLA** | Uptime expectations and support response times |

Capture evidence **while** the problem is occurring.

## Side-by-Side Comparison

| Symptom | First useful direction |
| --- | --- |
| No link light | Cable / port / physical |
| Loopback fails | Local OS / IP stack |
| APIPA / limited connectivity | DHCP failure |
| Intermittent Wi-Fi | Channel, signal, AP placement, multipath |
| Choppy VoIP / frozen video | Jitter, latency, congestion |
| Link blinking up/down | Port flapping — cable vs switch port |
| High delay | Latency — hops and packet capture |
| Weak Wi-Fi with “noise” | SNR / interference |
| Access denied in capture | Authentication / permissions |
| Random outages | Continuous ping / SLA with vendor |

## Key Terms

| Term | Meaning |
| --- | --- |
| Link light | LED showing Ethernet physical link |
| Loopback | `127.0.0.1` — tests local IP stack |
| Default gateway | Router for leaving the local subnet |
| Quad 8 / 9 / 1 | Common public DNS/test IPs (8.8.8.8, etc.) |
| Multipath | Reflected Wi-Fi signals causing problems |
| APIPA | Auto private IP when DHCP fails |
| Jitter | Variation in packet arrival timing |
| Port flapping | Interface repeatedly up/down |
| Latency | Delay between request and response |
| SNR | Signal-to-noise ratio |
| SLA | Service level agreement with a provider |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| No Ethernet LED | Physical / cable |
| Ping 127.0.0.1 fails | Local stack |
| 169.254.x.x | APIPA — DHCP problem |
| Limited connectivity | Often APIPA or no gateway path |
| Choppy VoIP | High jitter |
| Link up/down cycling | Port flapping — swap cable/port |
| Microwave kills Wi-Fi | Interference / SNR |
| Access denied in capture | Auth, not bandwidth |
| “Slow” but speed test is fine | App / server / local PC |

## Common Mix-Ups

### Slow = always network

Often CPU, app, or database — prove with ping, speed test, and captures.

### Jitter = same as latency

Latency is delay; jitter is **uneven** delay between packets.

### APIPA means “Internet is fine”

APIPA is local-only — no routing off the subnet.

### Port flapping = always switch failure

Often the **cable**; move ports to isolate.

### High SNR is bad

You want a **large** signal vs noise gap.

## Quick Review

| Topic | Remember |
| --- | --- |
| Baseline | Link → loopback → self → gateway → remote |
| Wireless | Channel, signal, antennas, placement, multipath |
| Slow? | Prove network vs app/CPU |
| Limited | Check IP; APIPA = DHCP |
| VoIP bad | Jitter + latency |
| Flapping | Cable then switch port |
| Latency | Measure hops and app share |
| Wi-Fi noise | SNR; mics, lights, neighbors |
| Auth | Credentials / timeout / capture deny |
| Intermittent | Ping while broken; use SLA |

---

## Continue Learning

- Previous Topic: [Troubleshooting Mobile Devices](troubleshooting-mobile-devices.md)
- Next Topic: [Troubleshooting Printers](troubleshooting-printers.md)
- Related: [Troubleshooting Hardware](troubleshooting-hardware.md)
- Back to [Domain 5 — Hardware and Network Troubleshooting](README.md)
