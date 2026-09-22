# Domain 5 --- Security Operations and Incident Response

**Exam weight: 17.3%**\
**Current exam outline effective: September 1, 2026**

## 2026 Exam Objectives

### 5.1 Understand data security

-   Data handling
    -   Classification
    -   Labeling
    -   Masking
    -   Sanitization
-   Encryption
    -   Symmetric
    -   Asymmetric
    -   Hashing
    -   Quantum-resistant cryptography

### 5.2 Understand security operations

-   Logging and monitoring security events
-   Security event triage
    -   Incident use cases
    -   Prioritization
    -   Correlation
-   Threat actors
    -   Types
    -   Motivations
-   Cyber threat intelligence
-   Threat frameworks

### 5.3 Understand Incident Response (IR)

-   Data handling policy implementing an Incident Response Plan (IRP)
-   Incident Response exercises
    -   Testing
    -   Tabletop

### 5.4 Understand asset protection

-   Asset lifecycle management
    -   End of Life (EOL) software and devices
-   Configuration and change management

### 5.5 Understand security testing

-   Security readiness testing
    -   Blue teaming
    -   Purple teaming
    -   Red teaming
-   Application testing
    -   Vulnerability scanning
    -   Static analysis
    -   Dynamic analysis
    -   Threat modeling
-   Physical penetration testing
    -   Phishing
    -   Tailgating
    -   Impersonation

------------------------------------------------------------------------

# 5.1 Data Security

## Data Handling

Know the purpose of: - Classification - Labeling - Masking -
Sanitization

## Classification

Classify information according to its sensitivity and required
protection.

## Labeling

Labels communicate the classification or handling requirements of
information.

## Masking

Masking obscures part or all of sensitive information.

## Sanitization

Sanitization removes or destroys data so it cannot be recovered through
normal means.

### Quick Distinction

**Classification = determine sensitivity**\
**Labeling = communicate classification/handling**\
**Masking = obscure information**\
**Sanitization = remove/destroy recoverable information**

------------------------------------------------------------------------

# Encryption and Cryptography

## Symmetric Encryption

Uses the **same key** for encryption and decryption.

**Strength:** Efficient for large amounts of data.

**Challenge:** Secure key distribution.

**Symmetric = same key**

## Asymmetric Encryption

Uses a **key pair**: - Public key - Private key

**Asymmetric = key pair**

## Hashing

A hash function produces a fixed-length value from data.

Hashing is commonly used for: - Integrity verification -
Password-related security mechanisms

> **Hashing is not the same as encryption.**

## Quantum-Resistant Cryptography

Quantum-resistant cryptography is designed to remain secure against
attacks from sufficiently capable quantum computers.

For CC, recognize why quantum-resistant cryptography is relevant to
future cryptographic security.

------------------------------------------------------------------------

# 5.2 Security Operations

## Logging and Monitoring

Security logs provide records of system and security activity.

Monitoring helps identify: - Unusual behavior - Suspicious activity -
Potential security events

**Logging = record activity**\
**Monitoring = watch activity for meaningful events**

------------------------------------------------------------------------

## Security Event Triage

**Triage** involves evaluating security events and determining their
priority and significance.

Important concepts:

### Incident Use Cases

Use cases describe situations or event patterns that security teams may
need to identify and investigate.

### Prioritization

Determine which events require attention first based on factors such as
significance and potential impact.

### Correlation

Connect related events or data points to identify patterns or
relationships that may not be obvious from one event alone.

**Triage = evaluate + prioritize**

------------------------------------------------------------------------

## Threat Actors

Threat actors are individuals or groups that may intentionally or
unintentionally create security threats.

Understand different: - Types - Capabilities - Resources - Motivations

### Motivations

The reason an actor carries out activity can affect how the threat
should be understood and handled.

> Do not assume every threat actor has the same objective.

------------------------------------------------------------------------

## Cyber Threat Intelligence (CTI)

**Cyber Threat Intelligence** is information about threats that can help
organizations understand, detect, and respond to adversary activity.

CTI can help security teams understand: - Threat activity - Adversary
behavior - Potential threats - Relevant indicators and context

------------------------------------------------------------------------

## Threat Frameworks

Threat frameworks provide structured ways to: - Describe adversary
behavior - Categorize threats - Analyze attack activity

------------------------------------------------------------------------

# 5.3 Incident Response

## Incident Response Plan (IRP)

An **Incident Response Plan** provides an organized approach for
responding to security incidents.

Know: - Its purpose - Why organizations need it - Major components - How
it supports coordinated response

## Data Handling Policy and IRP

The current outline specifically connects **data handling policy** with
implementation of the Incident Response Plan.

Understand that policies provide organizational direction for handling
data and responding appropriately when security incidents occur.

------------------------------------------------------------------------

## Incident Response Exercises

Organizations test response capabilities through exercises such as:

-   Tabletop exercises
-   Testing
-   Simulated scenarios

### Purpose

Exercises help identify: - Weaknesses - Gaps - Coordination problems -
Areas needing improvement

**Tabletop = discussion-based exercise**\
**Testing = exercises response capability**

------------------------------------------------------------------------

# 5.4 Asset Protection

## Asset Lifecycle Management

Assets can move through a lifecycle such as:

1.  Acquisition
2.  Deployment
3.  Maintenance
4.  Retirement
5.  Disposal

## End of Life (EOL)

End-of-life software or devices may no longer receive vendor support or
security updates.

EOL assets can therefore create security and operational risks.

------------------------------------------------------------------------

## Configuration Management

Configuration management helps maintain systems in known, controlled
states.

## Baselines

A **baseline** is an approved configuration against which changes can be
compared.

## Updates and Patches

Updates and patches can address: - Vulnerabilities - Bugs - Other issues

------------------------------------------------------------------------

## Change Management

Changes should be controlled and documented.

Typical concepts: - Documentation - Approval - Testing -
Implementation - Rollback

**Change management = controlled, documented change**

------------------------------------------------------------------------

# 5.5 Security Testing

## Security Readiness Testing

### Blue Team

Defensive security team.

Focus: - Defense - Detection - Response

### Red Team

Simulated adversary/offensive security team.

Focus: - Testing defenses by emulating attackers

### Purple Team

Collaboration between offensive and defensive teams.

**Blue = defense**\
**Red = adversary simulation**\
**Purple = collaboration**

------------------------------------------------------------------------

## Vulnerability Scanning

Automated or systematic identification of potential vulnerabilities.

## Static Analysis

Analyzes software **without executing it**.

**Static = not running**

## Dynamic Analysis

Analyzes software **while it is executing**.

**Dynamic = running**

## Threat Modeling

Identifies potential threats and attack paths so security controls can
be considered during design.

**Threat modeling = identify threats during design**

------------------------------------------------------------------------

## Physical Penetration Testing

Physical security can be tested through activities such as:

### Phishing

Attempting to manipulate people through deceptive communications.

### Tailgating

Following an authorized person into a restricted area without
authorization.

### Impersonation

Pretending to be an authorized person to gain access or information.

> The current outline explicitly includes phishing, tailgating, and
> impersonation under physical penetration testing.

------------------------------------------------------------------------

# Quick Recall

  Concept             Remember
  ------------------- ---------------------------------------------
  Classification      Determine sensitivity
  Labeling            Communicate handling category
  Masking             Obscure data
  Sanitization        Remove/destroy recoverable data
  Symmetric           Same key
  Asymmetric          Key pair
  Hashing             Fixed-length transformation; not encryption
  Quantum-resistant   Designed for future quantum threats
  Logging             Record activity
  Monitoring          Watch activity
  Triage              Evaluate/prioritize events
  Correlation         Connect related events
  CTI                 Threat information/context
  IRP                 Organized incident response plan
  EOL                 End of vendor/product lifecycle
  Baseline            Approved configuration
  Change management   Controlled/documented change
  Blue                Defense
  Red                 Adversary simulation
  Purple              Offensive + defensive collaboration
  Static analysis     Analyze without executing
  Dynamic analysis    Analyze while executing
  Threat modeling     Identify threats/attack paths
  Tailgating          Unauthorized following into restricted area
  Impersonation       Pretending to be authorized

# Active Recall

1.  What are the four major data-handling concepts?
2.  What is the difference between masking and sanitization?
3.  How does symmetric encryption work?
4.  How does asymmetric encryption work?
5.  Why is hashing different from encryption?
6.  What is quantum-resistant cryptography?
7.  What is the difference between logging and monitoring?
8.  What is security event triage?
9.  What are incident use cases?
10. Why is prioritization important?
11. What does event correlation accomplish?
12. What is CTI?
13. What is a threat framework?
14. What is the purpose of an IRP?
15. Why conduct tabletop exercises?
16. What happens during an asset lifecycle?
17. Why are EOL systems a concern?
18. What is a configuration baseline?
19. What are the main ideas of change management?
20. What is the difference between blue, red, and purple teams?
21. What is vulnerability scanning?
22. What is static analysis?
23. What is dynamic analysis?
24. What is threat modeling?
25. What is tailgating?
26. What is impersonation?
