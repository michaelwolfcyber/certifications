# Domain 3 — Identity and Access Management (IAM) Concepts

**Exam weight: 20%**

## 3.1 Identity Lifecycle Management

Identity lifecycle management controls an identity from creation through removal.

### Roles Definition

Determine what access a person or identity should have based on their role and responsibilities.

### Provisioning

Provisioning creates an account and assigns appropriate access.

### Review

Access should be reviewed to verify that permissions remain appropriate.

### Deprovisioning

Deprovisioning removes or disables access when it is no longer required.

**Lifecycle:**

Define role → Provision → Review → Deprovision

### Frameworks and Tools

IAM frameworks and tools help organizations manage identities, authentication, authorization, and access throughout the lifecycle.

---

## 3.2 Logical Access Controls

Logical access controls protect systems and information through technical mechanisms.

### Principle of Least Privilege

Give users and systems only the access required to perform their authorized tasks.

### Segregation of Duties (SoD)

Separate sensitive responsibilities among different people or roles to reduce the risk of fraud, abuse, or mistakes.

Example:

One person requests a payment while another approves it.

### Access Control Models

#### Discretionary Access Control (DAC)

Access is controlled based on the owner's discretion.

#### Mandatory Access Control (MAC)

Access is determined by centrally enforced security rules, often involving labels or classifications.

#### Role-Based Access Control (RBAC)

Access is assigned based on organizational roles.

Example:

A database administrator receives permissions associated with the DBA role.

---

## Scenario Thinking

When reading a question, ask:

1. Who is requesting access?
2. What resource are they trying to access?
3. Why do they need it?
4. What permissions are actually required?
5. Is the access still necessary?
6. Should another person approve or review the action?

---

## Quick Recall

- Provision = give access
- Review = verify access
- Deprovision = remove access
- Least privilege = minimum necessary access
- SoD = separate sensitive responsibilities
- DAC = owner-controlled
- MAC = centrally enforced
- RBAC = role-based
