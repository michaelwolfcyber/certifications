# Domain 4 — Networking and Cloud Security Concepts

**Exam weight:** 21.3%  
**Current CC exam outline:** Effective September 1, 2026

> Built from my Domain 4 notes and the ISC2 Domain 4 course/resource material. The 2026 objectives are the main structure; additional ISC2 course concepts are included where they help with understanding and scenario questions.

---

# 2026 Domain Objectives

## 4.1 Understand network security

- Network security concepts
- OSI model
- TCP/IP model
- IPv4
- IPv6
- VPN
- Ports/applications
- Firewalls
- Wireless
- Embedded systems
- ICS
- IoT

## 4.2 Understand network security architecture

- Network segmentation
- Firewall zones
- VLAN
- Micro-segmentation
- Defense in Depth
- Zero Trust
- Network Access Control (NAC)
- DMZ
- Segmentation for embedded systems and IoT

## 4.3 Understand cloud security

- Cloud characteristics
- Service models
- Deployment models
- Shared security model
- SLA
- MSP

---

# 4.1 Network Security

## What is a network?

A network is a group of connected devices that communicate and share resources.

Common network types include:

| Type | Meaning | Example |
|---|---|---|
| LAN | Local Area Network | Office or home network |
| WAN | Wide Area Network | Network connecting offices across cities |
| WLAN | Wireless LAN | Wi-Fi network |
| VPN | Virtual Private Network | Secure connection over the Internet |
| PAN | Personal Area Network | Bluetooth devices around a person |
| CAN | Campus Area Network | University or corporate campus |
| MAN | Metropolitan Area Network | Network spanning a city |
| SAN | Storage Area Network | Dedicated network for storage |
| VLAN | Virtual LAN | Logical network separation |

**Example:** Your home Wi-Fi is a WLAN. Your router connects that local network to the Internet.

**Think:** Network security is about protecting the devices, communications, and services that make up the network.

---

# OSI Model

The **Open Systems Interconnection (OSI) model** divides network communication into seven conceptual layers.

| Layer | Name | What to associate with it |
|---:|---|---|
| 7 | Application | Network services used by applications |
| 6 | Presentation | Data representation, formatting, encryption |
| 5 | Session | Establishing/managing communication sessions |
| 4 | Transport | End-to-end delivery, TCP/UDP |
| 3 | Network | IP addressing and routing |
| 2 | Data Link | Frames, MAC addresses, switching |
| 1 | Physical | Bits, cables, radio signals |

### Memory aid

**All People Seem To Need Data Processing**

Application → Presentation → Session → Transport → Network → Data Link → Physical

### Why it matters

The OSI model gives you a way to reason about where networking functions and security problems occur.

**Example:** An IP address is associated with Layer 3, while a MAC address is associated with Layer 2.

**Exam clue:**
- IP addressing/routing → Layer 3
- MAC addresses/frames → Layer 2
- TCP/UDP → Layer 4

---

# TCP/IP Model

The TCP/IP model is the practical networking model used by the Internet.

A common four-layer representation is:

1. Application
2. Transport
3. Internet
4. Network Access

| OSI | TCP/IP |
|---|---|
| Application | Application |
| Presentation | Application |
| Session | Application |
| Transport | Transport |
| Network | Internet |
| Data Link | Network Access |
| Physical | Network Access |

**Example:** HTTP belongs to the Application layer, TCP to the Transport layer, and IP to the Internet layer.

**Remember:** OSI is especially useful as a conceptual framework; TCP/IP describes the protocol architecture used by real-world Internet communications.

---

# Encapsulation and De-encapsulation

**Encapsulation** is the process of adding protocol information as data moves down the networking stack.

**De-encapsulation** is the reverse process as the receiving system processes the data upward.

**Example:** Application data receives transport information, then network information, then data-link information before transmission. The receiver reverses the process.

**Think:** Encapsulation = package it. De-encapsulation = unpack it.

---

# Packets, Frames, and Payloads

A **packet** is associated with the Network layer (Layer 3).

A **frame** is associated with the Data Link layer (Layer 2).

A **payload** is the useful data carried inside a protocol unit.

**Example:** A packet can contain addressing information plus a payload containing part of an application message.

---

# IPv4

IPv4 uses **32-bit IP addresses**.

Example:

`192.168.1.25`

IPv4 has a much smaller address space than IPv6.

**Exam clue:** IPv4 = 32-bit.

# IPv6

IPv6 uses **128-bit IP addresses**.

Example:

`2001:db8::1`

IPv6 provides a vastly larger address space.

| IPv4 | IPv6 |
|---|---|
| 32-bit | 128-bit |
| Smaller address space | Much larger address space |
| `192.168.1.10` | `2001:db8::1` |

**Exam clue:** If the question focuses on address size, remember **32 vs. 128 bits**.

---

# Ports and Applications

A **port** identifies a network service or application endpoint. Ports allow multiple services to operate on the same host.

| Port | Service | Typical use |
|---:|---|---|
| 21 | FTP | File transfer |
| 22 | SSH | Secure remote administration |
| 23 | Telnet | Remote access; insecure |
| 25 | SMTP | Email transfer |
| 53 | DNS | Name resolution |
| 80 | HTTP | Web traffic |
| 110 | POP3 | Email retrieval |
| 123 | NTP | Time synchronization |
| 143 | IMAP | Email retrieval |
| 161/162 | SNMP | Network management |
| 389 | LDAP | Directory services |
| 443 | HTTPS | Secure web traffic |
| 445 | SMB | File/printer sharing |
| 636 | LDAPS | Secure LDAP |
| 993 | IMAPS | Secure IMAP |
| 3389 | RDP | Remote desktop |

**Example:** HTTPS normally uses port 443.

**Exam clue:** Know what the service does, not just the number.

---

# Protocols

A **protocol** is a defined set of rules used for communication between systems.

Examples:

- HTTP/HTTPS — web communication
- DNS — name resolution
- SSH — secure remote administration
- SMTP — email transmission
- FTP — file transfer
- SNMP — network management
- NTP — time synchronization
- TCP — reliable transport
- UDP — connectionless transport

### Secure vs. insecure protocols

Common comparisons:

- HTTP → HTTPS
- Telnet → SSH
- FTP → SFTP/FTPS
- LDAP → LDAPS

**Example:** Using Telnet for administration can expose credentials and data; SSH provides protected remote administration.

---

# TCP and UDP

## TCP

**Transmission Control Protocol (TCP)** provides reliable, connection-oriented communication.

It uses mechanisms such as acknowledgments and sequencing.

**Example:** HTTPS commonly uses TCP because reliable delivery matters.

## UDP

**User Datagram Protocol (UDP)** is connectionless and does not provide TCP-style delivery guarantees.

It can be useful when speed and low overhead are more important than guaranteed delivery.

**Example:** Some real-time voice, video, and gaming traffic uses UDP.

**Think:** TCP = reliability. UDP = connectionless/low overhead.

---

# VPN

A **Virtual Private Network (VPN)** creates a protected communication path across an untrusted or shared network.

**Example:** An employee working from home connects to the company VPN to reach internal resources over the Internet.

**Why it matters:** A VPN can protect communications while they cross a network the organization does not control.

**Remember:** VPN = protected path over a shared/untrusted network.

A VPN does not automatically make the endpoint trustworthy. Authentication, authorization, device security, and other controls still matter.

---

# Firewalls

A **firewall** controls network traffic according to defined rules.

Rules can consider:

- Source/destination addresses
- Ports
- Protocols
- Applications
- Network zones

**Example:** A firewall might allow inbound HTTPS traffic to a public web server while blocking unsolicited inbound RDP.

## Firewall zones

Firewalls can separate network areas into security zones with different access rules.

**Example:**

```text
Internet
   |
Firewall
   |
  DMZ  ---> Public web server
   |
Internal firewall
   |
Internal network ---> Employee systems
```

The important idea is that different zones can have different trust and access rules.

---

# Wireless Security

Wireless networks use radio rather than physical network cables.

Security concerns include:

- Unauthorized devices
- Weak authentication
- Weak encryption
- Rogue access points
- Eavesdropping
- Misconfiguration

**Example:** An attacker creates a rogue access point that looks like legitimate company Wi-Fi. Employees connect to it, potentially exposing traffic.

**Remember:** Wireless convenience does not mean automatic security.

---

# Bluetooth

Bluetooth provides short-range wireless communication.

Security considerations include:

- Pairing
- Authentication
- Unauthorized devices
- Device visibility/discoverability

**Example:** An organization might restrict Bluetooth on sensitive systems to reduce unauthorized wireless connections.

---

# Embedded Systems

An embedded system is a computing system built into another device for a specific function.

Examples:

- Medical devices
- Industrial equipment
- Building systems
- Vehicle systems
- Network appliances

Security concerns can include:

- Long lifecycles
- Limited resources
- Specialized software
- Difficult patching
- Safety or availability requirements

**Example:** An industrial device may be difficult to patch because taking it offline could interrupt a critical process.

---

# ICS — Industrial Control Systems

**Industrial Control Systems (ICS)** control or monitor industrial processes.

Examples include:

- Manufacturing
- Utilities
- Energy
- Water treatment

Security priorities can place strong emphasis on **availability and safety**.

**Example:** Compromising an industrial control system could interrupt production or create a physical safety hazard, not just cause data loss.

**Exam clue:** Industrial processes + physical equipment + safety → think ICS/OT.

---

# IoT — Internet of Things

IoT devices are physical devices that connect to networks and often collect, process, or transmit data.

Examples:

- Cameras
- Smart sensors
- Smart appliances
- Building sensors
- Wearable devices

Common concerns:

- Weak/default credentials
- Poor patching
- Limited resources
- Large numbers of devices
- Difficult asset management
- Network exposure

**Example:** A company deploys hundreds of network-connected sensors. If one is compromised, segmentation can help prevent it from becoming a path into sensitive systems.

---

# 4.2 Network Security Architecture

## Network Segmentation

**Network segmentation** divides a network into separate security zones.

Benefits include:

- Limiting lateral movement
- Isolating systems
- Reducing attack surface
- Containing compromises
- Applying different security policies

**Example:** A company separates employee workstations from database servers. Compromising a workstation does not automatically give an attacker unrestricted access to the database network.

**Exam clue:** If the question asks how to limit an attacker's movement after an initial compromise, think segmentation.

---

# DMZ — Demilitarized Zone

A **DMZ** is a network segment used to isolate systems that need to be reachable from less-trusted networks such as the Internet.

Common DMZ systems:

- Public web servers
- Public DNS servers
- Email gateways
- Reverse proxies

**Example:**

```text
Internet
    |
 Firewall
    |
   DMZ
  /   Web   Mail Gateway
Servers
    |
 Internal Firewall
    |
Internal Network
```

A public web server can be exposed without placing it directly on the same network as sensitive internal systems.

**Think:** DMZ = controlled zone for externally accessible systems.

---

# VLAN

A **Virtual Local Area Network (VLAN)** logically separates network traffic even when devices share physical switching infrastructure.

**Example:**

```text
VLAN 10 → Employees
VLAN 20 → Servers
VLAN 30 → Guest Wi-Fi
```

The devices can use the same physical switches while remaining logically separated.

**Exam clue:** Logical network separation on shared physical infrastructure → VLAN.

---

# Micro-Segmentation

**Micro-segmentation** applies segmentation at a much more granular level, potentially between individual workloads, systems, applications, or services.

**Example:** Instead of putting every application server into one large server network, an organization can create separate policies for individual workloads and tightly control which workloads can communicate.

**Think:**

> Segmentation = separate networks/zones.  
> Micro-segmentation = smaller, more granular security boundaries.

Micro-segmentation is also closely associated with Zero Trust architectures.

---

# Network Access Control (NAC)

**Network Access Control (NAC)** controls whether devices are allowed to connect to a network and/or what network access they receive.

NAC can consider:

- Device identity
- User identity
- Authentication
- Security posture
- Compliance requirements

**Example:** A laptop connects to the corporate network. NAC checks whether it is authorized and meets security requirements. A noncompliant device could be denied access or placed on a restricted network.

**Exam clue:** Controlling whether a device can obtain network access → NAC.

---

# Segmentation for Embedded Systems and IoT

Embedded and IoT devices may have weaker security controls or longer lifecycles than normal endpoints.

Segmentation can reduce their exposure.

**Example:** A company places building-management sensors on a dedicated network instead of allowing direct communication with employee workstations.

**Why:** If an IoT device is compromised, segmentation can help prevent the compromise from spreading.

---

# Defense in Depth

**Defense in Depth** uses multiple layers of security rather than relying on one control.

Possible layers:

1. Physical controls
2. Network controls
3. Endpoint controls
4. Identity/access controls
5. Monitoring

**Example:** A server may be protected by a locked data center, firewall, segmentation, strong authentication, endpoint security, and logging.

If one control fails, other layers can still provide protection.

**Think:** Defense in depth = don't bet everything on one control.

This connects directly to Domain 1's security-control concepts.

---

# Zero Trust

Zero Trust removes the assumption that a user or device should automatically be trusted simply because it is inside the network.

Core ideas:

- Verify explicitly
- Apply least privilege
- Continuously evaluate access

**Example:** An employee is physically inside the office. That alone does not grant access to sensitive systems. The organization still evaluates identity, device, requested resource, and authorization.

**Think:** Zero Trust = location alone does not establish trust.

### Connection to Domain 3

Zero Trust connects directly to **least privilege and logical access controls**.

```text
Identity
   ↓
Authentication
   ↓
Authorization
   ↓
Least privilege
   ↓
Resource access
   ↓
Continuous evaluation
```

---

# 4.3 Cloud Security

## Cloud Computing

Cloud computing provides convenient, on-demand access to shared computing resources that can be rapidly provisioned and released.

The ISC2 material emphasizes:

- Broad network access
- Rapid elasticity
- Measured service
- On-demand self-service
- Resource pooling

---

# Cloud Characteristics

## Broad Network Access

Cloud capabilities can be accessed over networks using supported devices.

**Example:** Employees access a cloud application from authorized laptops over the network.

## Rapid Elasticity

Resources can scale up or down as needed.

**Example:** An online store experiences a large increase in traffic during a sale and adds cloud resources to handle the demand.

**Think:** Elasticity = resources expand and contract with demand.

## Measured Service

Resource usage can be monitored and measured.

**Example:** A customer tracks compute, storage, and network usage.

## On-Demand Self-Service

Customers can provision resources without direct provider interaction for every request.

**Example:** A developer creates a virtual machine through a cloud console instead of submitting a manual request.

## Resource Pooling

Provider resources are pooled to serve multiple customers.

**Example:** A cloud provider operates large pools of servers and dynamically allocates capacity among customers.

---

# Cloud Service Models

The three major models are:

- IaaS
- PaaS
- SaaS

The easiest way to understand them is by asking **how much of the stack the provider manages for you**.

## IaaS — Infrastructure as a Service

The provider supplies infrastructure such as:

- Compute
- Storage
- Networking

The customer generally manages more of the operating system and applications.

**Example:** A company rents virtual machines and storage from a cloud provider and manages its own operating systems and applications.

**Think:** IaaS = infrastructure.

## PaaS — Platform as a Service

The provider supplies a platform for developing and running applications.

The customer focuses more on the application while the provider manages more underlying infrastructure.

**Example:** A development team deploys an application using a managed platform without maintaining the underlying servers.

**Think:** PaaS = platform.

## SaaS — Software as a Service

The provider delivers the application to the customer.

**Example:** A company uses cloud email or collaboration software through a browser.

**Think:** SaaS = software.

| Model | Main idea | Customer focus |
|---|---|---|
| IaaS | Infrastructure | Systems, OS, applications |
| PaaS | Platform | Application development |
| SaaS | Software | Using the application |

---

# Cloud Deployment Models

## Public Cloud

Cloud infrastructure is provided for use by customers through a cloud provider.

**Example:** An organization hosts a web application using resources from a public cloud provider.

## Private Cloud

Cloud infrastructure is dedicated to a particular organization.

**Example:** An organization operates a cloud environment dedicated to its own requirements.

## Community Cloud

The ISC2 course material also includes **community cloud**.

A community cloud is designed for organizations that share concerns such as:

- Mission
- Security requirements
- Policy
- Compliance

**Example:** Several organizations with similar regulatory requirements share a cloud environment designed around those requirements.

## Hybrid Cloud

A **hybrid cloud** combines public and private cloud environments.

**Example:** A company keeps sensitive workloads in a private cloud while using public cloud resources for scalable web applications.

**Think:** Hybrid = combination.

---

# Shared Security Model

Cloud security responsibilities are divided between the cloud provider and the customer.

The exact division depends on:

- Service model
- Provider
- Specific service
- Customer responsibilities

**Important:**

> Moving to the cloud does NOT automatically transfer every security responsibility to the provider.

**Example:** The provider may protect underlying infrastructure while the customer remains responsible for users, authentication, data, permissions, and configuration.

### Connection to Domain 3

If the customer manages accounts and permissions, IAM and least privilege still matter in the cloud.

### Connection to Domain 1

The customer still has to manage risks and apply appropriate controls even when infrastructure is hosted by another organization.

---

# Service-Level Agreement (SLA)

An **SLA** defines agreed service expectations between parties.

It can establish expectations for:

- Availability
- Performance
- Support
- Response times
- Responsibilities

**Example:** A cloud provider's SLA specifies expected service availability and support response times.

**Exam clue:** SLA = agreed service expectations.

---

# Managed Service Provider (MSP)

An **MSP** delivers managed technology or security services to customers.

**Example:** A small business hires an MSP to manage its network equipment, backups, monitoring, and security services.

**Think:** MSP = outside organization managing technology/services for you.

---

# On-Premises Infrastructure

The ISC2 Domain 4 material also covers requirements for on-premises data centers.

Important considerations include:

- Power
- HVAC
- Fire suppression
- Redundancy
- Environmental controls
- Physical security

**Example:** A server room can have excellent network security but still experience an outage if cooling fails and servers overheat.

---

# Redundancy

**Redundancy** means having additional resources/components available so one failure does not necessarily cause a service outage.

Examples:

- Multiple power sources
- Backup generators
- Redundant network links
- Multiple servers
- Redundant storage
- Backup cooling

**Example:** A data center has two independent power sources. If one fails, the other can continue supplying power.

**Think:** Redundancy = reduce single points of failure.

### Connection to Domain 2

Redundancy supports **business continuity and disaster recovery** by helping maintain availability when components fail.

---

# MOU and MOA

The ISC2 course material also introduces:

- **MOU — Memorandum of Understanding**
- **MOA — Memorandum of Agreement**

These are formal documents used to establish an understanding or agreement between organizations or parties.

**Example:** Two organizations working together on a technology project may document responsibilities and cooperation.

---

# Network Threats — ISC2 Course Context

The ISC2 Domain 4 resource includes additional network threats and attacks. These help with scenario questions, but not every older course takeaway should be treated as a separate current 2026 objective.

## Spoofing

**Spoofing** involves falsifying an identity or address to appear to be something else.

**Example:** An attacker falsifies a source address so traffic appears to come from a trusted system.

**Think:** Spoofing = pretending to be something/someone else.

## Denial of Service (DoS)

A **DoS attack** attempts to prevent authorized users from accessing a resource or service.

**Example:** An attacker overwhelms a web server with malicious requests so legitimate users cannot access it.

## Distributed Denial of Service (DDoS)

A **DDoS attack** uses multiple systems to generate attack traffic against a target.

**Example:** A botnet sends huge volumes of traffic toward a company's public web server.

**Think:** DoS = denial of service. DDoS = distributed sources.

## Man-in-the-Middle (MITM)

A **MITM attack** occurs when an attacker positions themselves between communicating parties and can intercept or potentially alter communications.

**Example:** An attacker intercepts traffic between a user and a service and attempts to read or modify the communication.

## Fragmentation Attack

A fragmentation attack manipulates network packet fragmentation in a way that can cause problems for the receiving system or its ability to reconstruct packets.

**Remember:** malicious manipulation of fragmented traffic.

## Oversized Packet Attack

An oversized packet attack deliberately sends a packet larger than the receiving system expects or can properly handle.

**Example:** A vulnerable system crashes or behaves unexpectedly when processing a maliciously oversized packet.

## Phishing

Phishing uses deceptive communications to trick a target into taking an unsafe action.

**Example:** An attacker sends an email that appears to come from a manager and asks an employee to open a malicious link.

**Connection:** This directly connects to Domain 2 security awareness.

## Malware

Malware is malicious software designed to perform unauthorized or harmful actions.

Examples:

- Viruses
- Worms
- Trojans
- Ransomware
- Spyware

---

# Security Technologies — ISC2 Course Context

The ISC2 material also discusses:

- IDS
- NIDS
- HIDS
- SIEM
- Antivirus
- Scanning
- Firewalls
- IPS
- NIPS
- HIPS

## IDS

An **Intrusion Detection System (IDS)** detects and alerts on potentially malicious activity.

**Think:** IDS = detect/alert.

## IPS

An **Intrusion Prevention System (IPS)** is designed to detect and take action to prevent/block malicious activity.

**Think:** IPS = detect + prevent/block.

## NIDS vs. HIDS

- **NIDS:** Network-based detection
- **HIDS:** Host-based detection

## NIPS vs. HIPS

- **NIPS:** Network-based prevention
- **HIPS:** Host-based prevention

## SIEM

A **Security Information and Event Management (SIEM)** system collects and analyzes security-related logs/events from multiple sources.

**Example:** A SIEM can correlate authentication failures, firewall events, and endpoint alerts to help identify suspicious activity.

**Connection to Domain 5:** Logging, monitoring, event triage, and correlation are major Domain 5 concepts.

---

# How Domain 4 Connects to the Other Domains

## Domain 1 → Domain 4

Domain 1 gives you the foundation:

- CIA
- Threats
- Vulnerabilities
- Risk
- Security controls

Domain 4 applies those ideas to networks.

**Example:** A vulnerable public-facing server is an asset with a vulnerability. An attacker exploiting it is a threat event. Firewalls and segmentation are controls that can reduce the resulting risk.

## Domain 2 → Domain 4

Domain 2 covers:

- Governance
- Risk
- Business continuity
- Disaster recovery
- Security awareness

Domain 4 applies those ideas to infrastructure.

**Example:** Redundant power and network links can support business continuity by reducing the chance that a single hardware failure causes an outage.

## Domain 3 → Domain 4

Domain 3 covers:

- Identity lifecycle
- Least privilege
- Logical access controls
- DAC
- MAC
- RBAC
- Separation of duties

Domain 4's Zero Trust and NAC depend heavily on these concepts.

**Example:** Zero Trust may require a user to authenticate and then receive only the network/application access required for their role.

## Domain 4 → Domain 5

Domain 4 focuses on network and cloud architecture.

Domain 5 builds on that architecture through:

- Logging
- Monitoring
- Event triage
- Threat intelligence
- Incident response
- Security testing

**Example:** A firewall blocks suspicious traffic, but its logs can also become evidence for an incident responder.

---

# High-Value Comparisons

## Segmentation vs. VLAN vs. Micro-Segmentation

**Segmentation:** Broad concept of dividing a network into security zones.

**VLAN:** Technology used to logically separate network traffic.

**Micro-segmentation:** More granular segmentation, potentially down to individual workloads or applications.

## VPN vs. VLAN

**VPN:** Protected communication path across a network.

**VLAN:** Logical separation of traffic within a network.

**Example:**
- Remote employee → VPN to corporate network
- Guest Wi-Fi vs. employee Wi-Fi → VLAN separation

## Firewall vs. NAC

**Firewall:** Controls network traffic according to rules.

**NAC:** Controls whether devices/users can obtain network access and may enforce device requirements.

## Defense in Depth vs. Zero Trust

**Defense in Depth:** Use multiple layers of security controls.

**Zero Trust:** Do not automatically trust users/devices based on network location; verify and continuously evaluate access.

They can be used together.

---

# Exam Scenario Thinking

When reading a question, ask:

### What is the problem?

- Unauthorized access?
- Excessive access?
- Network exposure?
- Lateral movement?
- Lack of segmentation?
- Compromised device?
- Availability?
- Cloud responsibility?
- Physical infrastructure?
- Wireless exposure?

### What control or architecture addresses it?

| Scenario | Concept |
|---|---|
| Limit movement between network zones | Segmentation |
| Separate traffic logically | VLAN |
| Granular workload isolation | Micro-segmentation |
| Public server isolated from internal network | DMZ |
| Control whether a device joins the network | NAC |
| Multiple security layers | Defense in Depth |
| Never automatically trust internal devices | Zero Trust |
| Secure remote connection over Internet | VPN |
| Control allowed network traffic | Firewall |
| Scale resources with demand | Rapid elasticity |
| Customer uses provider's application | SaaS |
| Customer manages virtual infrastructure | IaaS |
| Developer uses managed application platform | PaaS |
| Determine provider/customer responsibilities | Shared security model |
| Agreed service expectations | SLA |
| Outside company manages IT services | MSP |

---

# Quick Recall

| Concept | Remember |
|---|---|
| OSI | 7-layer conceptual model |
| TCP/IP | Practical Internet protocol model |
| IPv4 | 32-bit addressing |
| IPv6 | 128-bit addressing |
| TCP | Reliable, connection-oriented transport |
| UDP | Connectionless, lower-overhead transport |
| Port | Identifies a network service/application |
| VPN | Protected path across shared/untrusted network |
| Firewall | Controls network traffic |
| WLAN | Wireless LAN |
| ICS | Controls/monitors industrial processes |
| IoT | Network-connected physical devices |
| Segmentation | Divide network into security zones |
| DMZ | Zone for systems exposed to less-trusted networks |
| VLAN | Logical network separation |
| Micro-segmentation | Granular separation |
| NAC | Controls network access |
| Defense in Depth | Multiple security layers |
| Zero Trust | Verify rather than automatically trust |
| IaaS | Infrastructure |
| PaaS | Platform |
| SaaS | Software |
| Public cloud | Provider cloud |
| Private cloud | Dedicated organization environment |
| Community cloud | Shared by organizations with common concerns |
| Hybrid cloud | Combination |
| Shared security | Provider + customer responsibilities |
| SLA | Agreed service expectations |
| MSP | Managed service provider |
| Redundancy | Reduce single points of failure |
| IDS | Detect/alert |
| IPS | Detect + prevent/block |
| SIEM | Collect/correlate security events |
| Spoofing | Pretending to be another identity/address |
| DoS | Deny access to a service |
| DDoS | Distributed denial of service |
| MITM | Intercept communication between parties |

---

# Active Recall

Try answering these without looking.

1. What are the seven OSI layers?
2. What is the difference between OSI and TCP/IP?
3. What happens during encapsulation?
4. What is the difference between a packet and a frame?
5. How many bits are in IPv4?
6. How many bits are in IPv6?
7. What is the purpose of a port?
8. What is the difference between TCP and UDP?
9. What does a VPN provide?
10. What can a firewall use to decide whether to allow traffic?
11. What security risks are associated with wireless networks?
12. What is an embedded system?
13. What is an ICS?
14. What is IoT?
15. Why is network segmentation useful?
16. What is a DMZ?
17. What is a VLAN?
18. How is micro-segmentation different from normal segmentation?
19. What does NAC do?
20. What is Defense in Depth?
21. What is the basic principle of Zero Trust?
22. How does Zero Trust connect to least privilege?
23. What are the five cloud characteristics?
24. Explain IaaS, PaaS, and SaaS.
25. What is the difference between public, private, community, and hybrid cloud?
26. What is the shared security model?
27. What is an SLA?
28. What is an MSP?
29. Why is redundancy important?
30. How does Domain 4 connect to Domain 1?
31. How does Domain 4 connect to Domain 3?
32. How does Domain 4 connect to Domain 5?
33. What is the difference between IDS and IPS?
34. What is the difference between NIDS and HIDS?
35. What is spoofing?
36. What is the difference between DoS and DDoS?
37. What is a man-in-the-middle attack?

---

# Feynman Check

Explain these out loud as if teaching someone with basic computer knowledge:

### 1. VLAN
Explain what problem a VLAN solves and give a real-world example.

### 2. Zero Trust
Explain why "the user is inside the corporate network" is not enough to automatically trust them.

### 3. Shared Security Model
Explain why moving an application to the cloud does not mean the customer has zero security responsibilities.

### 4. Defense in Depth
Explain what happens if one security control fails.

### 5. Micro-Segmentation
Explain why micro-segmentation provides more granular control than a traditional network segment.

---

# One-Minute Exam Sheet

**OSI:** Application → Presentation → Session → Transport → Network → Data Link → Physical

**IPv4:** 32-bit  
**IPv6:** 128-bit

**TCP:** reliable/connection-oriented  
**UDP:** connectionless/lower overhead

**VPN:** protected path across shared/untrusted network

**Firewall:** controls network traffic

**Segmentation:** divide network into zones  
**DMZ:** zone for systems exposed to less-trusted networks  
**VLAN:** logical separation  
**Micro-segmentation:** granular separation  
**NAC:** controls network access  
**Defense in Depth:** multiple security layers  
**Zero Trust:** verify; don't automatically trust

**IaaS:** infrastructure  
**PaaS:** platform  
**SaaS:** software

**Public:** provider cloud  
**Private:** dedicated organization  
**Community:** shared common requirements  
**Hybrid:** combination

**Shared security:** provider + customer

**SLA:** agreed service expectations  
**MSP:** managed services provider

**Redundancy:** avoid single points of failure

**IDS:** detect  
**IPS:** prevent/block

**Domain connections:**
- D1 → risk + controls
- D2 → BC/DR + governance
- D3 → IAM + least privilege
- D4 → network/cloud architecture
- D5 → monitoring + IR
