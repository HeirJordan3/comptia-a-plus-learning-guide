# Windows Network Connections

CompTIA A+ Core 2 — 220-1202  
Objective 1.7 — Given a scenario, configure Microsoft Windows networking features on a client/desktop

## What You Need to Know

By the end of this lesson, you should understand:

- Where Windows sets up **Ethernet**, **VPN**, and **dial-up** connections
- How a **VPN** and a **VPN concentrator** protect traffic on a public network
- Wireless settings: **SSID**, **AES**, **WPA2/WPA3** Personal vs Enterprise
- Why a wired link usually becomes the **default** connection
- **WWAN**, proxies, and **private vs public** network profiles
- How to **map** and disconnect a network drive
- What a **metered** connection changes

## What Is It?

Windows can join many kinds of networks: a cable, Wi-Fi, a cell connection, a dial-up line, or an encrypted tunnel back to the office. **Network location** (private or public) then decides how much of your PC you expose. You can also point a drive letter at a shared folder and tell Windows when a link is expensive to use.

## Why Does It Matter?

The same laptop behaves differently at a desk, at home, and in a coffee shop. You need to know:

- How to build a VPN back to company resources
- Which wireless security a business uses versus a home
- Why Ethernet wins when several connections are up
- Why a public profile blocks file sharing
- How to map `\\server\share` and how to limit data on a metered link

## Real-World Analogy

| Connection | Like |
| --- | --- |
| Ethernet | A private hallway inside the building — usually the fastest door |
| Wi-Fi | The same building, but you need the network name and a key |
| WWAN | Using the cell network when there is no building network |
| VPN | An armored tunnel from the coffee shop back to the office |
| Proxy | A security desk that fetches web pages for you and checks them first |
| Public profile | Hotel mode — do not share your files |
| Mapped drive | A short nickname (H:) for a folder that lives on another computer |

## How It Works

### Where You Create a Connection

**Control Panel → Network and Sharing Center → Set up a new connection or network**

You can connect to the internet, set up a new network, or connect to a workplace.

**Settings → Network & Internet** offers the same kinds of choices. A wizard asks for the settings that match the connection type: Ethernet, VPN, dial-up, and others.

### VPN

A **VPN** (Virtual Private Network) sends traffic across a public network **encrypted**.

Example: company file servers and printers are on a protected network. A coffee-shop Wi-Fi network is open to everyone. A **VPN client** on the laptop encrypts the traffic. A **VPN concentrator** at the company decrypts it and delivers it to internal resources. Replies are encrypted on the way back and decrypted on the laptop.

| Piece | Role |
| --- | --- |
| VPN client | Software on your PC; Windows includes one, or the company may require its own |
| Public network | The unsafe path (coffee shop, hotel, home internet) |
| VPN concentrator | Company device that ends the tunnel |
| Encryption | Protects the data while it crosses the public network |

Built-in client path: set up a connection → **Connect to a workplace** → use your internet connection (VPN) rather than dial-up.

You then enter:

- The concentrator address, such as `vpn.example.com`
- A connection name
- Optional **smart card** (extra authentication)
- Whether to remember credentials
- Whether other people on this PC may use the connection

A smart card is **something you have**. A password is **something you know**. A fingerprint is **something you are**. Together those are multi-factor authentication.

Turn the VPN on or off from the network icon in the system tray.

### Wireless Networks

At home you often pick a network name and type a password. A business setup asks for more:

| Setting | Meaning |
| --- | --- |
| **SSID** | Service Set Identifier — the wireless network name |
| Security type | Which protection the network uses |
| Encryption | How the wireless data is scrambled |
| Security key | The password or enterprise credentials |

**TKIP** is the older encryption type. Most networks now use **AES**.

| Mode | Typical use |
| --- | --- |
| **WPA2** or **WPA3 Personal** | Home — a **PSK** (pre-shared key) everyone types |
| **WPA2** or **WPA3 Enterprise** | Business — **802.1X** checks a central username and password |

Enterprise Wi-Fi lets you use the same account you use for the rest of the organization.

### Wired Ethernet

Plug in a cable. That direct link is usually the **fastest**. When Ethernet, Wi-Fi, and a wireless wide-area connection are all up, Windows uses the **fastest as the default**. That is normally Ethernet.

Adapter properties (right-click the Ethernet adapter → Properties → **Internet Protocol Version 4**) let you:

- Type a manual IP address, or obtain one automatically with DHCP
- Receive DNS automatically, or type DNS servers
- Set an **Alternate Configuration** if DHCP is unavailable: APIPA, or a manual address

If DHCP does not answer, Windows uses whatever you saved on that Alternate Configuration tab.

### WWAN

A **WWAN** (Wireless Wide Area Network) is a cellular connection, the kind phones and tablets use.

| Method | Detail |
| --- | --- |
| Internal or USB adapter | A modem card in the PC or a dongle |
| Tether | The phone shares its cell connection over a cable |
| Hotspot | The phone becomes a small Wi-Fi network |

A hardware adapter may need the vendor’s own software. Check the device documentation.

### Proxy Servers

A **proxy** sits between you and the rest of the network, often as a security control. It sends the request for you, checks the answer, and then passes a safe response back.

Configure it in either place:

- Control Panel → **Internet Options → Connections → LAN settings**
- **Settings → Network & Internet → Proxy**

You can use automatic setup, or type a proxy server and its authentication. Some apps break through a proxy. Add those as **exceptions** so they go straight to the internet and skip the proxy.

### Network Location (Profile)

Windows attaches a **network profile** to the connection. The profile is a broad security preset.

| Profile | Typical place | Default posture |
| --- | --- | --- |
| **Private** | Home or work | Treated as a safer network, often behind a firewall |
| **Public** | Coffee shop, hotel, open Wi-Fi | No file sharing, no inbound connections — highest default security |

You can tighten or loosen either profile, and some PCs have extra profiles for finer control.

### Mapping a Network Drive

You need the **server name** and the **share name**. Mapping assigns a local drive letter so you do not type the full path every time.

UNC path shape:

```text
\\fileserver\Gate Room
```

Two backslashes, the server, one backslash, then the share. If the share name has a space, put **quotes** around the destination on the command line.

In File Explorer, use **Map network drive** from the toolbar or the three-dot menu. Pick a free letter (for example **H:**), enter the folder, and finish. If your current login is not allowed, Windows asks for the right username and password. The new letter then shows in File Explorer.

Command-line equivalent:

```text
net use H: "\\fileserver\Gate Room"
```

Right-click a mapped share to **disconnect** it.

### Metered Connections

Some links bill you by how much data you use. Mark the connection as **metered** so Windows uses less data.

**Settings → Network & Internet → Ethernet** (or the wireless connection) → **Metered connection**.

**Set a data limit** shows app usage and lets you set:

- A monthly limit
- A one-time limit
- Unlimited

You can also set when the limit resets and how much data is allowed.

## Side-by-Side Comparison

| Need | Use |
| --- | --- |
| Encrypt traffic from a public network to the office | VPN client to a concentrator |
| Extra VPN login factor | Smart card (something you have) plus password |
| Home Wi-Fi password | WPA2/WPA3 Personal, PSK, AES |
| Company Wi-Fi with your domain account | WPA2/WPA3 Enterprise, 802.1X |
| Cable and Wi-Fi both connected | Ethernet is usually the default because it is fastest |
| No DHCP | Alternate Configuration |
| Cellular when there is no Wi-Fi | WWAN, tether, or hotspot |
| Company scans web traffic | Proxy, with exceptions for apps that cannot use it |
| Open Wi-Fi | Public profile — sharing off |
| Short name for a share | Map a drive, or `net use` |
| Pay-by-the-gigabyte link | Metered connection and a data limit |

## Key Terms

| Term | Meaning |
| --- | --- |
| VPN | Encrypted tunnel across a public network |
| VPN concentrator | Device at the company that ends the VPN tunnel |
| SSID | The wireless network name |
| AES | Current wireless encryption; TKIP is older |
| PSK | Pre-shared key — the personal Wi-Fi password |
| 802.1X | Enterprise Wi-Fi login against a central authentication server |
| WWAN | Cellular wide-area connection |
| Proxy | A middle device that requests and checks traffic for you |
| Private network | Home or work profile |
| Public network | Open-network profile with sharing and inbound access off by default |
| UNC path | `\\server\share` |
| Metered connection | A link Windows treats as limited or costly |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Coffee shop to company file server, traffic encrypted | VPN |
| Device that decrypts the tunnel at the office | VPN concentrator |
| Password plus smart card | Multi-factor: know + have |
| Wireless network name | SSID |
| Old vs current wireless encryption | TKIP vs AES |
| Home Wi-Fi uses one shared password | WPA2/WPA3 Personal, PSK |
| Work Wi-Fi uses your user account | Enterprise, 802.1X |
| Ethernet, Wi-Fi, and WWAN all connected | Fastest (usually Ethernet) is the default |
| Phone shares internet | Tether or hotspot (WWAN) |
| Web requests go through a middle server | Proxy; exceptions bypass it |
| Hotel Wi-Fi should not share your files | Public network profile |
| `\\server\share` becomes H: | Mapped drive; quote names that contain spaces |
| Carrier charges by data used | Metered connection |

## Common Mix-Ups

### A VPN makes the coffee shop network private

The coffee shop is still a public network. The VPN encrypts **your tunnel** to the company. It does not secure everyone else in the shop.

### WPA2 Personal and WPA2 Enterprise are the same login

Personal uses a **pre-shared key**. Enterprise uses **802.1X** and a central username and password.

### Every connection is equal

If several are up, Windows prefers the **fastest**. A plugged-in Ethernet cable normally wins over Wi-Fi and WWAN.

### Public and private are just labels

Public defaults to **no file sharing** and **no inbound** connections. Private is the home-or-work preset.

### A mapped drive is a second copy of the files

The letter is a shortcut to a share. Disconnect removes the shortcut, not the files on the server.

## Quick Review

| Topic | Remember |
| --- | --- |
| Setup | Network and Sharing Center, or Settings → Network & Internet |
| VPN | Client encrypts; concentrator decrypts; workplace wizard |
| Wi-Fi | SSID, AES, Personal PSK vs Enterprise 802.1X |
| Wired | Usually fastest, so it becomes the default |
| WWAN | Cell adapter, USB modem, tether, or hotspot |
| Proxy | Middle server; automatic or manual; app exceptions |
| Profile | Private at home/work; public when the network is open |
| Drive map | `\\server\share` or `net use`; quotes if the name has a space |
| Metered | Limits data use and can enforce a cap |

---

## Continue Learning

- Previous Topic: [Windows IP Address Configuration](windows-ip-address-configuration.md)
- Next Topic: [macOS Overview](macos-overview.md)
- Related: [Windows Network Technologies](windows-network-technologies.md)
- Related: [Configuring Windows Firewall](configuring-windows-firewall.md)
- Back to [Domain 1 — Operating Systems](README.md)
- Course Map: [Core 2 Study Path](../COURSE-MAP.md)
