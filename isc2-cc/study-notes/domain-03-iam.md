# Domain 3 — Identity and Access Management (IAM) Concepts

**Exam weight: 20%**  
**Current CC exam outline effective: September 1, 2026**

> **Study goal:** Understand how access is granted, limited, monitored, reviewed, and removed. Be able to select the appropriate access control in a scenario.

---

# 2026 Exam Objectives

## 3.1 Understand identity life cycle management

- Roles definition
- Provision
- Review
- Deprovision
- Frameworks and tools

## 3.2 Understand logical access controls

- Principle of Least Privilege (PoLP)
- Separation of Duties (SoD)
- Access control models

---

# 3.1 Identity Life Cycle Management

Identity lifecycle management controls an identity from creation through removal.

## Identity Lifecycle

**Define role → Provision → Review → Deprovision**

The key idea is that access should **change with the user's job and responsibilities** and should be **removed when it is no longer required**.

## Roles Definition

Determine what access a person or identity should have based on:

- Job role
- Responsibilities
- Business need
- Required resources
- Level of authority

**Role definition = determine what access the identity should need.**

## Provisioning

**Provisioning** is the process of creating, maintaining, and assigning access to a user identity.

It can include:

- Creating an account
- Assigning permissions
- Assigning the user to appropriate groups or roles
- Providing required resources
- Applying appropriate security settings

### Common lifecycle situations

| Situation | Access action |
|---|---|
| New employee | Create account and assign appropriate access |
| Employee changes position | Modify access to match the new role |
| Temporary leave | Disable or otherwise restrict access as required |
| Employee leaves | Deactivate/remove access |

### Onboarding

**Onboarding** establishes an account and the access needed by a new employee.

### Offboarding

**Offboarding** disables/deletes an account and removes access for a terminated or departing employee.

**Exam idea:** Access should follow the person's current job, not their previous job.

## Review

Access should be periodically reviewed to verify that permissions remain appropriate.

Reviews can identify:

- Excessive permissions
- Unused accounts
- Outdated role assignments
- Access that is no longer required
- Privileged access that should be removed or restricted

**Review = verify that existing access is still justified.**

## Deprovisioning

**Deprovisioning** removes or disables access when it is no longer required.

It is especially important when:

- An employee leaves the organization
- An employee changes roles
- A temporary account expires
- A contractor's assignment ends
- Access is no longer justified

> **Scenario:** An employee transfers from accounting to marketing but keeps access to the accounting database. The user's access should be reviewed and modified through the identity lifecycle.

## Frameworks and Tools

IAM frameworks and tools help organizations manage identities and access throughout the lifecycle.

They can support:

- Identity creation
- Access assignment
- Role/group management
- Authentication
- Access review
- Access removal
- Privileged access management

**Remember:** the lifecycle is the process; IAM tools help organizations implement and manage that process.

---

# 3.2 Logical Access Controls

**Logical access controls** are technical mechanisms used to control access to systems, applications, networks, accounts, and data.

ISC2's CC material describes logical access control systems as automated systems that control an individual's ability to access computer-system resources. They validate identity through mechanisms such as a PIN, card, biometric, or other token and can assign different privileges based on roles and responsibilities.

### Examples

- Account permissions
- Passwords/PINs
- Authentication mechanisms
- File permissions
- Security groups
- Access-control lists
- Application permissions
- Configuration settings managed through software

**Logical = technical/software-based access.**

---

# Principle of Least Privilege (PoLP)

**Least privilege** means users and programs should have only the **minimum privileges necessary to complete their tasks**.

### Goal

Reduce:

- Unnecessary access
- Accidental misuse
- Abuse of privileges
- Damage from compromised accounts
- Potential impact of an attacker

**Least privilege = minimum necessary access.**

> **Scenario:** A user only needs to read a database. Giving them permission to modify or delete records violates least privilege.

---

# Privileged Access

A **privileged account** is an account with elevated or administrative authorization.

Examples may include:

- System administrator
- Database administrator
- Network administrator
- Security administrator

Privileged access should be carefully controlled because compromise of a privileged account can provide extensive access to systems and data.

## Privileged Access Management (PAM)

**Privileged Access Management (PAM)** is the management and control of privileged accounts and administrative access.

ISC2's material emphasizes using administrative privileges only when needed and limiting administrative access during routine activities.

### Key PAM principles

- Limit administrative privileges to what is necessary
- Avoid using privileged accounts for routine work
- Allow administrative access during approved activities
- Provide elevated access when needed
- Remove/restrict elevated access when it is no longer needed

> **Scenario:** An administrator uses a normal account for email and web browsing and a privileged account only for approved administrative tasks. This supports **least privilege and PAM**.

---

# Separation of Duties (SoD)

**Separation of Duties (SoD)** divides sensitive responsibilities among different people or roles.

The goal is to prevent one person from controlling all critical steps of a sensitive process.

### Why SoD matters

It reduces the risk of:

- Fraud
- Abuse
- Insider threats
- Unauthorized changes
- Mistakes

> **Example:** One employee requests a payment while another approves it.

**SoD = separate critical responsibilities.**

## SoD vs Least Privilege

| Concept | Main idea |
|---|---|
| **Least Privilege** | Give an identity only the access it needs |
| **Separation of Duties** | Divide sensitive responsibilities among multiple people/roles |

They are related, but they solve different problems.

---

# Access Control Fundamentals

ISC2 presents access control around three basic elements:

| Element | Meaning |
|---|---|
| **Subject** | The entity requesting or causing access |
| **Object** | The resource being accessed |
| **Rule** | The instruction that allows or denies access |

### Subject

A **subject** is generally the individual, process, or device attempting to access a resource or change system state.

Examples:

- User
- Application
- Process
- Device

### Object

An **object** is a passive information-system resource containing or receiving information.

Examples:

- File
- Database record
- Table
- Program
- Device
- Domain

### Rule

A **rule** determines whether access should be allowed or denied by comparing the validated identity of the subject with applicable access permissions.

### Easy mental model

**Subject → requests access → Object**  
**Rule → decides allow/deny**

---

# Access Control Models

## Discretionary Access Control (DAC)

**DAC** allows the owner of an object, or someone authorized by the owner, to determine who can access the object and what rights they have.

**DAC = owner-controlled**

> **Example:** A file owner decides which users can read or modify the file.

### Key characteristic

The owner has discretion over access.

## Mandatory Access Control (MAC)

**MAC** requires the system itself to enforce access according to centrally defined security policies.

Access is commonly associated with:

- Security labels
- Classifications
- Centrally enforced rules

**MAC = centrally/system enforced**

> **Example:** A system uses security classifications and allows access only when the subject's authorization permits access to that classification.

### Key characteristic

Users/owners cannot simply change the access decision at their discretion.

## Role-Based Access Control (RBAC)

**RBAC** assigns permissions according to organizational roles.

**RBAC = role-based**

> **Example:** A database administrator receives the permissions associated with the **DBA role**.

Mental model:

**User → Role → Permissions**

### Why RBAC is useful

When many users perform similar jobs, permissions can be assigned to the role and users can be assigned to that role.

---

# DAC vs MAC vs RBAC

| Model | Access is primarily based on | Remember |
|---|---|---|
| **DAC** | Owner's discretion | **Owner-controlled** |
| **MAC** | Centrally enforced security policy/labels | **System-controlled** |
| **RBAC** | Organizational role | **Role-controlled** |

### Exam clues

- **Owner decides** → DAC
- **Classification/labels/central policy** → MAC
- **Job function/role** → RBAC

---


---

## Supplemental 2026 ISC2 AI Context

ISC2's current 2026 guidance applies IAM concepts to AI systems and automated identities.

Know these foundational ideas:

- AI **bots and automated service accounts** should go through identity lifecycle management.
- Apply **least privilege** so automated systems receive only the permissions they need.
- Apply **Separation of Duties** where appropriate.
- Use established access-control models to constrain AI-enabled systems.
- AI can support authentication security through **behavioral analysis**, such as identifying anomalous login patterns or impossible-travel behavior.
- **MFA** remains a foundational access-control concept.

> **Exam-level takeaway:** Treat an AI bot/service account as an identity that needs appropriate provisioning, review, least privilege, and deprovisioning.


# Supplemental ISC2 Course Material — Physical Access Controls

> **2026 scope note:** Physical access controls appear in the ISC2 Domain 3 course material you provided, but they are **not a separate 3.x objective in the current September 1, 2026 exam outline**. They are retained because ISC2 teaches them as access-control concepts and because physical controls remain part of the broader CC exam. Treat this section as supporting knowledge rather than a standalone Domain 3 blueprint item.

## Physical Access Controls

Access control is not limited to software. ISC2 also covers **physical access controls**.

**Physical access controls** use tangible mechanisms to control entry to buildings, rooms, equipment, or other physical areas.

### Examples

- Security guards
- Fences
- Motion detectors
- Locked doors/gates
- Sealed windows
- Lights
- Cable protection
- Laptop locks
- Badges
- Swipe cards
- Cameras
- Guard dogs
- Mantraps
- Turnstiles
- Alarms

### Physical vs Logical

| Physical | Logical |
|---|---|
| Badge reader on a door | User account |
| Fence | File permission |
| Security guard | Access-control rule |
| Mantrap | Authentication mechanism |
| Laptop lock | Application permission |

**Physical = controls access to physical spaces/assets.**  
**Logical = controls access to systems/data.**

---

# Mantrap

A **mantrap** is an entrance to a building or area that requires people to pass through two doors, with only one door opening at a time.

**Mantrap = two-door controlled entry.**

# Turnstile

A **turnstile** is a one-way spinning door or barrier that generally allows only one person at a time to enter or pass through an area.

**Turnstile = controlled one-person-at-a-time entry.**

# Crime Prevention Through Environmental Design (CPTED)

**CPTED** is an architectural approach to designing buildings and spaces using features intended to reduce the likelihood of criminal activity.

**CPTED = security through environmental design.**

---

# Defense in Depth

**Defense in depth** is a security strategy that uses multiple layers of controls to protect assets.

ISC2 describes it as integrating people, technology, and operational capabilities to establish multiple barriers across layers and missions of an organization.

### Layers can include

- Administrative controls
- Technical/logical controls
- Physical controls
- People and operational processes

### Why use multiple controls?

If one control fails, another control may still provide protection.

> **Example:** A sensitive server room could use a security policy, employee authorization, badge access, a mantrap, a locked server rack, network access controls, and system authentication.

**Defense in depth = multiple layers of protection.**

> Defense in depth reduces risk, but it does **not** guarantee that an attack will never succeed.

---

# Layered Defense

**Layered defense** means using multiple controls arranged in sequence to provide several consecutive protections for an asset.

The ISC2 Domain 3 graphic illustrates the concept with **physical controls, logical/technical controls, and administrative controls** surrounding the protected asset.

**Multiple control categories can work together instead of relying on one control alone.**

---

# Authorized vs Unauthorized Personnel

### Authorized personnel

People who have been granted permission to access a resource or area.

### Unauthorized personnel

People who have not been granted the required permission.

> **Scenario:** A person follows an employee into a restricted server room without presenting a badge. They may be physically present, but they are **not authorized** to access the area.

**Authorization determines whether access is permitted.**

---

# Monitoring and Logging

Access controls should be monitored to identify unusual or unauthorized activity.

## Logging

**Logging** is collecting and storing user/system activities in a log.

Examples of events that may be logged:

- Authentication attempts
- Access attempts
- Administrative actions
- System events
- Configuration changes

## Log Anomaly

A **log anomaly** is a system irregularity identified while examining logs that may represent an event requiring further investigation.

## Log Consolidation

**Log consolidation** combines logs from multiple systems so they can be centrally reviewed and analyzed.

## Log Retention

**Log retention** means keeping logs for a defined period so they remain available for monitoring, investigation, auditing, or organizational requirements.

**Logging = record events.**  
**Monitoring = watch/analyze events.**

---

# Security Controls Relevant to Access

| Control type | Examples |
|---|---|
| **Administrative** | Policies, procedures, role definitions |
| **Technical/Logical** | Authentication, permissions, access-control systems |
| **Physical** | Guards, locks, badges, fences, mantraps |

A strong access-control strategy can combine multiple categories.

---

# High-Yield Comparisons

## Least Privilege vs Separation of Duties

**Least privilege:** Give one identity only the permissions it needs.

**Separation of duties:** Prevent one person from controlling all critical steps.

## Provisioning vs Deprovisioning

**Provisioning:** Create/assign access.

**Deprovisioning:** Remove/disable access.

## Physical vs Logical Access

**Physical:** Controls access to places and physical assets.

**Logical:** Controls access to systems, applications, networks, and data.

## DAC vs MAC vs RBAC

**DAC:** Owner decides.  
**MAC:** System/central policy decides.  
**RBAC:** Role determines permissions.

## Authentication vs Authorization

**Authentication:** Who are you?  
**Authorization:** What are you allowed to access/do?

## Defense in Depth vs Single Control

**Single control:** One primary barrier.  
**Defense in depth:** Multiple layers of protection so one failed control does not necessarily expose the asset.

---

# Scenario Thinking

When reading an access-control question, ask:

1. **Who** is requesting access?
2. **What** resource are they trying to access?
3. **Why** do they need it?
4. What permissions are actually required?
5. Is the access still necessary?
6. Is the person authorized?
7. Is the control physical or logical?
8. Is the question describing least privilege?
9. Is the question describing separation of duties?
10. Which access-control model is being described?
11. Is the question about creating, reviewing, modifying, or removing access?
12. Are multiple layers of controls being used?

---

# Exam Scenario Examples

### Scenario 1 — Least Privilege

> A user needs to read a file but does not need to modify it.

**Answer concept:** Least privilege. Give the user the minimum permission required.

### Scenario 2 — Separation of Duties

> One employee creates a purchase order and another approves it.

**Answer concept:** Separation of Duties.

### Scenario 3 — DAC

> A file's owner decides which users can access it.

**Answer concept:** DAC.

### Scenario 4 — MAC

> Access is determined by centrally enforced security classifications.

**Answer concept:** MAC.

### Scenario 5 — RBAC

> All database administrators receive permissions associated with the DBA role.

**Answer concept:** RBAC.

### Scenario 6 — Role Change

> An employee transfers departments but keeps permissions from the previous department.

**Answer concept:** Identity lifecycle/access review. Access should be reviewed and adjusted to the new role.

### Scenario 7 — Offboarding

> An employee leaves the organization, but their account remains active.

**Answer concept:** Deprovisioning failure.

### Scenario 8 — Defense in Depth

> A data center requires a badge, a mantrap, and a locked server room.

**Answer concept:** Defense in depth / layered security.

### Scenario 9 — Privileged Access

> An administrator uses an elevated account for ordinary web browsing and email.

**Answer concept:** PAM / least privilege. Administrative privileges should be limited to tasks that require them.

---

# Quick Recall

| Concept | Remember |
|---|---|
| Identity lifecycle | Define → Provision → Review → Deprovision |
| Provisioning | Create/assign access |
| Review | Verify access remains appropriate |
| Deprovisioning | Remove/disable access |
| Least privilege | Minimum necessary access |
| SoD | Separate critical responsibilities |
| Privileged account | Elevated authorization |
| PAM | Control/manage privileged access |
| Subject | Requests/causes access |
| Object | Resource being accessed |
| Rule | Allows/denies access |
| DAC | Owner-controlled |
| MAC | Centrally/system enforced |
| RBAC | Role-based |
| Physical access | Tangible barriers/mechanisms |
| Logical access | Technical/system access |
| Mantrap | Two-door controlled entry |
| Turnstile | One-person-at-a-time barrier |
| Logging | Record/store events |
| Log anomaly | Unusual event in logs |
| Defense in depth | Multiple layers of protection |
| CPTED | Security through environmental design |

---

# Active Recall

Answer these **without looking at the notes**.

1. What is identity lifecycle management?
2. What are the four major lifecycle stages?
3. What happens during provisioning?
4. Why should access be reviewed?
5. When should deprovisioning occur?
6. What is least privilege?
7. Why is least privilege important?
8. What is a privileged account?
9. What is Privileged Access Management?
10. What is Separation of Duties?
11. How is SoD different from least privilege?
12. What is a subject?
13. What is an object?
14. What is a rule?
15. What is DAC?
16. What is MAC?
17. What is RBAC?
18. Which model is owner-controlled?
19. Which model is centrally enforced?
20. Which model is based on organizational roles?
21. What is the difference between physical and logical access controls?
22. What is a mantrap?
23. What is a turnstile?
24. What is CPTED?
25. What is defense in depth?
26. Why are multiple controls useful?
27. What is logging?
28. What is a log anomaly?
29. What is the difference between authentication and authorization?
30. What should happen when an employee changes roles?
31. What should happen when an employee leaves the organization?
32. Why should privileged accounts not be used for routine activities?

---

# One-Minute Exam Sheet

### Lifecycle
**Define role → Provision → Review → Deprovision**

### Access control
**Subject → Object → Rule**

### Principles
**Least privilege = minimum access**  
**SoD = split critical responsibilities**

### Models
**DAC = owner**  
**MAC = central/system policy**  
**RBAC = role**

### Access types
**Physical = places/assets**  
**Logical = systems/data**

### Privileged access
**PAM = control elevated/admin access**

### Monitoring
**Logging = record**  
**Monitoring = observe/analyze**  
**Log anomaly = unusual event**

### Layered security
**Defense in depth = multiple controls/layers**

---

# Source Alignment Note

These notes combine the user's original Domain 3 study notes with the ISC2 2026 Domain 3 **Access Control Concepts** material provided for this study set.

The ISC2 material identifies Domain 3 learning objectives around selecting appropriate access controls in scenarios, relating access-control concepts and processes, comparing physical access controls, describing logical access controls, and practicing access-control terminology. It organizes the material around access-control concepts, physical access controls, and logical access controls.

The ISC2 resource specifically reinforces:

- Subjects, objects, and rules
- Defense in depth
- Privileged Access Management
- User provisioning and lifecycle events
- Physical access controls
- Monitoring and logging
- DAC, MAC, and RBAC
- Least privilege
- Separation of Duties

The current 2026 exam outline remains the controlling scope for the exam objectives listed at the beginning of this document.


---

# Exam Objective Checklist

- [ ] **3.1 Identity life cycle management**
  - [ ] Roles definition
  - [ ] Provision
  - [ ] Review
  - [ ] Deprovision
  - [ ] Frameworks and tools
  - [ ] AI bots/service accounts as managed identities
- [ ] **3.2 Logical access controls**
  - [ ] Principle of Least Privilege
  - [ ] Separation of Duties
  - [ ] Access control models
  - [ ] DAC
  - [ ] MAC
  - [ ] RBAC
- [ ] Explain subject, object, and rule
- [ ] Explain privileged access/PAM
- [ ] Explain how physical and logical access differ
- [ ] Recognize physical access material as supporting ISC2 course knowledge, not a separate current 3.x objective
