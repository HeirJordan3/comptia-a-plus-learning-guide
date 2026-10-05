# Authentication and Access

CompTIA A+ Core 2 — 220-1202  
Objective 2.1 — Summarize various security measures and their purposes

## What You Need to Know

By the end of this lesson, you should understand:

- How **SAML** lets a web app trust a separate login server
- What **single sign-on (SSO)** saves, and that the session times out
- How **just-in-time** access and **PAM** protect administrator accounts
- What **MDM** does for company phones and **BYOD**
- Where **DLP** watches sensitive data
- What **IAM** and **directory services** (such as Active Directory) are for

## What Is It?

**Authentication** proves who is signing in. **Access** decides what that person or device may open afterward. This lesson is the set of systems that do both: a shared login for web apps, short-lived admin rights, phone management, and one directory of users and resources.

## Why Does It Matter?

People no longer use one app on one server in one building. Employees, customers, and contractors reach desktops, phones, and cloud apps. Help desk work is password resets, phone policies, and “why can’t this person open that folder.” The exam asks which system matches that job.

## Real-World Analogy

Think of a large office campus with a badge office:

| Campus practice | IT equivalent |
| --- | --- |
| One badge opens the garage, the lobby, and the gym | Single sign-on |
| The front desk sends you to security to prove who you are, then the gym lets you in | SAML |
| A master key is checked out for one hour, then it stops working | Just-in-time access |
| Facilities tracks every master key in a safe | Privileged access management |
| The company sets a PIN on phones it manages | Mobile device management |
| Mailroom stops a package labeled with customer card numbers | Data loss prevention |
| HR file plus the badge database | Identity and access management / directory services |

## How It Works

### SAML

**SAML** is the **Security Assertion Markup Language**. It is an open standard. A web app does not store every password itself. It asks a different authentication source to approve the user.

SAML fits **web** apps in a browser. It was not designed for mobile apps, so a phone app may use a different login process.

Three parts take part in the flow:

| Part | Role |
| --- | --- |
| Client | Your laptop, usually in a browser |
| Resource server | The app you want |
| Authorization server | Checks your credentials |

1. The browser opens a URL on the resource server.
2. That server sends back a **signed and encrypted SAML request**. The request points the browser to the authorization server.
3. You see a login page and enter your credentials.
4. If they match, the authorization server builds a **SAML token** and gives it to the client.
5. The client presents that token to the resource server.
6. The resource server trusts the token and opens the app.

The app never had to collect the password itself. It trusted the signed token.

### Single Sign-On

**Single sign-on (SSO)** means you do not type a username and password again for every resource on that network. SAML is often the method that makes SSO work for web apps.

The session is not permanent. It **times out**, often after about 24 hours. When the timer ends, you sign in again and get another window of access.

SSO only works if the authentication process in use supports it. Not every protocol does.

### Just-in-Time Access

Someone in IT must be able to administer systems. Putting those rights on their everyday login is dangerous. If an attacker steals that login, they are an administrator.

**Just-in-time (JIT) access** grants administrator rights only for a short time, then removes them.

Typical path:

1. The IT person requests elevated access from a central service.
2. That request uses extra authentication.
3. The real administrator account stays in a **password vault**. Nobody is handed those original credentials.
4. The system creates a **new** administrator account with **ephemeral** (short-lived) credentials.
5. When the time ends, those credentials are deleted and cannot be reused.

An attacker who later steals the IT user’s normal account still does not have administrator rights.

### Privileged Access Management

**Privileged Access Management (PAM)** is how an organization controls super-user accounts: a Windows administrator, a Linux **root** account, or any login with extra rights. Just-in-time access is one part of PAM.

PAM also:

- Keeps those accounts in a protected vault
- Can automate checkout of access
- Records an audit of who received rights and when

### Mobile Device Management

**Mobile device management (MDM)** is one console for phones and tablets that are always moving. The devices may be company-owned, or they may be personal phones people brought to work. Personal devices are **BYOD** (**bring your own device**).

From that console an administrator can:

- See where devices are
- Set what each device is allowed to do
- Choose which apps may run
- Require a lock screen and a PIN
- Put company data in a **separate partition** from personal data

On a BYOD phone, that split matters when someone leaves. MDM can wipe the **company** data and leave the person’s own photos and files in place.

### Data Loss Prevention

**Data loss prevention (DLP)** watches sensitive data and applies rules about where it may go. Examples: Social Security numbers, credit card numbers, medical records, and other personal data.

Organizations usually run DLP in more than one place:

| Location | What it watches |
| --- | --- |
| Endpoint client | The PC or phone |
| Cloud systems | Files stored with a cloud provider |
| Email server | Messages leaving the company |
| Firewall | Traffic crossing the network |

Data that meets policy can go to the right destination. Data sent in the clear, or to the wrong place, is stopped before someone who should not see it receives it.

### Identity and Access Management

Apps now sit on desktops, on phones, in a private data center, and in more than one cloud. The people using them are employees, customers, and contractors. A customer should see only their own data. An employee may need more.

**Identity and access management (IAM)** gives every person and every device a **digital identity**, then manages that identity over its life:

- Authentication and authorization, including multifactor login
- Access limited to the data that role needs
- Proof that the account matches the real person
- An audit of who opened which resource, and when

Some industries must keep that record. IAM is how they show where the data lives and who touched it.

### Directory Services

Administrators also need one database for the network’s resources: servers, user accounts, file shares, printers, and more. That database is **directory services**.

On a Microsoft network, the usual directory is **Active Directory**. Because the records are in one place, one console can:

- Store usernames and passwords securely
- Decide which folders and printers each login may use
- Reset a password when the help desk takes the call

## Side-by-Side Comparison

| System | Main job |
| --- | --- |
| SAML | A web app accepts a signed token from another login server |
| SSO | One login covers many resources until it times out |
| JIT | Admin rights exist only for a short task |
| PAM | Vault, automation, and audit for super-user accounts |
| MDM | One console for phones, including BYOD company data |
| DLP | Stop sensitive data from leaving the wrong way |
| IAM | Identity, access, and audit for people and devices |
| Directory services | One database of users and network resources |

## Key Terms

| Term | Meaning |
| --- | --- |
| SAML | Security Assertion Markup Language; an open standard for web-app login |
| SAML token | The signed proof the client shows to the app after login |
| Authorization server | The server that checks credentials and issues the token |
| Resource server | The app or data the user is trying to open |
| SSO | Single sign-on; one login for many resources |
| JIT access | Administrator rights granted only for a limited time |
| Ephemeral credentials | A temporary login that is deleted when time runs out |
| Password vault | Where the real administrator passwords stay |
| PAM | Privileged Access Management for super-user accounts |
| Root | The Linux super-user account |
| MDM | Mobile device management from one console |
| BYOD | Bring your own device; a personal phone or tablet used for work |
| DLP | Data loss prevention; rules for sensitive data in motion |
| IAM | Identity and access management across apps and clouds |
| Digital identity | The account record for a person or a device |
| Directory services | One database of users and network resources |
| Active Directory | Microsoft’s directory service |

## CompTIA Exam Connections

| Clue | Think |
| --- | --- |
| Web app uses another system to log you in | SAML |
| Signed token presented to the app | SAML token |
| Mobile app does not use this web standard | SAML was not designed for mobile apps |
| One password opens many internal apps | SSO |
| Asked to sign in again the next day | SSO session timed out |
| Everyday IT account is not a full administrator | Just-in-time access |
| New admin login disappears after the task | Ephemeral credentials |
| Real admin password never leaves the safe | Password vault |
| Windows admin and Linux root tightly controlled | PAM |
| Company sets a PIN and allowed apps on phones | MDM |
| Personal phone; company data removed at offboarding | BYOD plus MDM partition wipe |
| Credit card numbers blocked in email | DLP |
| DLP on the PC, in the cloud, in email, and on the firewall | More than one DLP location |
| Customers see only their own records | IAM |
| One database of users, shares, and printers | Directory services |
| Help desk resets a Windows domain password | Active Directory |

## Common Mix-Ups

### SAML is the app storing your password

The **authorization server** checks the password and issues a token. The **resource server** trusts that token. The web app does not have to keep its own copy of every password.

### SSO means you never sign in again

The session **expires**. A common window is about a day. After that you authenticate again. The protocol in use also has to support SSO.

### Just-in-time access hands out the domain admin password

The original administrator account stays in the **vault**. JIT creates a **separate, temporary** admin login and deletes it when time runs out.

### MDM always erases the whole phone

On **BYOD**, company data can sit in its own partition. When the person leaves, MDM can remove the company data and leave personal data on the device.

### DLP is only an email filter

Email is one place. The same idea also runs on endpoints, in cloud storage, and on the firewall.

### IAM and Active Directory are different jobs with no overlap

**Active Directory** is a directory service: one database of users and resources, common on Windows networks. **IAM** is the broader life cycle of identities and access, including customers and cloud apps. A help-desk password reset on a Windows domain is directory services. Deciding that a customer may see only their own cloud data is IAM.

## Quick Review

| Topic | Remember |
| --- | --- |
| SAML | Browser, resource server, authorization server, then a token |
| SSO | One login, many resources, then a timeout |
| JIT | Short-lived admin account; original password stays in the vault |
| PAM | Vault, automation, and audit for admin and root |
| MDM | One console; lock screen, apps, company partition |
| BYOD | Wipe company data, keep personal data |
| DLP | Watch SSN, cards, medical data on PC, cloud, email, firewall |
| IAM | A digital identity and an audit for each person and device |
| Directory | Active Directory: users, shares, printers, password resets |

---

## Continue Learning

- Previous Topic: [Logical Security](logical-security.md)
- Next Topic: [Defender Antivirus](defender-antivirus.md)
- Related: [Physical Access Security](physical-access-security.md)
- Back to [Domain 2 — Security](README.md)
- Course Map: [Core 2 Study Path](../COURSE-MAP.md)
