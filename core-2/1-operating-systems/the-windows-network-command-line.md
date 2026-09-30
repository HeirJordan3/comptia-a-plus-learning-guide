# The Windows Network Command Line

CompTIA A+ Core 2 — 220-1202  
Objective 1.5 — Given a scenario, use the appropriate Windows command-line tools

## What You Need to Know

By the end of this lesson, you should understand:

- **ipconfig** and **ipconfig /all**
- **ping** and what a reply tells you
- **netstat**, including `-a`, `-b`, and `-n`
- **nslookup**
- **net view**, **net use**, and **net user**
- **tracert** and how Time to Live finds each hop
- **pathping** as traceroute plus per-hop loss stats

## What Is It?

These are Windows command-line tools for network troubleshooting. They show how this PC is addressed, whether another device answers, which apps have connections open, how names become IP addresses, which Windows shares exist, and which routers sit between you and a destination.

## Why Does It Matter?

Every PC can have a different network setup. Before you change anything, read the current configuration. Then test reachability, name resolution, and the path. That separates “this PC has a bad address” from “a router in the middle dropped the traffic.”

## Real-World Analogy

| Command | Like |
| --- | --- |
| ipconfig | Reading the address on your own mailbox |
| ping | Knocking on one door and waiting for an answer |
| netstat | A list of phone calls in progress |
| nslookup | Asking the phone book to turn a name into a number |
| net use | Mapping a shared filing cabinet to a drive letter |
| tracert | Listing every intersection between here and the destination |
| pathping | That same route, then timing how many cars get lost at each intersection |

## How It Works

### ipconfig

**ipconfig** shows how this computer is set up on the network: IPv4 and IPv6 addresses, subnet masks, and default gateways. It works for wired Ethernet and wireless adapters.

**ipconfig /all** adds more:

- Host name and DNS suffix
- DNS servers
- Whether DHCP is enabled
- Adapter and other configuration details

Run plain `ipconfig` first. Use `/all` when you need DNS, DHCP, and host details.

### ping

**ping** tests whether another device answers. It sends a small packet and waits for a reply using **ICMP** (Internet Control Message Protocol).

A typical test sends **four** pings of **32 bytes**. The summary shows:

| Result | Meaning |
| --- | --- |
| Replies received | The device answered |
| 0% loss | All four came back |
| Round-trip time (ms) | How long the reply took (minimum, maximum, average) |
| Time to live (TTL) | How many hops the reply is still allowed to travel |

Example: ping the DNS server address you saw in `ipconfig` (such as `192.168.1.155`). Replies mean you can reach that server. Large or uneven times mean the path is slow or uneven, even if it works.

### netstat

**netstat** (network statistics) lists network connections. Windows, Linux, and macOS all have a version of it.

| Option | What you see |
| --- | --- |
| `netstat` | Current connections |
| `netstat -a` | All active connections |
| `netstat -b` | The program (`.exe`) that owns each connection |
| `netstat -n` | IP addresses only — skip DNS name lookups |

Columns usually include:

| Column | Meaning |
| --- | --- |
| Protocol | TCP or UDP |
| Local address | This PC and port |
| Foreign address | The other device |
| State | For example **ESTABLISHED** or **CLOSE_WAIT** |

Opening a browser adds rows because the browser opened new connections. **netstat -b** needs an **elevated** Command Prompt. After you open a site, those HTTPS rows often show `chrome.exe` or another browser as the executable.

### nslookup

**nslookup** asks DNS to turn a name into an IP address, or an IP address into a name. It can also ask for other DNS record types. Most of the time you look up one name.

```text
nslookup www.example.com
```

The reply names the DNS server that answered (the one from `ipconfig`) and the address or addresses for that name. More than one address is normal when a name is set up with redundancy.

### NET commands

**net** is a Windows command for shares and local or domain accounts. It is not only a TCP/IP test.

| Command | Use |
| --- | --- |
| `net view \\servername` | List shares on that server |
| `net use H: \\servername\Sharename` | Map that share to drive **H:** |
| `net user username /domain` | Show a domain account |

`net view` often shows built-in shares such as **NETLOGON** and **SYSVOL**, plus file shares the company created. After `net use` succeeds, the new drive letter appears in File Explorer.

`net user` can show the full name, whether the account is active, when the password was set and when it expires, login script, home directory, and group membership.

### tracert

**tracert** is the Windows name for traceroute. It lists each router between you and a destination. Like ping, it uses **ICMP**.

**Time to live (TTL)** in IPv4 is **not a clock**. It is a **hop count**. A hop is one pass through a router. Each router subtracts 1 from the TTL. When TTL hits **0**, that router sends back **Time to Live Exceeded** and does not forward the packet.

tracert uses that on purpose:

1. Send a probe with TTL = 1. The first router drops it and replies. That reply is hop 1.
2. Send TTL = 2. The second router is the one that hits 0 and replies.
3. Keep increasing TTL until the destination itself answers.

Each line usually shows **three** tries, the response time for each, and the router’s name or IP address. If a router in the middle fails later, run tracert again and compare the path.

Some firewalls block ICMP. Those hops can show timeouts even when other traffic still works. You may not see every router.

### pathping

**pathping** combines tracert and ping. It runs in two phases:

| Phase | What it does |
| --- | --- |
| 1 | Traceroute — build the list of hops |
| 2 | Send traffic to each hop for a while (often several minutes) and count loss and round-trip time |

The report shows each hop, packets sent, packets lost, and addresses. A hop with no statistics often means a firewall or filter at that router, not necessarily that the whole path is down.

## Side-by-Side Comparison

| Question | Command |
| --- | --- |
| What is my IP, mask, and gateway? | `ipconfig` |
| Which DNS server and is DHCP on? | `ipconfig /all` |
| Can I reach this one address? | `ping` |
| What connections are open right now? | `netstat` |
| Which program opened that connection? | `netstat -b` (as administrator) |
| Show numbers instead of names | `netstat -n` |
| What IP goes with this name? | `nslookup` |
| What folders are shared on that server? | `net view \\server` |
| Give this share a drive letter | `net use` |
| Is this domain account active, and which groups? | `net user name /domain` |
| Which routers are on the path? | `tracert` |
| Which hop is losing packets? | `pathping` |

## Key Terms

| Term | Meaning |
| --- | --- |
| ipconfig | Shows this PC’s IP configuration |
| ping | ICMP reachability test |
| ICMP | Internet Control Message Protocol |
| Round-trip time | How long a reply takes, in milliseconds |
| netstat | Lists network connections and states |
| nslookup | DNS lookup tool |
| net view / net use / net user | List shares, map a share, or inspect an account |
| tracert | Windows traceroute |
| Hop | One router along the path |
| TTL | Time to live — a hop limit, not a clock |
| pathping | Traceroute plus per-hop loss statistics |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Need IP, subnet, gateway, DNS, DHCP | `ipconfig /all` |
| “Is the server up?” from this PC | `ping` |
| Four sent, four received, 0% loss | ping succeeded |
| Which exe owns the connection | `netstat -b`, elevated |
| Do not resolve names in the connection list | `netstat -n` |
| Name will not become an IP | `nslookup` |
| Map `\\server\share` to H: | `net use H: \\server\share` |
| Password age and group membership | `net user` |
| First router, second router, then the host | `tracert` and TTL |
| TTL exceeded | A router hit TTL 0 and reported itself |
| Where along the path are packets dropped? | `pathping` |
| One hop shows no replies | ICMP filtered — often a firewall |

## Common Mix-Ups

### TTL is measured in seconds

On an IPv4 packet, TTL is a **hop counter**. Routers decrease it by 1. It is not a time of day.

### ping and tracert prove every application works

They prove **ICMP** reachability and the router path. A firewall can block ICMP while web traffic still works, or the reverse.

### netstat -b works in a normal prompt

Showing the executable needs an **administrator** Command Prompt.

### net view tests an IP route

`net view`, `net use`, and `net user` are **Windows share and account** commands. Use ping, tracert, and pathping for the IP path.

### pathping is a faster ping

The first phase is a traceroute. The second phase measures each hop and can take several minutes.

## Quick Review

| Topic | Remember |
| --- | --- |
| Address | `ipconfig`, then `ipconfig /all` |
| Reachability | `ping` — ICMP, four tries, loss and round-trip time |
| Connections | `netstat`; `-a` all, `-b` program (admin), `-n` numbers only |
| DNS | `nslookup` |
| Shares and users | `net view`, `net use`, `net user` |
| Path | `tracert` — TTL starts at 1 and increases each hop |
| Loss by hop | `pathping` — map the path, then measure it |

---

## Continue Learning

- Previous Topic: [Windows Command Line Tools](windows-command-line-tools.md)
- Next Topic: [The Windows Control Panel](the-windows-control-panel.md)
- Related: [Windows Network Technologies](windows-network-technologies.md)
- Back to [Domain 1 — Operating Systems](README.md)
- Course Map: [Core 2 Study Path](../COURSE-MAP.md)
