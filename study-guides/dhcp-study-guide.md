# DHCP Study Guide

CompTIA A+ Core 1 — 220-1201  
Objective 2.4 — Network Configurations

Use this guide after the DHCP lesson for deeper review and exam recognition practice.

## What DHCP Is

DHCP stands for Dynamic Host Configuration Protocol.

DHCP automatically provides network configuration to devices so users do not have to enter every setting by hand.

That configuration may include:

- IP address
- Subnet mask
- Default gateway
- DNS server
- Lease information
- Other network options

## Why DHCP Exists

Manual configuration does not scale well.

If every laptop, phone, and workstation needed a technician to type in network settings, day-to-day support would become slow and error-prone.

DHCP solves that by handing out settings automatically.

Coffee shop example: When you join Wi-Fi, you usually do not configure an IP address yourself. DHCP handles much of that work.

Useful comparison:

- DNS helps you find an address
- DHCP gives you your network configuration

## Static vs Dynamic Configuration

### Static

A static IP address is configured manually on the device.

It can be useful for some servers, printers, or network devices, but it requires careful documentation and more manual effort.

### Dynamic

A dynamic configuration is provided automatically by DHCP.

This is the normal approach for most end-user devices.

## DORA

DHCP uses a four-step process remembered as **DORA**:

```text
CLIENT                    DHCP SERVER

Discover  -------------->
          Anyone there?

          <-------------- Offer
          Use this address.

Request   -------------->
          I'll take it.

          <-------------- Acknowledge
          It's yours.
```

Meaning of each step:

- Discover = Find DHCP
- Offer = Here is an address
- Request = I want that one
- Acknowledge = Approved

Exam tip: If you see Discover, Offer, Request, and Acknowledge, think DHCP and DORA.

## Broadcast Concept

Early in the DHCP process, the client often uses broadcast communication.

Why? The client may not yet know the DHCP server and may not have normal IP configuration yet.

Analogy: Walking into a room and asking, “Is anyone here who can help me?”

That is the idea behind Discover.

## UDP 67 and 68

| Device | Port |
| --- | --- |
| DHCP Server | UDP 67 |
| DHCP Client | UDP 68 |

Memory tip:

- Server = 67
- Client = 68

## Scope

A **scope** is the overall DHCP configuration for a network.

A scope may include:

- IP address range
- Exclusions
- Subnet mask
- Lease duration
- DNS server
- Default gateway
- Other configuration options

Think of the scope as the full DHCP setup for that network segment.

## Pool

A **pool** is the set of addresses available for DHCP assignment.

If a scenario says `192.168.10.100` through `192.168.10.199` are available for clients, that range is acting as a pool.

## Exclusion

An **exclusion** identifies addresses that DHCP should not dynamically assign.

Example: Keep the router address out of the dynamic handout range so another device does not receive it.

Exam clue: “Do not dynamically assign” → Exclusion

## Lease

A **lease** is a temporary assignment of an IP address.

Hotel analogy: You use the room for a period of time, but you do not own it forever.

When the lease ends, the address may be renewed or returned to the pool.

Exam clue: Temporary assignment → Lease

## Reservation

A **reservation** allows a particular device to receive the same IP address through DHCP every time.

DHCP uses the device’s MAC address to identify it.

Association:

MAC address → Reserved IP address

You may also hear:

- DHCP reservation
- IP reservation
- Static DHCP assignment

## MAC Address

A MAC address is the hardware address of a network interface.

For reservations, the MAC address is how DHCP knows which device should always receive which IP address.

## Static IP vs Reservation

These are related but not the same.

| Approach | How It Works |
| --- | --- |
| Static IP | Configured manually on the device |
| DHCP reservation | DHCP still assigns the address, but always the same one for that MAC address |

If a printer needs `192.168.10.150` every time through DHCP, configure a reservation. That is different from typing a static IP directly into the printer.

## CompTIA Scenario Recognition

| Scenario Clue | Best Match |
| --- | --- |
| Automatic IP configuration | DHCP |
| Discover / Offer / Request / Acknowledge | DORA |
| DHCP server port | UDP 67 |
| DHCP client port | UDP 68 |
| Available address range | Pool |
| Do not hand out this address dynamically | Exclusion |
| Temporary IP assignment | Lease |
| Same device always gets the same IP via DHCP | Reservation |
| Identifier used for a reservation | MAC address |

## Final Memory Map

| Term | Remember |
| --- | --- |
| DHCP | Automatic network configuration |
| DORA | Discover → Offer → Request → Acknowledge |
| UDP 67 | Server |
| UDP 68 | Client |
| Scope | Overall DHCP configuration |
| Pool | Available addresses |
| Exclusion | Do not dynamically assign |
| Lease | Temporary assignment |
| Reservation | Same device receives same IP |
| MAC Address | Identifies device for reservation |

---

## Continue Learning

- Lesson: [DHCP](../core-1/2-networking/2.4-dhcp.md)
- Activity: [DHCP Scenario Challenge](../activities/dhcp-scenario-challenge.md)
- Next Topic: [VLANs and VPNs](../core-1/2-networking/2.4-vlans-and-vpns.md)
- Back to [Study Guides](README.md)
