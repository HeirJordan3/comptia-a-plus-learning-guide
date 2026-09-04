# DNS Study Guide

CompTIA A+ Core 1 — 220-1201  
Objective 2.4 — Network Configurations

Use this guide after the DNS lesson for deeper review and exam recognition practice.

## DNS Definition

DNS stands for Domain Name System.

DNS is the system that helps computers find resources by translating human-friendly hostnames into IP addresses.

Without DNS, users would often need to remember numeric addresses instead of names like `www.example.com`.

## Name Resolution

**Name resolution** is the process of converting a hostname into an IP address.

Simple path:

```text
Hostname
   ↓
DNS lookup
   ↓
IP address
   ↓
Connection to the destination
```

### Phone Contacts Analogy

You remember “Mom,” not a long phone number. Your contacts list resolves the name into the number.

DNS does something similar for networks.

## Why DNS Matters

In IT support, DNS problems often look like this:

- A website or server fails by name
- The same destination works by IP address

That pattern usually means name resolution is the problem, not the destination server itself.

Help desk example:

A user cannot open `server.company.com`, but `192.168.1.50` works.

Start by investigating DNS.

## Distributed and Hierarchical DNS

### Distributed

DNS is distributed. No single server stores every hostname for the whole internet. Responsibility is shared across many systems.

### Hierarchical

DNS is hierarchical. Names are organized in layers.

```text
ROOT
 |
.com
 |
example
 |
www / mail
```

Examples of top-level domains:

- `.com`
- `.org`
- `.net`
- `.us`
- `.ca`
- `.uk`

For A+, focus on the idea of hierarchy and name resolution, not deep DNS infrastructure design.

## Resource Records

DNS stores data in **resource records**.

| Record | Purpose | Memory Tip |
| --- | --- | --- |
| A | IPv4 address | A → IPv4 |
| AAAA | IPv6 address | AAAA → IPv6 |
| CNAME | Alias | Nickname |
| MX | Mail exchanger | M = Mail |
| TXT | Text information | Text |

### A Record

An A record maps a hostname to an IPv4 address.

Exam clue: IPv4 → A

### AAAA Record

An AAAA record maps a hostname to an IPv6 address.

Exam clue: IPv6 → AAAA

Clear comparison:

- A = IPv4
- AAAA = IPv6

### CNAME Record

A CNAME record creates an alias.

The alias points to another canonical hostname.

Nickname analogy: Robert / Bobby. Bobby still refers to Robert.

Important: A CNAME points to another hostname, not directly to an IP address.

### MX Record

An MX record identifies the mail exchanger for a domain.

Exam clue: Mail exchanger → MX

### TXT Record

A TXT record stores text information in DNS.

Common uses include:

- Domain verification
- Email-related configuration
- Other published text values

Remember: TXT is broader than email. It can store many kinds of text.

## TTL

TTL stands for Time to Live.

TTL controls how long DNS information can remain cached before it should be requested again.

Directions analogy: If someone just told you where the cafeteria is, you do not ask again 30 seconds later. You remember it for a while.

Memory tip: TTL → Cache duration

## SPF, DKIM, and DMARC

These email authentication technologies often appear with DNS.

| Technology | Think | Key Question |
| --- | --- | --- |
| SPF | Authorized sending servers | Who is authorized to send? |
| DKIM | Digital signature | Can the signature be verified? |
| DMARC | Policy + reporting | What should happen when authentication fails? |

### SPF

SPF helps identify which servers are authorized to send email for a domain.

### DKIM

DKIM helps verify a digital signature on an email message.

### DMARC

DMARC provides policy and reporting guidance when authentication fails.

## SPF vs DKIM vs DMARC Comparison

Keep these separate:

- SPF answers authorization
- DKIM answers signature verification
- DMARC answers policy and reporting

If an exam question mentions authorized senders, think SPF.  
If it mentions a digital signature, think DKIM.  
If it mentions what to do when authentication fails, think DMARC.

## CompTIA Scenario Recognition

| Scenario Clue | Best Match |
| --- | --- |
| Hostname to IPv4 | A |
| Hostname to IPv6 | AAAA |
| Alias hostname | CNAME |
| Mail receiving server | MX |
| Publish text in DNS | TXT |
| Cache duration | TTL |
| Authorized email senders | SPF |
| Email digital signature | DKIM |
| Authentication failure policy | DMARC |
| IP works, hostname fails | DNS / name resolution |

## Final Memory Map

| Term | Remember |
| --- | --- |
| DNS | Name resolution |
| A | IPv4 |
| AAAA | IPv6 |
| CNAME | Alias |
| MX | Mail |
| TXT | Text |
| TTL | Cache duration |
| SPF | Authorized sender |
| DKIM | Digital signature |
| DMARC | Policy + reporting |

---

## Continue Learning

- Lesson: [DNS Configuration](../core-1/2-networking/2.4-dns-configuration.md)
- Activity: [DNS Record Matching Challenge](../activities/dns-record-matching.md)
- Next Topic: [DHCP](../core-1/2-networking/2.4-dhcp.md)
- Back to [Study Guides](README.md)
