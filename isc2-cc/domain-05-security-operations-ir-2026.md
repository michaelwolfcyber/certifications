# Domain 5 — Security Operations and Incident Response

**Exam weight:** 17.3%  
**Current CC exam outline:** Effective September 1, 2026

> These notes use my original Domain 5 notes as the foundation and organize them around the current 2026 objectives. ISC2 course concepts are included where they add useful context or terminology. Examples are included to make concepts easier to apply to scenario questions.

---

# 2026 Exam Objectives

- **5.1 Understand data security**
  - Data handling: classification, labeling, masking, sanitization
  - Encryption: symmetric, asymmetric, hashing, quantum-resistant cryptography
- **5.2 Understand security operations**
  - Logging and monitoring
  - Security event triage: incident use cases, prioritization, correlation
  - Threat actors: types and motivations
  - Cyber threat intelligence
  - Threat frameworks
- **5.3 Understand Incident Response**
  - Data handling policy implementing an IRP
  - Incident Response exercises: testing and tabletop
- **5.4 Understand asset protection**
  - Asset lifecycle management
  - End of Life (EOL)
  - Configuration and change management
- **5.5 Understand security testing**
  - Blue, purple, red teaming
  - Vulnerability scanning
  - Static and dynamic analysis
  - Threat modeling
  - Physical penetration testing: phishing, tailgating, impersonation

---


# Study Examples and High-Value Distinctions

## Data handling

**Classification:** determines how sensitive information is.

**Example:** A company classifies employee medical records as highly sensitive and applies stronger protections than it uses for a public brochure.

**Labeling:** communicates the classification or handling requirement.

**Example:** A document marked `CONFIDENTIAL` tells users that it needs restricted handling.

**Masking:** obscures some or all of the information while keeping the underlying record usable.

**Example:** `4532 1111 2222 3333` → `**** **** **** 3333`.

**Sanitization:** removes or destroys data so it cannot be recovered through normal means.

**Example:** A laptop is being retired, so its storage is properly sanitized before disposal.

**Exam clue:**  
Classification = decide sensitivity.  
Labeling = communicate it.  
Masking = obscure it.  
Sanitization = remove/destroy it.

## Cryptography

### Symmetric encryption

Uses the same key for encryption and decryption.

**Example:** A large database is encrypted with a secret key. Anyone who needs to decrypt it needs access to that key.

**Think:** same key.

### Asymmetric encryption

Uses a public/private key pair.

**Example:** A sender encrypts a confidential message with the recipient's public key; the recipient uses the corresponding private key to decrypt it.

**Think:** key pair.

### Hashing

Produces a fixed-length digest from input data.

**Example:** You download a file, calculate its hash, and compare it with a published hash to check whether the file changed.

**Important:** Hashing is not encryption.

**Exam clue:**  
Confidentiality → encryption.  
Integrity verification → hashing.

### Quantum-resistant cryptography

Cryptographic approaches designed to remain secure against sufficiently capable quantum computers.

**Example:** An organization protecting information that must remain confidential for decades may need to consider future quantum threats.

## Security operations

### Logging

Records activity.

**Example:** An authentication log records repeated failed login attempts.

### Monitoring

Watches activity for meaningful or suspicious events.

**Example:** A monitoring system alerts when an account suddenly generates hundreds of failed login attempts.

### Triage

Evaluates events and determines their priority/significance.

**Example:** A suspicious event affecting a critical production server may receive attention before a low-impact alert from a test machine.

### Correlation

Connects related events to reveal a pattern.

**Example:**

```text
Failed logins
    +
Successful unusual login
    +
Privilege change
    +
Large outbound transfer
    ↓
Possible account compromise
```

**Think:** correlation = connect the dots.

## Threat actors

Threat actors can differ in type, capability, resources, and motivation.

**Example:** A cybercriminal may seek financial gain, while a nation-state actor may pursue espionage.

Do not assume every attacker has the same objective.

## Cyber Threat Intelligence

CTI provides threat information and context that helps organizations understand, detect, and respond to adversary activity.

**Example:** An organization learns that a threat actor targeting its industry commonly uses a particular technique and improves monitoring for that behavior.

## Incident Response

An **IRP** provides an organized approach for responding to security incidents.

**Example:** During a ransomware incident, the IRP helps establish responsibilities, escalation, communication, containment, and coordinated response.

### Tabletop

Discussion-based exercise.

**Example:** The team is told, "Ransomware has been detected on a critical server. What do you do?" Participants talk through the response.

### Testing

Exercises the actual response capability.

**Think:** tabletop = discuss; testing = exercise.

## Asset protection

### EOL

End-of-life software or devices may stop receiving vendor support and security updates.

**Example:** An organization continues running an unsupported operating system. A newly discovered vulnerability may remain unpatched.

### Configuration baseline

An approved configuration used as a reference for detecting unauthorized or unexpected changes.

**Example:** A server baseline specifies required services, patches, and security settings.

### Change management

Controls and documents changes through processes such as request, approval, testing, implementation, verification, and rollback.

**Example:** An administrator wants to modify a firewall rule. The change is requested, approved, tested, implemented, and documented with a rollback plan.

## Security testing

### Blue Team

Defensive team focused on defense, detection, and response.

### Red Team

Simulates an adversary to test defenses.

### Purple Team

Coordinates offensive and defensive work so lessons from testing improve detection and defense.

**Memory:** Blue = defend, Red = attack simulation, Purple = collaborate.

### Vulnerability scanning

Systematically identifies potential vulnerabilities.

**Example:** A scanner identifies an outdated software package with a known vulnerability.

### Static analysis

Analyzes software without executing it.

**Example:** A source-code analysis tool identifies a possible security flaw before deployment.

### Dynamic analysis

Analyzes software while it is executing.

**Example:** A tester runs an application and observes how it handles unexpected input.

### Threat modeling

Identifies threats and attack paths during design so controls can be considered before deployment.

**Example:** A development team maps possible attacks against authentication, APIs, and sensitive databases before releasing an application.

### Physical penetration testing

The current objective explicitly includes:

- **Phishing** — deceptive communication used to manipulate a target.
- **Tailgating** — following an authorized person into a restricted area without authorization.
- **Impersonation** — pretending to be an authorized person.

**Example:** A tester sends a simulated phishing message, attempts to tailgate through a secured door, or pretends to be a contractor to test whether staff follow security procedures.

---

# Domain Connections

## Domain 1 → Domain 5

Domain 1 gives you assets, threats, vulnerabilities, risk, CIA, and controls.

**Example:** An exposed server is an asset with a vulnerability. A threat actor exploits it. Domain 5 is where the organization detects the activity, triages it, responds, and improves controls.

## Domain 2 → Domain 5

Domain 2 covers governance, policies, awareness, and continuity.

**Example:** A data-handling policy tells employees how sensitive information should be handled; during an incident, those requirements still matter.

Phishing also connects both domains:
- Domain 2 → awareness and prevention
- Domain 5 → security testing

## Domain 3 → Domain 5

Domain 3 covers identities and access.

**Example:** Security monitoring detects repeated failed logins followed by an unusual successful login. Investigators can then examine the account's permissions and activity.

## Domain 4 → Domain 5

Domain 4 covers networks and cloud architecture.

**Example:** A firewall records suspicious traffic. Security personnel correlate the firewall event with authentication and endpoint events during triage.

---

# High-Value Comparisons

| Concept | Remember |
|---|---|
| Classification vs. labeling | Decide sensitivity vs. communicate handling |
| Masking vs. sanitization | Obscure vs. remove/destroy |
| Encryption vs. hashing | Confidentiality vs. integrity |
| Symmetric vs. asymmetric | Same key vs. key pair |
| Logging vs. monitoring | Record vs. watch |
| Triage vs. correlation | Evaluate/prioritize vs. connect events |
| Tabletop vs. testing | Discuss vs. exercise capability |
| Configuration vs. change management | Maintain known state vs. control changes |
| Static vs. dynamic analysis | Not running vs. running |
| Vulnerability scanning vs. threat modeling | Find weaknesses vs. identify threats/paths |
| Blue vs. red vs. purple | Defend vs. simulate adversary vs. collaborate |
| Phishing vs. tailgating vs. impersonation | Deceptive communication vs. physical following vs. pretending to be authorized |

---

# Scenario Thinking

When you see a Domain 5 scenario, ask:

1. **What is happening?**
2. **What security objective is involved?**
3. **What concept from the objective best fits?**
4. **What evidence or control would help?**

| Scenario | Likely concept |
|---|---|
| Determine how sensitive data is | Classification |
| Communicate how data must be handled | Labeling |
| Hide part of a record | Masking |
| Destroy data before disposal | Sanitization |
| Protect data confidentiality | Encryption |
| Verify whether data changed | Hashing |
| Prepare for future quantum threats | Quantum-resistant cryptography |
| Record activity | Logging |
| Watch for suspicious activity | Monitoring |
| Rank alerts by importance | Triage/prioritization |
| Connect multiple events | Correlation |
| Understand adversary activity | CTI |
| Organize incident response | IRP |
| Discuss a simulated incident | Tabletop |
| Exercise response capability | Testing |
| Unsupported software/device | EOL |
| Maintain approved configuration | Baseline/configuration management |
| Control a system change | Change management |
| Defend against simulated attacks | Blue Team |
| Simulate an attacker | Red Team |
| Improve defense through Red/Blue collaboration | Purple Team |
| Identify potential weaknesses | Vulnerability scanning |
| Analyze without running software | Static analysis |
| Analyze while running software | Dynamic analysis |
| Identify attack paths during design | Threat modeling |
| Test deceptive messages | Phishing |
| Follow someone into a restricted area | Tailgating |
| Pretend to be authorized | Impersonation |

---

# Active Recall

Try answering these without looking:

1. What are the four current data-handling concepts?
2. Classification vs. labeling?
3. Masking vs. sanitization?
4. Symmetric vs. asymmetric encryption?
5. Why is hashing different from encryption?
6. What is quantum-resistant cryptography?
7. Logging vs. monitoring?
8. What is security event triage?
9. Why is prioritization necessary?
10. What is event correlation?
11. What is an incident use case?
12. What is a threat actor?
13. Why do threat actor motivations matter?
14. What is CTI?
15. What is the purpose of a threat framework?
16. What is an IRP?
17. What is a tabletop exercise?
18. How is testing different from a tabletop?
19. Why are EOL systems risky?
20. What is a configuration baseline?
21. What is hardening?
22. What is change management?
23. What is the purpose of rollback?
24. Blue vs. Red vs. Purple?
25. What is vulnerability scanning?
26. Static vs. dynamic analysis?
27. What is threat modeling?
28. What is phishing?
29. What is tailgating?
30. What is impersonation?

---

# Feynman Check

Explain these out loud in your own words:

### 1. Hashing
Why can hashing help determine whether a file changed, but not be used like normal encryption to recover the original file?

### 2. Triage
If you have thousands of alerts, why can't a security team simply investigate them in the order received?

### 3. Correlation
How can several individually minor events become important when viewed together?

### 4. Incident Response
Why is an IRP useful before an incident rather than trying to invent a response during the incident?

### 5. Change Management
Why should a major firewall change involve approval, testing, documentation, and rollback?

### 6. Purple Team
What does the Blue Team gain from working with the Red Team?

### 7. Threat Modeling
How can threat modeling prevent problems before an application is deployed?

### 8. Physical Penetration Testing
How can phishing, tailgating, and impersonation test an organization's security without exploiting software?

---

# One-Minute Exam Sheet

**Classification:** determine sensitivity  
**Labeling:** communicate handling requirements  
**Masking:** obscure data  
**Sanitization:** remove/destroy recoverable data

**Symmetric:** same key  
**Asymmetric:** public/private key pair  
**Hashing:** fixed-length digest; integrity  
**Quantum-resistant:** designed for future quantum threats

**Logging:** record  
**Monitoring:** watch  
**Triage:** evaluate/prioritize  
**Correlation:** connect events  
**CTI:** threat information/context

**IRP:** organized incident response plan  
**Tabletop:** discussion  
**Testing:** exercise response capability

**Asset lifecycle:** acquire → deploy → maintain → retire → dispose  
**EOL:** unsupported/near unsupported asset  
**Baseline:** approved configuration  
**Hardening:** reduce attack surface  
**Change management:** controlled/documented change

**Blue:** defend  
**Red:** simulate attacker  
**Purple:** improve defense through Red/Blue collaboration

**Vulnerability scanning:** find potential weaknesses  
**Static:** not running  
**Dynamic:** running  
**Threat modeling:** identify threats/attack paths

**Phishing:** deceptive communication  
**Tailgating:** unauthorized following into restricted area  
**Impersonation:** pretend to be authorized

**Domain connections:**
- D1 → assets + threats + vulnerabilities + risk + controls
- D2 → governance + policies + awareness + BC/DR
- D3 → identities + access + least privilege
- D4 → network/cloud architecture + monitoring sources
- D5 → operate + detect + respond + protect + test

---

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
