---
description: 'Domain 1 — Security Principles'
---

# Domain 1 — Security Principles

**Exam weight: 24%**

## Learning Objectives

> **Exam focus:** Know what each objective is asking you to understand, not just the definitions.

After completing this domain, you should be able to:

1. Discuss the foundational concepts of cybersecurity principles.
2. Recognize foundational security concepts of information assurance.
3. Define risk management terminology and summarize the process.
4. Relate risk management to personal or professional practices.
5. Classify types of security controls.
6. Distinguish between policies, procedures, standards, regulations, and laws.
7. Demonstrate the relationship among governance elements.
8. Analyze appropriate outcomes according to the canons of the ISC2 Code of Ethics when given examples.
9. Practice the terminology and review security principles.

### Exam Objective Map

The Domain 1 material is organized into five main areas:

- **1.1 Understand cybersecurity concepts**
- **1.2 Understand risk management concepts**
- **1.3 Understand governance concepts**
- **1.4 Understand cybersecurity controls**
- **1.5 Maintain professional and ethical conduct**

The ISC2 outline places confidentiality, integrity, availability, AAA, non-repudiation, and privacy under 1.1; risk lifecycle/processes under 1.2; governance elements under 1.3; technical, administrative, and physical controls under 1.4; and professional conduct, due care/due diligence, and the ISC2 Code of Ethics under 1.5.

**Key Topics**

- Identity assurance
- Privacy control mechanisms
- Safeguarding data
- Strategic risk management

---

# 1.1 Security Concepts of Information Assurance

## CIA Triad

The CIA Triad is the foundation of information security.

### Confidentiality

Protecting information from unauthorized access or disclosure.

**Examples**

- Access controls
- Encryption
- Data classification
- Need-to-know access

### Integrity

Ensuring information is not altered or destroyed in an unauthorized manner.

**Examples**

- Hashing
- Digital signatures
- File integrity monitoring
- Change controls

### Availability

Ensuring authorized users can access information when and where it is needed, in the required form and format.

**Examples**

- Redundancy
- Backups
- Failover
- Disaster recovery
- Load balancing

**Remember:**

> Confidentiality = prevent unauthorized access
> Integrity = prevent unauthorized changes
> Availability = access when needed

---

## Assets

An **asset** is anything of value owned by an organization that needs protection.

Examples:

- Information
- Hardware
- Software
- Systems
- People
- Reputation

---

## Threats

A **threat** is any circumstance or event with the potential to adversely affect an organization, its assets, individuals, other organizations, or the nation.

Threats can involve:

- Unauthorized access
- Disclosure of information
- Destruction
- Modification
- Denial of service

### Common Threat Actors

- **Insiders** — Employees or other trusted individuals; may act deliberately or accidentally.
- **Outside individuals or informal groups** — Attackers who may discover or exploit vulnerabilities.
- **Nonpolitical formal entities** — Competitors or cybercriminals.
- **Political formal entities** — Nation-states, terrorists, or hacktivists.
- **Intelligence or information gatherers**
- **Technology** — Bots and artificial intelligence can also be involved in threats.

---

## Threat Actor

A **threat actor** is an individual or group that attempts to exploit vulnerabilities to cause or force a threat to occur.

## Threat Vector

A **threat vector** is the means by which a threat actor carries out their objectives.

**Easy distinction:**

Threat actor = who
Threat vector = how

---

## Vulnerability

A **vulnerability** is a weakness in an information system, security procedure, internal control, or implementation that could be exploited by a threat source.

Examples:

- Unpatched software
- Weak passwords
- Misconfigured systems
- Missing security controls

**Easy distinction:**

Threat = potential danger
Vulnerability = weakness
Threat actor = who exploits it
Threat vector = how they do it

---

## Risk

Risk is a possible event or condition that can have a negative impact on an organization.

A useful conceptual model is:

**Risk ≈ Probability/Likelihood × Impact**

### Probability / Likelihood

The probability or likelihood that a threat will be capable of exploiting a vulnerability.

### Impact

The magnitude of harm that could be caused by a threat exploiting a vulnerability.

---

## Authentication, Authorization, and Accounting (AAA)

### Authentication — Who are you?

Authentication verifies the identity of a user, device, or system.

### Authentication Factors

1. **Something you know** — Passwords, PINs, passphrases
2. **Something you have** — Tokens, smart cards, security keys
3. **Something you are** — Biometrics

### Single-Factor Authentication

Uses only one authentication factor.

### Multi-Factor Authentication (MFA)

Uses two or more different authentication factors for identity verification.

**Important:** Two passwords are still one factor because both are something you know.

### Token

A physical object a user possesses and controls that is used to authenticate their identity.

---

### Authorization — What are you allowed to do?

Authorization determines what an authenticated user, device, or system is permitted to access or perform.

**Examples**

- Read a file
- Modify a database
- Access a network
- Run an application

**Remember:**

Authentication = identity
Authorization = permissions

---

### Accounting — What did you do?

Accounting records and tracks user or system activity.

**Examples**

- Login records
- Audit logs
- File access logs
- System activity

---

## Non-Repudiation

**Non-repudiation** is the inability to deny taking an action, such as creating, approving, sending, or receiving information.

Common technologies include:

- Digital signatures
- Audit records

---

## Privacy

Privacy is the right of an individual to control the distribution of information about themselves.

### Personally Identifiable Information (PII)

Information that can identify an individual or is linked or linkable to an individual.

Examples can include:

- Name
- Social Security number
- Date/place of birth
- Biometric information
- Medical information
- Educational information
- Financial information
- Employment information

### Protected Health Information (PHI)

Information regarding health status, healthcare provision, or payment for healthcare as defined by HIPAA.

### Sensitivity

A measure of the importance assigned to information by its owner for the purpose of determining its need for protection.

---

## Data Integrity

Data integrity means information is recorded, used, and maintained in a way that preserves its:

- Completeness
- Accuracy
- Internal consistency
- Usefulness for its stated purpose

## System Integrity

A system has integrity when it performs its intended function in an unimpaired manner, free from unauthorized manipulation, whether intentional or accidental.

## Encryption

Encryption is the process of converting a message into a form that prevents unauthorized parties from understanding it.

---

# 1.2 Risk Management Process

Risk management is a major part of cybersecurity and information assurance.

Security decisions should consider the level of risk an organization is willing to accept.

## Risk Identification

Organizations identify risks in order to protect against them.

Employees at all levels can be responsible for identifying risk.

---

## Risk Assessment

Risk assessment is the process of identifying, analyzing, estimating, and prioritizing risks.

It considers risks to:

- Operations
- Mission and functions
- Image and reputation
- Assets
- Individuals
- Other organizations
- The nation

Risk assessment considers threats, vulnerabilities, and security controls that are planned or already in place.

---

## Risk Analysis

### Qualitative Risk Analysis

Uses descriptive categories to analyze risk.

Examples:

- Low
- Medium
- High

### Quantitative Risk Analysis

Uses numerical values for likelihood and impact, often using statistical probabilities and monetary values.

**Remember:**

Qualitative = descriptive
Quantitative = numerical

---

## Risk Prioritization

Risk can be prioritized using **probability/likelihood** and **impact**.

| Probability | Impact | General Risk Relationship |
|---|---|---|
| Low | Low | Lower |
| Low | High | Higher |
| High | Low | Higher |
| High | High | Highest |

---

## Risk Treatment

**Risk treatment** is determining the best way to address an identified risk.

### Risk Acceptance

Accepting the risk when the potential benefits of the business function outweigh the possible risk.

No additional action is taken to reduce the risk.

### Risk Avoidance

Not performing a business function because the risk's impact and/or likelihood is considered too great compared with the potential benefits.

### Risk Mitigation

Putting security controls in place to reduce the possible impact and/or likelihood of a specific risk.

### Risk Transference

Paying or otherwise using an external party to accept the financial impact of a given risk.

**Remember:**

- Accept = live with it
- Avoid = don't do it
- Mitigate = reduce it
- Transfer = shift the financial impact

---

## Risk Tolerance

Risk tolerance is the level of risk an entity is willing to assume in order to achieve a potential desired result.

---

## Risk Management

Risk management is the process of identifying, evaluating, and controlling threats.

It includes:

1. Risk identification
2. Risk assessment
3. Risk treatment
4. Risk monitoring

### Risk Management Framework

A structured approach used to oversee and manage risk for an enterprise.

---

# 1.3 Security Controls

Security controls are safeguards or countermeasures used to protect the confidentiality, integrity, and availability of systems and information.

## Physical Controls

Physical controls are implemented through tangible mechanisms.

Examples:

- Walls
- Fences
- Guards
- Locks
- Badge readers
- Cameras

## Technical Controls

Technical controls, also called logical controls, are security controls primarily implemented through hardware, software, or firmware.

Examples:

- Firewalls
- Encryption
- MFA
- IDS/IPS
- Access control systems

## Administrative Controls

Administrative controls, also called managerial controls, are directives, guidelines, or advisories aimed at people within an organization.

Examples:

- Policies
- Training
- Risk assessments
- Procedures
- Security guidelines

**Remember:**

Physical = tangible protection
Technical = technology
Administrative = people/management

---

# 1.4 Governance Elements

Governance is the process by which an organization is managed, including how decisions are made and how the organization is directed.

## Policies

Policies are established by organizational governance, such as executive management, to provide guidance for activities and support compliance with standards and regulations.

**Policy = direction**

## Standards

Standards provide a framework for implementing policies and procedures and supporting regulations.

**Standard = defined requirement**

## Procedures

Procedures are detailed steps used to complete a task and support organizational policies.

**Procedure = how to perform the task**

## Regulations and Laws

Regulations are commonly issued by governments and can carry penalties for non-compliance.

**Regulation/law = external requirement**

## Frameworks and Guidelines

Frameworks provide structured approaches for managing cybersecurity and risk.

Guidelines provide recommendations or direction rather than necessarily being mandatory requirements.

### Easy Distinction

**Policy → Standard → Procedure**

What the organization requires
↓
Specific requirements
↓
How to perform the task

---

## Important Organizations and Standards

### NIST — National Institute of Standards and Technology

A U.S. Department of Commerce organization involved in measurement infrastructure, science and technology, and information security standards and guidance.

### ISO — International Organization for Standardization

Develops voluntary international standards, including standards related to information and communication technologies.

### IETF — Internet Engineering Task Force

Develops Internet standards and protocols through collaboration and consensus.

Examples include standards related to:

- TCP
- DNS

### IEEE — Institute of Electrical and Electronics Engineers

A professional organization that develops standards for telecommunications, computer engineering, and related disciplines.

---

## Common Regulations / Laws and Data Categories

### GDPR — General Data Protection Regulation

A European Union regulation addressing data protection and privacy.

### HIPAA — Health Insurance Portability and Accountability Act

U.S. legislation addressing healthcare information and privacy, among other healthcare-related requirements.

---

# 1.5 ISC2 Code of Ethics

## Preamble

The safety and welfare of society and the common good, duty to our principles, and duty to each other require adherence to the highest ethical standards of behavior.

Strict adherence to the Code is a condition of ISC2 certification.

## Four Canons

### 1. Protect Society

Protect society, the common good, necessary public trust and confidence, and the infrastructure.

### 2. Act Honorably

Act honorably, honestly, justly, responsibly, and legally.

### 3. Provide Diligent and Competent Service

Provide diligent and competent service to principals.

### 4. Advance and Protect the Profession

Advance and protect the cybersecurity profession.

---

## Due Care

Taking reasonable steps to protect people, systems, and information.

## Due Diligence

Continuously investigating, evaluating, and maintaining security practices.

**Remember:**

Due care = reasonable protection
Due diligence = ongoing effort

---

---

# Domain 1 Quick Recall

### CIA Triad

| Concept | Remember |
|---|---|
| **Confidentiality** | Prevent unauthorized access |
| **Integrity** | Prevent unauthorized modification |
| **Availability** | Access when needed |

### Security Terminology

| Term | Remember |
|---|---|
| **Asset** | Something valuable that needs protection |
| **Threat** | Potential danger |
| **Threat actor** | Who causes or attempts to cause the threat |
| **Threat vector** | How the threat actor carries out the objective |
| **Vulnerability** | Weakness that can be exploited |
| **Risk** | Potential negative event/impact |
| **Likelihood / Probability** | Chance of occurrence |
| **Impact** | Magnitude of harm |

### Identity & Access

| Term | Remember |
|---|---|
| **Authentication** | Who are you? |
| **Authorization** | What can you do? |
| **Accounting** | What did you do? |
| **MFA** | Two or more different authentication factors |
| **Non-repudiation** | Inability to credibly deny an action |

### Risk

| Concept | Remember |
|---|---|
| **Qualitative** | Descriptive |
| **Quantitative** | Numerical |
| **Acceptance** | Accept the risk |
| **Avoidance** | Don't perform the activity |
| **Mitigation** | Reduce likelihood/impact |
| **Transference** | Shift financial impact |
| **Tolerance** | Amount of risk the organization is willing to assume |

### Controls

| Type | Remember |
|---|---|
| **Physical** | Tangible |
| **Technical** | Technology |
| **Administrative** | Management / people |

### Governance

| Element | Remember |
|---|---|
| **Policy** | Direction |
| **Standard** | Requirement |
| **Procedure** | Instructions |
| **Regulation / Law** | External legal requirement |

### Ethics

| Concept | Remember |
|---|---|
| **Due care** | Reasonable protection |
| **Due diligence** | Ongoing effort |
