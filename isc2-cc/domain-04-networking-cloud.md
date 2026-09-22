# Domain 4 --- Networking and Cloud Security Concepts

**Exam weight: 21.3%**\
**Current exam outline effective: September 1, 2026**

## 2026 Exam Objectives

### 4.1 Understand network security

-   Network security concepts
-   OSI model
-   TCP/IP model
-   IPv4
-   IPv6
-   VPN
-   Firewalls
-   Ports/applications
-   Wireless
-   Embedded systems
-   ICS
-   IoT

### 4.2 Understand network security architecture

-   Network segmentation
-   Firewall zones
-   VLAN
-   Micro-segmentation
-   Defense in Depth
-   Zero Trust

### 4.3 Understand cloud security

-   Cloud characteristics
-   Service models
-   Deployment models
-   Shared security model

------------------------------------------------------------------------

# 4.1 Network Security

## OSI Model

Know the seven layers:

    Layer Name
  ------- --------------
        7 Application
        6 Presentation
        5 Session
        4 Transport
        3 Network
        2 Data Link
        1 Physical

### Easy Memory

**All People Seem To Need Data Processing**

Application → Presentation → Session → Transport → Network → Data Link →
Physical

------------------------------------------------------------------------

## TCP/IP Model

Know the major TCP/IP layers and how they relate to the OSI model.

Common four-layer representation:

1.  Application
2.  Transport
3.  Internet
4.  Network Access

------------------------------------------------------------------------

## IPv4 and IPv6

### IPv4

Uses 32-bit IP addresses.

### IPv6

Uses 128-bit IP addresses and provides a much larger address space.

For CC, understand the basic purpose of IP addressing and the difference
in address size.

------------------------------------------------------------------------

## VPN

A **Virtual Private Network (VPN)** creates a protected communication
path across an untrusted or shared network.

**VPN = protected path over an untrusted network**

------------------------------------------------------------------------

## Ports

Ports help identify network services and applications.

Know common examples:

  Service     Port
  --------- ------
  HTTP          80
  HTTPS        443
  SSH           22
  DNS           53
  RDP         3389

> The exam outline specifically connects firewalls with ports and
> applications.

------------------------------------------------------------------------

## Firewalls

Firewalls enforce traffic rules based on defined criteria such as: -
Addresses - Ports - Protocols - Applications

**Firewall = controls permitted network traffic**

------------------------------------------------------------------------

## Wireless

Understand common Wi-Fi security concepts and the risks associated with
wireless communications.

## Bluetooth

Bluetooth provides short-range wireless communication.

Security considerations include: - Pairing - Authentication -
Unauthorized devices

------------------------------------------------------------------------

## Embedded Systems

Understand security concerns associated with: - **Industrial Control
Systems (ICS)** - **Internet of Things (IoT)**

Potential concerns include: - Availability - Safety - Legacy systems -
Segmentation

------------------------------------------------------------------------

# 4.2 Network Security Architecture

## Network Segmentation

Segmentation divides a network into separate security zones.

Examples: - **DMZ** - **VLAN** - **VPN** - **Micro-segmentation**

### Why Segment?

Segmentation can: - Limit lateral movement - Isolate systems - Reduce
the impact of compromise

------------------------------------------------------------------------

## Firewall Zones

Firewalls can separate network areas into different security zones with
different access rules.

------------------------------------------------------------------------

## VLAN

A **Virtual Local Area Network (VLAN)** logically separates network
traffic even when systems share physical network infrastructure.

------------------------------------------------------------------------

## Micro-Segmentation

Micro-segmentation applies segmentation at a more granular level,
allowing tighter controls between individual workloads, systems, or
applications.

------------------------------------------------------------------------

## Defense in Depth

**Defense in Depth** uses multiple layers of security instead of relying
on a single control.

Example layers can include: - Physical controls - Network controls -
Endpoint controls - Identity controls - Monitoring

**Defense in depth = multiple layers**

------------------------------------------------------------------------

## Zero Trust

Zero Trust is based on the principle that access should not
automatically be trusted simply because a user or device is inside a
network.

Core ideas: - Verify explicitly - Use least privilege - Continuously
evaluate access

**Zero Trust = don't automatically trust; verify.**

------------------------------------------------------------------------

# 4.3 Cloud Security

## Cloud Characteristics

Know:

-   **Broad network access**
-   **Rapid elasticity**
-   **Measured service**
-   **On-demand self-service**
-   **Resource pooling**

### Broad Network Access

Cloud capabilities can be accessed over networks using supported
devices.

### Rapid Elasticity

Resources can be scaled up or down as needed.

### Measured Service

Resource usage can be monitored and measured.

### On-Demand Self-Service

Customers can provision resources without requiring direct provider
interaction for every request.

### Resource Pooling

Provider resources are pooled to serve multiple customers.

------------------------------------------------------------------------

# Cloud Service Models

## IaaS --- Infrastructure as a Service

The provider supplies infrastructure such as: - Compute - Storage -
Networking

**IaaS = infrastructure**

## PaaS --- Platform as a Service

The provider supplies a platform for developing and running
applications.

**PaaS = platform**

## SaaS --- Software as a Service

The provider delivers the application to the customer.

**SaaS = software**

------------------------------------------------------------------------

# Cloud Deployment Models

## Public Cloud

Cloud infrastructure is provided for use by customers through a cloud
provider.

## Private Cloud

Cloud infrastructure is dedicated to a particular organization.

## Hybrid Cloud

Combines public and private cloud environments.

------------------------------------------------------------------------

# Shared Security Model

Cloud security responsibilities are divided between the cloud provider
and the customer.

The exact division depends on: - Service model - Provider - Customer
responsibilities

> Moving to the cloud does **not** automatically transfer every security
> responsibility to the provider.

------------------------------------------------------------------------

## SLA

A **Service-Level Agreement (SLA)** defines agreed service expectations
between parties.

## MSP

A **Managed Service Provider (MSP)** delivers managed technology or
security services to customers.

------------------------------------------------------------------------

# Quick Recall

  Concept              Remember
  -------------------- ----------------------------------------------
  OSI                  7-layer model
  TCP/IP               Network communication model
  IPv4                 32-bit addressing
  IPv6                 128-bit addressing
  VPN                  Protected path over shared/untrusted network
  Firewall             Controls network traffic
  Port                 Identifies network service/application
  Segmentation         Divide security zones
  VLAN                 Logical network separation
  Micro-segmentation   Granular workload/system separation
  Defense in depth     Multiple security layers
  Zero Trust           Verify rather than automatically trust
  IaaS                 Infrastructure
  PaaS                 Platform
  SaaS                 Software
  Public cloud         Provider cloud for broad customer use
  Private cloud        Dedicated organization environment
  Hybrid cloud         Combination
  Shared security      Provider + customer responsibilities
  SLA                  Agreed service expectations
  MSP                  Managed services provider

# Active Recall

1.  Name the seven OSI layers.
2.  How does TCP/IP relate to OSI?
3.  What is the basic difference between IPv4 and IPv6?
4.  What does a VPN provide?
5.  Why are ports important?
6.  What does a firewall control?
7.  What security concerns can wireless introduce?
8.  What are ICS and IoT?
9.  Why is network segmentation useful?
10. What is a VLAN?
11. What is micro-segmentation?
12. What is defense in depth?
13. What is the basic idea behind Zero Trust?
14. What are the five cloud characteristics in the outline?
15. Explain IaaS, PaaS, and SaaS.
16. Explain public, private, and hybrid cloud.
17. What is the shared security model?
