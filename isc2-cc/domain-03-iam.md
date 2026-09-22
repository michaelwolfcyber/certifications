# Domain 3 --- Identity and Access Management (IAM) Concepts

**Exam weight: 20%**\
**Current exam outline effective: September 1, 2026**

## 2026 Exam Objectives

### 3.1 Understand identity life cycle management

-   Roles definition
-   Provision
-   Review
-   Deprovision
-   Frameworks and tools

### 3.2 Understand logical access controls

-   Principle of Least Privilege (PoLP)
-   Separation of Duties (SoD)
-   Access control models

------------------------------------------------------------------------

# 3.1 Identity Life Cycle Management

Identity lifecycle management controls an identity from creation through
removal.

## Roles Definition

Determine what access a person or identity should have based on their
role and responsibilities.

## Provisioning

**Provisioning** creates an account and assigns appropriate access.

## Review

Access should be reviewed to verify that permissions remain appropriate.

## Deprovisioning

**Deprovisioning** removes or disables access when it is no longer
required.

### Identity Lifecycle

**Define role → Provision → Review → Deprovision**

### Why the Lifecycle Matters

Access should change as a person's responsibilities change and should be
removed when access is no longer required.

## Frameworks and Tools

IAM frameworks and tools help organizations manage identities and access
throughout the lifecycle.

They can support: - Identity creation - Access assignment - Access
review - Access removal

------------------------------------------------------------------------

# 3.2 Logical Access Controls

Logical access controls protect systems and information through
technical mechanisms.

## Principle of Least Privilege (PoLP)

Give users and systems **only the access required** to perform
authorized tasks.

### Goal

Reduce unnecessary access and limit the potential impact of misuse or
compromise.

**Least privilege = minimum necessary access**

------------------------------------------------------------------------

## Separation of Duties (SoD)

**Separation of Duties** divides sensitive responsibilities among
different people or roles to reduce the risk of fraud, abuse, or
mistakes.

### Example

One person requests a payment while another approves it.

**SoD = don't give one person all the critical steps.**

------------------------------------------------------------------------

# Access Control Models

## Discretionary Access Control (DAC)

Access is controlled according to the owner's discretion.

**DAC = owner-controlled**

## Mandatory Access Control (MAC)

Access is determined by centrally enforced security rules, often using
labels or classifications.

**MAC = centrally enforced**

## Role-Based Access Control (RBAC)

Access is assigned according to organizational roles.

Example:

A database administrator receives permissions associated with the DBA
role.

**RBAC = role-based**

------------------------------------------------------------------------

# Scenario Thinking

When reading an IAM question, ask:

1.  Who is requesting access?
2.  What resource are they trying to access?
3.  Why do they need it?
4.  What permissions are actually required?
5.  Is the access still necessary?
6.  Should another person approve or review the action?
7.  Which access-control model is being described?

------------------------------------------------------------------------

# Quick Recall

  Concept           Remember
  ----------------- -------------------------------------
  Provision         Give/create access
  Review            Verify access remains appropriate
  Deprovision       Remove access
  Least privilege   Minimum necessary access
  SoD               Separate sensitive responsibilities
  DAC               Owner-controlled
  MAC               Centrally enforced
  RBAC              Role-based

# Active Recall

1.  What is identity lifecycle management?
2.  What happens during provisioning?
3.  Why are access reviews necessary?
4.  When should deprovisioning occur?
5.  What is least privilege?
6.  What problem does SoD reduce?
7.  How does DAC differ from MAC?
8.  How does RBAC assign access?
9.  Which model is owner-controlled?
10. Which model is centrally enforced?
11. Which model is based on organizational roles?
