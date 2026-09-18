# HSM and TPM

CompTIA A+ Core 1 — 220-1201  
Objective 3.5 — Motherboards, CPUs, and Add-on Cards

## What You Need to Know

By the end of this lesson, you should understand:

- Why encryption needs protected keys
- What a TPM is and where it lives
- What a TPM does (crypto processor, keys, secure storage)
- How TPM supports full-disk encryption (for example, BitLocker)
- What “root of trust” means in plain language
- How TPM can be enabled or cleared in BIOS/UEFI
- What an HSM is and when it is used
- How TPM and HSM differ

## What Is It?

**TPM** and **HSM** are hardware tools that protect **cryptographic keys** — the secret digital “keys” used for encryption and decryption.

- **TPM** = **Trusted Platform Module** — usually for **one computer**
- **HSM** = **Hardware Security Module** — usually for **many systems** / a data center

Encryption methods are often public standards. Security comes from keeping the **key** secret — like knowing how a door lock works, but still needing the unique key to open it.

## Why Does It Matter?

Techs see TPMs and HSMs when:

- Enabling BitLocker or other full-disk encryption
- A drive is moved to another PC and the data will not decrypt
- BIOS shows TPM / TCG options
- A company stores web server or certificate authority keys in a central secure device
- Comparing “chip on the motherboard” vs “appliance in the data center”

Exam questions often ask: TPM vs HSM, BitLocker + TPM, or keys tied to one device.

## Real-World Analogy

- **TPM** = a **safe welded into one house**. The valuables (keys) stay with that house. You cannot easily move the safe to another house and open it the same way.
- **HSM** = a **bank vault** that many branches use. Many systems store and use keys in one highly protected place.

## How It Works

### The Key Problem

We encrypt:

- Phones (storage and wireless)
- Web traffic
- Hard drives and SSDs

If data is encrypted with a key, we must protect that key. Storing keys only as ordinary files on the same drive is weaker. Hardware modules help keep keys safer.

### Trusted Platform Module (TPM)

A **TPM** is standardized security hardware built for cryptography.

It may be:

- Built into the motherboard, or
- A separate module installed on the motherboard

What a TPM typically includes:

| Part | Role |
| --- | --- |
| Cryptographic processor | Random numbers, key generation, crypto functions |
| Persistent memory | Keys burned in at manufacture (unique to that TPM) |
| Versatile memory | Stores keys and related data during use |
| Security protections | Password-protected features that resist key theft |

Important idea: the TPM holds a secret that is **unique to that system**. Nobody else has the same key.

### TPM Use Cases

**Full-disk encryption (example: BitLocker)**

- TPM helps protect the keys used to encrypt the drive
- Keys are associated with **that computer**
- Pulling the drive out and putting it in another PC usually does **not** give easy access — decryption still needs the original TPM-backed key material

**Root of trust**

- Because the TPM is unique and hardware-tied, the system can be treated as a trusted identity
- Helps confirm you are talking to the expected physical machine

**Remote integrity ideas**

- TPM-related features can help detect whether a system has changed from what you expect when connecting over the network

Because the TPM is physical hardware, it is hard to simply copy and move to another computer.

### Enabling TPM in BIOS/UEFI

TPM features are often under **Security**.

You may see **TCG** — **Trusted Computing Group** (the group behind TPM standards).

Typical options:

- Enable or disable the TPM (example: TPM 2.0 security chip)
- Clear data stored in the TPM
- Configure how TPM data is deleted

Clearing a TPM can affect disk encryption and other features that depend on those keys — document and understand first.

### Hardware Security Module (HSM)

An **HSM** is a hardware device (or appliance) for managing keys at a larger scale.

Why HSM instead of only TPM?

- A data center may have hundreds or thousands of devices
- Each may need keys
- Organizations need centralized, protected key management

HSM roles:

| Role | Example |
| --- | --- |
| Central key storage / backup | Store many web server keys in one protected place |
| Crypto acceleration | Offload encryption/decryption from servers into HSM hardware |
| Protect high-value keys | Web server TLS keys, certificate authority keys |

Forms of HSM:

- High-end data center appliances with cryptographic hardware
- Lightweight / personal HSMs (portable devices for personal keys — for example, some cryptocurrency hardware wallets)

### TPM vs HSM

| | TPM | HSM |
| --- | --- | --- |
| Scale | Usually **one** system | Usually **many** systems |
| Location | Built into board or add-on module | Often data center appliance (or portable personal unit) |
| Main job | Protect keys / trust on that device | Centralize and protect keys for infrastructure |
| Everyday PC example | BitLocker, device encryption, boot security features | Not typical for a single home PC |
| Enterprise example | Each laptop has its own TPM | Web farm / CA keys in an HSM |

## Key Terms

| Term | Meaning |
| --- | --- |
| Encryption | Scrambling data so it needs a key to read |
| Cryptographic key | Secret value used to encrypt/decrypt |
| TPM | Trusted Platform Module — device-level crypto hardware |
| HSM | Hardware Security Module — centralized (or dedicated) key hardware |
| BitLocker | Windows full-disk encryption that can use TPM |
| Root of trust | Hardware-based foundation for trusting a system |
| TCG | Trusted Computing Group — TPM standards organization |
| Persistent keys | Keys fixed in the TPM at manufacture |
| Crypto acceleration | Doing encryption in specialized hardware for speed/security |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Chip on motherboard for encryption / BitLocker | TPM |
| Drive moved to another PC will not decrypt easily | Keys tied to original TPM |
| Enable TPM in firmware | BIOS Security / TCG / TPM 2.0 |
| Clear TPM | Can wipe TPM-stored key material — high impact |
| Many servers’ keys in one secure appliance | HSM |
| Offload TLS crypto from web servers | HSM |
| Single device vs many devices | TPM vs HSM |
| Portable personal key device | Lightweight / personal HSM |

## Common Mix-Ups

### TPM vs HSM

- **TPM** = one computer’s hardware trust/crypto helper
- **HSM** = shared or dedicated module for larger key management (often data center)

### Encryption algorithm vs the key

Public standards explain *how* encryption works. Security still depends on protecting the **key**.

### TPM vs antivirus

Antivirus watches software behavior. TPM protects cryptographic keys and hardware-rooted trust.

### “Remove the drive to bypass encryption”

If encryption keys are TPM-backed, moving the drive alone usually is **not** enough to read the data.

### Clearing TPM casually

Clearing TPM can break BitLocker/recovery unless recovery keys are available. Treat it like a security-sensitive change.

## Quick Review

| Topic | Remember |
| --- | --- |
| Why TPM/HSM | Protect encryption keys in hardware |
| TPM | Single system; motherboard chip/module |
| BitLocker | Common TPM use case |
| Root of trust | Unique hardware-tied identity |
| BIOS | Enable/disable/clear TPM under Security / TCG |
| HSM | Many systems; data center key vault / crypto hardware |
| Compare | TPM = one device; HSM = centralized / multi-system |

---

## Continue Learning

- Previous Topic: [BIOS Settings](bios-settings.md)
- Next Topic: [CPU Features](cpu-features.md)
- Related: [The BIOS](the-bios.md)
- Back to [Domain 3 — Hardware](README.md)
