---
description: Domain 1 --- Security Principles
---

# Domain 1 --- Security Principles

**Exam weight: 24%**\
**Current exam outline effective: September 1, 2026**

## 2026 Exam Objectives

### 1.1 Understand cybersecurity concepts

-   Confidentiality
-   Integrity
-   Availability
-   Authentication, Authorization, Accounting (AAA)
-   Non-repudiation
-   Privacy

### 1.2 Understand risk management concepts

-   Risk management lifecycle
-   Risk management processes

### 1.3 Understand governance concepts

-   Regulations and laws
-   Frameworks and guidelines
-   Policies
-   Standards
-   Procedures

### 1.4 Understand cybersecurity controls

-   Technical controls
-   Administrative controls
-   Physical controls

### 1.5 Maintain professional and ethical conduct

-   Professional code of conduct
-   Due care and due diligence
-   ISC2 Code of Ethics

------------------------------------------------------------------------

# 1.1 Cybersecurity Concepts

## CIA Triad

The **CIA Triad** is a foundation of information security.

  -----------------------------------------------------------------------
  Principle               Meaning                 Examples
  ----------------------- ----------------------- -----------------------
  **Confidentiality**     Prevent unauthorized    Access controls,
                          access or disclosure    encryption,
                                                  classification,
                                                  need-to-know

  **Integrity**           Prevent unauthorized    Hashing, digital
                          modification or         signatures, integrity
                          destruction             monitoring, change
                                                  controls

  **Availability**        Ensure authorized       Redundancy, backups,
                          access when needed      failover, disaster
                                                  recovery, load
                                                  balancing
  -----------------------------------------------------------------------

**Remember:**\
Confidentiality = prevent unauthorized access\
Integrity = prevent unauthorized changes\
Availability = access when needed

------------------------------------------------------------------------

## Assets

An **asset** is something of value that needs protection.

Examples: - Information - Hardware - Software - Systems - People -
Reputation

------------------------------------------------------------------------

## Threats

A **threat** is a circumstance or event with the potential to adversely
affect an organization, its assets, individuals, or other entities.

Threats can involve: - Unauthorized access - Disclosure - Destruction -
Modification - Denial of service

### Common Threat Actors

-   **Insiders** --- trusted individuals who may act deliberately or
    accidentally
-   **Outside individuals or informal groups** --- external attackers
-   **Nonpolitical formal entities** --- competitors or cybercriminal
    groups
-   **Political formal entities** --- nation-states, terrorists, or
    hacktivists
-   **Intelligence/information gatherers**
-   **Technology** --- bots and artificial intelligence can also be
    involved in threats

### Threat Actor

A **threat actor** is an individual or group that attempts to exploit a
vulnerability.

### Threat Vector

A **threat vector** is the means by which a threat actor carries out an
objective.

**Threat actor = who**\
**Threat vector = how**

------------------------------------------------------------------------

## Vulnerability

A **vulnerability** is a weakness in an information system, security
procedure, internal control, or implementation that could be exploited.

Examples: - Unpatched software - Weak passwords - Misconfigured
systems - Missing security controls

**Threat = potential danger**\
**Vulnerability = weakness**\
**Threat actor = who exploits it**\
**Threat vector = how they do it**

------------------------------------------------------------------------

## Risk

Risk is a possible event or condition that can negatively affect an
organization.

A useful conceptual model is:

**Risk ≈ Likelihood × Impact**

### Likelihood

The probability that a threat will be capable of exploiting a
vulnerability.

### Impact

The magnitude of harm that could result.

------------------------------------------------------------------------

## Authentication, Authorization, and Accounting (AAA)

### Authentication --- Who are you?

Authentication verifies the identity of a user, device, or system.

### Authentication Factors

1.  **Something you know** --- password, PIN, passphrase
2.  **Something you have** --- token, smart card, security key
3.  **Something you are** --- biometric characteristic

### Single-Factor Authentication

Uses one authentication factor.

### Multi-Factor Authentication (MFA)

Uses two or more **different** authentication factors.

> Two passwords are still one factor because both are something you
> know.

### Token

A physical object a user possesses and controls that can be used for
authentication.

### Authorization --- What are you allowed to do?

Authorization determines what an authenticated identity is permitted to
access or perform.

### Accounting --- What did you do?

Accounting records and tracks user or system activity.

Examples: - Login records - Audit logs - File access logs - System
activity

**Authentication = identity**\
**Authorization = permissions**\
**Accounting = activity**

------------------------------------------------------------------------

## Non-Repudiation

**Non-repudiation** provides evidence that helps prevent someone from
credibly denying an action.

Examples: - Digital signatures - Audit records

------------------------------------------------------------------------

## Privacy

Privacy concerns an individual's ability to control the distribution and
use of information about themselves.

### Personally Identifiable Information (PII)

Information that identifies or can be linked to an individual.

Examples can include: - Name - Social Security number - Date/place of
birth - Biometrics - Medical information - Educational information -
Financial information - Employment information

### Protected Health Information (PHI)

Information relating to health status, healthcare provision, or payment
for healthcare as defined by HIPAA.

### Sensitivity

The importance assigned to information by its owner for determining the
level of protection it requires.

------------------------------------------------------------------------

## Data Integrity

Data integrity means information is maintained with: - Completeness -
Accuracy - Internal consistency - Usefulness for its purpose

## System Integrity

A system has integrity when it performs its intended function without
unauthorized manipulation.

## Encryption

Encryption converts information into a form intended to prevent
unauthorized parties from understanding it.

------------------------------------------------------------------------

# 1.2 Risk Management Concepts

## Risk Management

Risk management is the process of identifying, evaluating, treating, and
monitoring threats and risks.

Security decisions should consider the amount of risk an organization is
willing to accept.

## Risk Identification

Organizations identify risks in order to understand what could affect
assets, operations, people, or objectives.

Employees at different levels can identify risks.

## Risk Assessment

Risk assessment involves identifying, analyzing, estimating, and
prioritizing risks.

It can consider risks to: - Operations - Mission and functions - Image
and reputation - Assets - Individuals - Other organizations - The nation

Risk assessment considers threats, vulnerabilities, and controls.

### Qualitative Risk Analysis

Uses descriptive categories.

Examples: - Low - Medium - High

**Qualitative = descriptive**

### Quantitative Risk Analysis

Uses numerical values for likelihood and impact, often including
statistical probabilities or monetary values.

**Quantitative = numerical**

## Risk Prioritization

Risk can be prioritized using likelihood and impact.

  Likelihood   Impact   General relationship
  ------------ -------- ----------------------
  Low          Low      Lower
  Low          High     Higher
  High         Low      Higher
  High         High     Highest

## Risk Treatment

### Accept

Accept the risk and continue the activity.

### Avoid

Do not perform the activity creating the risk.

### Mitigate

Implement controls to reduce likelihood and/or impact.

### Transfer

Use another party to take on some of the financial or operational
consequences of the risk.

**Accept = live with it**\
**Avoid = don't do it**\
**Mitigate = reduce it**\
**Transfer = shift consequences**

## Risk Tolerance

**Risk tolerance** is the level of risk an organization is willing to
assume to achieve a desired result.

## Risk Management Lifecycle

Know the basic flow:

1.  **Identify** risk
2.  **Assess/analyze** risk
3.  **Treat/respond** to risk
4.  **Monitor/review** risk

------------------------------------------------------------------------

# 1.3 Governance Concepts

## Governance

Governance is how an organization is directed, managed, and overseen,
including how decisions are made.

## Policies

Policies provide high-level organizational direction.

**Policy = direction**

## Standards

Standards provide defined requirements that support policies and
procedures.

**Standard = requirement**

## Procedures

Procedures provide detailed steps for completing a task.

**Procedure = how**

## Regulations and Laws

Regulations and laws establish external requirements that organizations
may be legally required to follow.

**Regulation/law = external legal requirement**

## Frameworks and Guidelines

**Frameworks** provide structured approaches for managing cybersecurity
and risk.

**Guidelines** provide recommendations or direction and are not
necessarily mandatory.

### Important Organizations

**NIST** --- U.S. organization involved in standards and cybersecurity
guidance.

**ISO** --- develops international standards, including information and
communications technology standards.

**IETF** --- develops Internet standards and protocols.

**IEEE** --- develops standards for telecommunications, computing, and
related fields.

### Common Regulations/Laws

**GDPR** --- European Union regulation concerning data protection and
privacy.

**HIPAA** --- U.S. healthcare legislation addressing healthcare
information and privacy, among other requirements.

### Governance Relationship

A useful conceptual distinction is:

**Policy → Standard → Procedure**

-   Policy = what/why
-   Standard = specific requirement
-   Procedure = how

> The exact hierarchy among laws, regulations, standards, policies, and
> procedures can vary by context. Focus on the function of each element
> rather than memorizing an absolute hierarchy.

------------------------------------------------------------------------

# 1.4 Cybersecurity Controls

Security controls are safeguards or countermeasures used to protect
systems and information.

## Physical Controls

Tangible protections.

Examples: - Walls - Fences - Guards - Locks - Badge readers - Cameras

## Technical Controls

Technology-based controls implemented through hardware, software, or
firmware.

Examples: - Firewalls - Encryption - MFA - IDS/IPS - Access control
systems

## Administrative Controls

Management and organizational controls directed at people and processes.

Examples: - Policies - Training - Risk assessments - Procedures -
Security guidelines

**Physical = tangible**\
**Technical = technology**\
**Administrative = management/people**

------------------------------------------------------------------------

# 1.5 Professional and Ethical Conduct

## Professional Code of Conduct

Cybersecurity professionals should act responsibly, ethically, legally,
and competently.

## Due Care

Taking reasonable steps to protect people, systems, and information.

## Due Diligence

Continuously investigating, evaluating, and maintaining security
practices.

**Due care = reasonable protection**\
**Due diligence = ongoing effort**

------------------------------------------------------------------------

## ISC2 Code of Ethics

### Preamble

The safety and welfare of society and the common good, duty to our
principles, and duty to each other require adherence to high ethical
standards.

Strict adherence to the Code is a condition of ISC2 certification.

### Four Canons

#### 1. Protect Society

Protect society, the common good, necessary public trust and confidence,
and infrastructure.

#### 2. Act Honorably

Act honorably, honestly, justly, responsibly, and legally.

#### 3. Provide Diligent and Competent Service

Provide diligent and competent service to principals.

#### 4. Advance and Protect the Profession

Advance and protect the cybersecurity profession.

------------------------------------------------------------------------

# Domain 1 Quick Recall

  Term                     Remember
  ------------------------ --------------------------------------------------
  Confidentiality          Prevent unauthorized access
  Integrity                Prevent unauthorized modification
  Availability             Access when needed
  Authentication           Who are you?
  Authorization            What can you do?
  Accounting               What did you do?
  MFA                      Two or more different factors
  Non-repudiation          Evidence against denying an action
  Asset                    Something valuable needing protection
  Threat                   Potential danger
  Threat actor             Who
  Threat vector            How
  Vulnerability            Weakness
  Risk                     Potential negative impact
  Qualitative              Descriptive
  Quantitative             Numerical
  Accept                   Live with risk
  Avoid                    Don't perform activity
  Mitigate                 Reduce risk
  Transfer                 Shift consequences
  Tolerance                Risk level the organization is willing to assume
  Physical control         Tangible
  Technical control        Technology
  Administrative control   Management/people
  Policy                   Direction
  Standard                 Requirement
  Procedure                How
  Due care                 Reasonable protection
  Due diligence            Ongoing effort

------------------------------------------------------------------------

# Active Recall

1.  Explain confidentiality, integrity, and availability.
2.  What is the difference between a threat and a vulnerability?
3.  What is the difference between a threat actor and a threat vector?
4.  Explain authentication, authorization, and accounting.
5.  What makes MFA multi-factor?
6.  What is non-repudiation?
7.  What is PII? What is PHI?
8.  Explain qualitative versus quantitative risk analysis.
9.  Explain accept, avoid, mitigate, and transfer.
10. What is risk tolerance?
11. Explain the risk management lifecycle.
12. Distinguish policy, standard, and procedure.
13. Distinguish physical, technical, and administrative controls.
14. Explain due care versus due diligence.
15. State the four ISC2 Code of Ethics canons.
