# Windows IP Address Configuration

CompTIA A+ Core 2 — 220-1202  
Objective 1.7 — Given a scenario, configure Microsoft Windows networking features on a client/desktop

## What You Need to Know

By the end of this lesson, you should understand:

- **DHCP** as the usual way a PC gets an address
- **APIPA** (link-local) and the `169.254` range
- **Static** addresses and DHCP **reservations**
- IP address, subnet mask, default gateway, and **DNS**
- The IPv4 **loopback** address `127.0.0.1`
- Windows **Alternate Configuration** when DHCP is missing

## What Is It?

Windows IP configuration is how a PC gets the addresses it needs to use a network. Most of the time that happens automatically with **DHCP**. If DHCP is missing, Windows can invent a local-only **APIPA** address, or you can set a **static** address or an **alternate configuration** yourself.

## Why Does It Matter?

A PC that “has no internet” is often using the wrong kind of address. You need to tell these apart:

- A normal DHCP address that can reach the gateway and the internet
- An APIPA address that only works on the local link
- A static address you typed in for a device that must stay at the same number

## Real-World Analogy

| Method | Like |
| --- | --- |
| DHCP | A hotel that assigns you a room number when you check in |
| DHCP reservation | The hotel always saving the same room for you |
| Static address | You nail your own room number to the door |
| APIPA | You invent a number that only people in this hallway understand |
| Default gateway | The front door that leads to every other building |
| DNS | The directory that turns a name into a room number |
| Loopback | Talking to yourself to prove your phone works |

## How It Works

### DHCP

**DHCP** (Dynamic Host Configuration Protocol) gives a computer an IP address automatically. It is the default on most operating systems. Turn on the PC at home, in a coffee shop, or in a hotel, and it can get an address and use the network without you typing one.

At home, the DHCP server is often built into the internet router. A business often runs **more than one** DHCP server so the service still works if one server fails.

### APIPA (Link-Local)

If no DHCP server answers and nobody configured a static address, Windows assigns itself an **APIPA** address. **APIPA** means Automatic Private IP Addressing. It is also called a **link-local** address.

| Fact | Detail |
| --- | --- |
| Range | `169.254.1.0` through `169.254.254.255` |
| Where it works | Only on the local network |
| Internet | No — an APIPA address cannot be routed onto the internet |

See `169.254.x.x` on a workstation and treat it as “DHCP did not give this PC an address.”

### Static Addresses

A **static** address stays the same every time the device turns on. Two ways to get that:

- Type it on the computer
- Create an **address reservation** on the DHCP server so that device always receives the same address

A manual TCP/IP setup needs three values first:

| Value | Job |
| --- | --- |
| **IP address** | Unique identifier for this computer |
| **Subnet mask** | Defines which IP subnet this device is on |
| **Default gateway** | Router that forwards traffic off the local subnet |

You usually also set **DNS** (Domain Name System). DNS turns a name such as `www.example.com` into an IP address so you do not have to memorize the server’s number. DHCP can hand out the IP address, mask, gateway, and DNS server together.

### Loopback

The IPv4 **loopback** address is **127.0.0.1**. Any address on the `127` network is loopback, but `127.0.0.1` is the one to remember. It means “this computer.” It exists on every machine. Pinging it checks that the local IP stack is working. It does not test the cable, the router, or the internet.

### Alternate Configuration

Sometimes you want DHCP when a server is available, and a **known address** when it is not — not an APIPA address.

In Windows, the **Alternate Configuration** tab appears only after you choose **Obtain an IP address automatically**.

Path:

1. Control Panel → **Network and Sharing Center**
2. **Change adapter settings**
3. Right-click the Ethernet adapter → **Properties**
4. **Internet Protocol Version 4 (TCP/IPv4)** → **Properties**
5. Select **Obtain an IP address automatically**
6. Open **Alternate Configuration** → **User configured**
7. Enter the IP address, subnet mask, default gateway, and DNS servers you want if DHCP fails

Example of a user-configured alternate:

| Setting | Example |
| --- | --- |
| IP address | `10.1.10.102` |
| Subnet mask | `255.255.255.0` |
| Default gateway | `10.1.10.1` |
| DNS | A DNS server you choose, such as Quad9 |

Click OK. Windows uses DHCP when a server answers, and this alternate set when it does not.

## Side-by-Side Comparison

| Situation | Address you should see |
| --- | --- |
| Normal home or office network | DHCP address, plus a real gateway and DNS |
| No DHCP and no static or alternate setup | APIPA `169.254.x.x` — local only |
| Server or printer that must not change | Static address, or a DHCP reservation |
| DHCP at the office, fixed address at a site with no DHCP server | Automatic IP, plus Alternate Configuration |
| “Is the IP software on this PC alive?” | Ping `127.0.0.1` |

## Key Terms

| Term | Meaning |
| --- | --- |
| DHCP | Protocol that assigns IP settings automatically |
| Static address | An IP address configured to stay the same |
| Reservation | A DHCP server entry that always gives one device the same address |
| APIPA | Automatic Private IP Addressing — Windows self-assigns `169.254.x.x` |
| Link-local | An address that only works on the local network |
| Subnet mask | Defines the local subnet |
| Default gateway | Router used to leave the local subnet |
| DNS | Turns a domain name into an IP address |
| Loopback | `127.0.0.1` — this computer’s internal IP test address |
| Alternate Configuration | A backup IP setup Windows uses when DHCP is unavailable |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| PC gets an address by itself on a normal network | DHCP |
| Address starts with `169.254` | APIPA — no DHCP, no manual address |
| Can talk to nearby PCs but not the internet | Link-local / APIPA, or no usable gateway |
| Same address every boot, typed on the PC | Static configuration |
| Same address every boot, still using DHCP | DHCP reservation |
| Must know three settings for manual TCP/IP | IP address, subnet mask, default gateway |
| `www.example.com` becomes an IP | DNS |
| Ping `127.0.0.1` works | Local IP stack is up |
| DHCP when possible, this address if not | Alternate Configuration tab |

## Common Mix-Ups

### APIPA means the internet is down but the address is fine

An APIPA address is only for the **local link**. It is not a normal routed address.

### Loopback tests the network cable

`127.0.0.1` never leaves the computer. It tests the local IP stack.

### Alternate Configuration replaces DHCP

It is the **fallback**. Windows still tries DHCP first. The Alternate Configuration tab shows up only when the adapter is set to obtain an address automatically.

### A static address and a DHCP reservation are configured in the same place

A static address is typed on the device. A reservation is configured on the **DHCP server**.

## Quick Review

| Topic | Remember |
| --- | --- |
| Default | DHCP |
| No DHCP, no static | APIPA `169.254.1.0`–`169.254.254.255`, local only |
| Manual | IP, subnet mask, default gateway, often DNS |
| Always the same via DHCP | Reservation |
| Test this PC only | `127.0.0.1` |
| Fallback | Alternate Configuration after “Obtain automatically” |

---

## Continue Learning

- Previous Topic: [Configuring Windows Firewall](configuring-windows-firewall.md)
- Next Topic: [Windows Network Connections](windows-network-connections.md)
- Related: [The Windows Network Command Line](the-windows-network-command-line.md)
- Back to [Domain 1 — Operating Systems](README.md)
- Course Map: [Core 2 Study Path](../COURSE-MAP.md)
