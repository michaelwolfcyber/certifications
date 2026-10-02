---
description: 'After completing this domain you need to be able to:'
---

# Domain 1 — Security Principles

* Discuss the foundational concepts of cybersecurity principles.
* Recognize foundational security concepts of information assurance.&#x20;
* Define risk management terminology and summarize the process.
* Relate risk management to personal or proffesional practices.&#x20;
* Classify types of security controls.&#x20;
* Distinguish between policies, procedures and standards, regulations and laws.&#x20;
* Demonstrate the relationship among governance elements.
* Analyze appropriate outcomes according to the canons of the ISC2 Code of Ethics when given examples.&#x20;
* Practice the terminology and review security principles.&#x20;

**KEY TOPICS:**&#x20;

* Identity Assurance
* Privacy Control Mechanisms
* Safeguarding Data
* Strategic Risk Management&#x20;

**Exam weight: 24%**

## 1.1 Cybersecurity Concepts

### Confidentiality

Confidentiality means preventing unauthorized people or systems from accessing information.

**Examples**

* Access controls
* Encryption
* Data classification
* Need-to-know access

### Integrity

Integrity means protecting information from unauthorized modification or destruction.

**Examples**

* Hashing
* Digital signatures
* File integrity monitoring
* Change controls

### Availability

Availability means authorized users can access systems and information when needed.

**Examples**

* Redundancy
* Backups
* Failover
* Disaster recovery
* Load balancing

### Authentication, Authorization, and Accounting (AAA)

#### **Authentication:** Who are you?

* Authentication is the process of validating your identity.

&#x20; There are three common methods of authentication:

1. Something you know: Passwords or passphrases.
2. Something you have: Tokens, memory cards, smart cards.
3. Something you are: Biometrics, measurable characteristics.&#x20;

#### **Authorization:** What are you allowed to do?



#### **Accounting:** What did you do?

Do not confuse authentication with authorization.

### Non-repudiation

Non-repudiation provides evidence that helps prevent someone from credibly denying an action or transaction.

Common technologies include digital signatures and audit records.

### Privacy

Privacy is the right of an individual to control the distribution of information about themselves.&#x20;

Ex: Not wanting to let Amazon see what you see in a different app like instagram via cookies.

***

## 1.1 AI Security Context — Current ISC2 2026 Guidance

ISC2 explicitly integrates foundational AI concepts across the CC domains.

For Domain 1, understand the basic security implications of AI systems:

- **Confidentiality:** protect sensitive AI training data, prompts, outputs, and other information.
- **Integrity:** protect AI data and models from unauthorized modification, including the risk of **model poisoning**.
- **Availability:** ensure AI-enabled services remain available when needed.
- **AAA:** apply authentication, authorization, and accounting to AI users, bots, and AI-enabled actions.
- **Non-repudiation:** maintain traceability for AI-generated actions where appropriate.
- **Privacy:** protect personal and sensitive information used by or processed by AI systems.
- **Controls:** AI systems can require technical, administrative, and physical controls.
- **Governance:** AI use remains subject to organizational policies, legal requirements, risk decisions, due care, and due diligence.

### Exam-level takeaway

You do **not** need advanced machine-learning knowledge for CC. Think:

**AI + CIA + AAA + privacy + governance + controls**

> **Source note:** This is current ISC2 2026 guidance expanding the concise 1.1–1.5 outline bullets; it is not a separate Domain 1 sub-objective.

***

## 1.2 Risk Management Concepts

Information Assurance and Cybersecurity are very involved with Risk Management.&#x20;

The level of security required depends on the level of risk the entity is ready to accept.&#x20;

### Risk

Risk is the possibility that a threat will exploit a vulnerability and cause harm.

A useful conceptual model is:

**Risk ≈ Likelihood × Impact**

#### **Example of Risks:**

* Cyber Attacks such as malware.
* Social Engineering.
* Denial of Service.
* Other situations such as fire or natural disasters.&#x20;

### Risk Management Lifecycle

Know the basic flow:

1. Identify risk
2. Assess/analyze risk
3. Treat/respond to risk
4. Monitor and review

### Risk Treatment

Common approaches include:

* **Mitigate:** Reduce likelihood or impact.
* **Transfer:** Shift some financial or operational consequences to another party.
* **Avoid:** Stop the activity creating the risk.
* **Accept:** Acknowledge the risk and continue.

### Risk Tolerance

Risk tolerance describes how much risk an organization is willing to accept.

### Risk Priorities

Risk decisions should consider factors such as:

* Business impact
* Likelihood
* Asset importance
* Threat exposure
* Regulatory requirements

***

## 1.3 Governance Concepts

### Regulations and Laws

Legal and regulatory requirements establish obligations an organization must follow.

### Frameworks and Guidelines

Frameworks provide structured approaches for managing cybersecurity.

### Policies

High-level management direction describing what the organization requires.

### Standards

Specific mandatory requirements that support a policy.

### Procedures

Step-by-step instructions for carrying out a task.

**Easy distinction:**

Policy = what/why\
Standard = required rule\
Procedure = how

***

## 1.4 Cybersecurity Controls

### Technical Controls

Technology-based protections.

Examples:

* Firewalls
* Encryption
* MFA
* IDS/IPS

### Administrative Controls

Management and organizational protections.

Examples:

* Policies
* Training
* Risk assessments
* Procedures

### Physical Controls

Physical protections.

Examples:

* Locks
* Guards
* Cameras
* Fences
* Badge systems

***

## 1.5 Professional and Ethical Conduct

### Due Care

Taking reasonable steps to protect people, systems, and information.

### Due Diligence

Continuously investigating, evaluating, and maintaining security practices.

### Professional Conduct

Cybersecurity professionals should act responsibly, protect information, follow applicable requirements, and avoid actions that cause unnecessary harm.

### ISC2 Code of Ethics

IT Professionals are expected to be honorable, honest, just and responsible within legal conduct.&#x20;

ISC2 Code of Ethics Preamble:&#x20;

* The safety and welfare of society and the common good, duty to our principles and duty to each other require that we adhere and be seen to adhere to the highest ethical standards of behavior.&#x20;
* Therefore, strict adherence to this code is a condition of certification.&#x20;

ISC2 Code of Ethics Canons:&#x20;

* Protect society, the common good, necessary public trust, confidence and infrastructure.&#x20;
* Act honorably, honestly, justly, responsibly and legally.&#x20;
* Provide diligent and competent service to principles.&#x20;
* Advance and protect the profession.&#x20;

***

## Quick Recall

* CIA = Confidentiality, Integrity, Availability
* Asset = Something in need of protection
* A vulnerability = A gap or weakness in protection&#x20;
* A threat = Something or someone that aims to exploit vulnerability.&#x20;
* Authentication = identity
* Authorization = permissions
* Accounting = activity
* Risk = likelihood and impact
* Policy = direction
* Standard = requirement
* Procedure = instructions
* Technical = technology
* Administrative = management
* Physical = environment
* Due care = reasonable protection
* Due diligence = ongoing effort


---

# Exam Objective Checklist

- [ ] **1.1 Cybersecurity concepts**
  - [ ] Confidentiality
  - [ ] Integrity
  - [ ] Availability
  - [ ] AAA
  - [ ] Non-repudiation
  - [ ] Privacy
  - [ ] Foundational AI security implications
- [ ] **1.2 Risk management concepts**
  - [ ] Risk management lifecycle
  - [ ] Risk identification, assessment, treatment, monitoring
  - [ ] Risk priorities and tolerance
- [ ] **1.3 Governance concepts**
  - [ ] Regulations and laws
  - [ ] Frameworks and guidelines
  - [ ] Policies
  - [ ] Standards
  - [ ] Procedures
- [ ] **1.4 Cybersecurity controls**
  - [ ] Technical
  - [ ] Administrative
  - [ ] Physical
- [ ] **1.5 Professional and ethical conduct**
  - [ ] Professional code of conduct
  - [ ] Due care
  - [ ] Due diligence
  - [ ] ISC2 Code of Ethics
