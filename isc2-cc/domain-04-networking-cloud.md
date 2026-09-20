# Domain 4 — Networking and Cloud Security Concepts

**Exam weight: 21.3%**

## 4.1 Network Security

### OSI Model

Know the seven layers:

1. Physical
2. Data Link
3. Network
4. Transport
5. Session
6. Presentation
7. Application

### TCP/IP Model

Know the major TCP/IP layers and how they relate to the OSI model.

### IPv4 and IPv6

Understand the basic purpose of IP addressing and the differences between IPv4 and IPv6.

### VPN

A Virtual Private Network creates a protected communication path across an untrusted or shared network.

### Ports

Ports help identify network services and applications.

Examples worth recognizing:
- HTTP — 80
- HTTPS — 443
- SSH — 22
- DNS — 53
- RDP — 3389

### Firewalls

Firewalls enforce traffic rules based on defined criteria such as addresses, ports, protocols, or applications.

### Wireless

Understand common Wi-Fi security concepts and the risks associated with wireless communications.

### Bluetooth

Bluetooth provides short-range wireless communication and introduces security considerations related to pairing, authentication, and unauthorized devices.

### Embedded Systems

Understand the security concerns of:
- Industrial Control Systems (ICS)
- Internet of Things (IoT)

These systems can have availability, safety, legacy-system, and segmentation concerns.

---

## 4.2 Network Security Architecture

### Network Segmentation

Segmentation divides a network into separate security zones.

Examples:
- DMZ
- VLAN
- VPN
- Micro-segmentation

Segmentation can limit lateral movement and reduce the impact of compromise.

### Defense in Depth

Use multiple layers of security rather than relying on one control.

### Network Access Control (NAC)

NAC can control whether devices are permitted to access network resources based on defined requirements.

### Zero Trust

Zero Trust is based on the idea that access should not be trusted simply because a user or device is inside a network.

Core ideas include:
- Verify explicitly
- Use least privilege
- Continuously evaluate access

---

## 4.3 Cloud Security

### Cloud Characteristics

Know the common characteristics:
- Broad network access
- Rapid elasticity
- Measured service
- On-demand self-service
- Resource pooling

### Service Models

#### IaaS — Infrastructure as a Service

The provider supplies infrastructure such as compute, storage, and networking.

#### PaaS — Platform as a Service

The provider supplies a platform for developing and running applications.

#### SaaS — Software as a Service

The provider delivers the application to the customer.

### Deployment Models

Know the basic concepts of:
- Public cloud
- Private cloud
- Hybrid cloud

### Shared Security Model

Cloud security responsibilities are divided between the cloud provider and the customer.

The exact division depends on the service model.

**Key idea:** Moving to the cloud does not automatically transfer every security responsibility to the provider.

### SLA

A Service-Level Agreement defines agreed service expectations between parties.

### MSP

A Managed Service Provider delivers managed technology or security services to customers.

---

## Quick Recall

- OSI = 7 layers
- Firewall = controls network traffic
- VPN = protected communication path
- Segmentation = divide network/security zones
- Defense in depth = multiple layers
- Zero Trust = verify rather than automatically trust
- IaaS = infrastructure
- PaaS = platform
- SaaS = software
- Shared security = provider + customer responsibilities
