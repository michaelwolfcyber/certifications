# Domain 2 --- Security Governance

**Exam weight: 17.3%**\
**Current exam outline effective: September 1, 2026**

> **Study scope:** These notes follow the current ISC2 CC Domain 2
> structure. The existing ISC2 training remains useful for foundational
> explanations, but the current exam outline determines how the material
> is organized and what topics must be covered.

------------------------------------------------------------------------

## Exam Objectives

### 2.1 Plan Governance, Risk, and Compliance (GRC)

-   Purpose
-   Importance
-   Frameworks and tools

### 2.2 Understand Redundancy

-   Business Continuity (BC)
-   Disaster Recovery (DR)

### 2.3 Understand Security Awareness

-   Organizational culture
    -   Importance of security
    -   Security leadership
-   Concepts
    -   Social engineering
    -   Password protection
    -   Phishing

### 2.4 Measure Cybersecurity Effectiveness

-   Key metrics
-   Key Risk Indicators (KRI)
-   Dashboards
-   Scorecards
-   Reports

------------------------------------------------------------------------

# 2.1 Plan Governance, Risk, and Compliance (GRC)

## Governance, Risk, and Compliance

**GRC** stands for **Governance, Risk, and Compliance**.

  Area             Main Idea
  ---------------- ------------------------------------------
  **Governance**   Direction, accountability, and oversight
  **Risk**         Identifying and managing uncertainty
  **Compliance**   Meeting applicable requirements

### Governance

Governance provides organizational **direction, accountability, and
oversight**.

It helps establish who is responsible for security decisions and how
cybersecurity supports organizational objectives.

### Risk

Risk involves identifying and managing uncertainty that could affect the
organization.

Risk management helps an organization make informed decisions about
which risks need attention and how much risk is acceptable.

### Compliance

Compliance means meeting applicable requirements.

These requirements may come from organizational rules, contracts, laws,
regulations, standards, or other obligations.

------------------------------------------------------------------------

## Purpose of GRC

GRC brings governance, risk management, and compliance together so
cybersecurity activities support:

-   Business objectives
-   Organizational responsibilities
-   Risk management
-   Applicable requirements
-   Security decision-making

### Easy Way to Remember

**Governance** = Who directs and oversees?\
**Risk** = What could go wrong, and how do we manage it?\
**Compliance** = What requirements must we meet?

------------------------------------------------------------------------

## Importance of GRC

Effective GRC helps an organization:

-   Establish accountability
-   Manage risk consistently
-   Support informed security decisions
-   Demonstrate compliance
-   Align cybersecurity with organizational objectives

> **Exam focus:** GRC is not only about compliance. It connects
> organizational direction, risk decisions, and requirements.

------------------------------------------------------------------------

## Frameworks and Tools

Frameworks provide a **structured approach** for managing cybersecurity
and risk.

Tools can help organizations implement, track, measure, and report GRC
activities.

For the CC exam, understand **why organizations use frameworks and
tools** rather than treating GRC as an informal or unstructured process.

------------------------------------------------------------------------

# 2.2 Understand Redundancy

## Redundancy

**Redundancy** means having additional resources or components available
so the failure of one component does not necessarily cause an outage.

### Examples

-   Redundant servers
-   Multiple network paths
-   Backup power
-   Backup systems

### Why Redundancy Matters

Redundancy supports:

-   **Availability**
-   **Resilience**
-   **Business Continuity**
-   **Disaster Recovery**

> **Key idea:** Avoid a single point of failure.

------------------------------------------------------------------------

# Business Continuity (BC)

## Definition

**Business Continuity (BC)** focuses on maintaining or restoring
**critical business functions** when a disruption occurs.

### Purpose

Keep essential business operations functioning during and after a
disruption.

### Importance

Interruptions to critical services can create:

-   Financial consequences
-   Operational consequences
-   Legal consequences
-   Reputational consequences

### Important BC Concepts

The existing ISC2 training provides useful depth around:

-   Critical business functions
-   Recovery priorities
-   Alternate processes
-   Personnel and communications
-   Dependencies
-   Continuity planning

### Business Continuity Plan (BCP)

A **Business Continuity Plan (BCP)** documents how an organization will
maintain or restore critical business operations during a disruption.

Older ISC2 training includes practical BCP concepts such as:

-   BCP team members and contact information
-   Backup team members
-   Immediate response procedures
-   Checklists
-   Notification procedures and call trees
-   Management guidance
-   Procedures for activating the plan
-   Critical supply-chain contacts

These remain useful for understanding **how business continuity works**,
even though the current Domain 2 outline lists BC more broadly under
redundancy.

------------------------------------------------------------------------

# Disaster Recovery (DR)

## Definition

**Disaster Recovery (DR)** focuses on restoring **systems,
infrastructure, and services** following a disaster or major disruption.

### Purpose

Recover technology and services after disruption.

### Importance

Disaster recovery helps:

-   Reduce downtime
-   Restore critical technology
-   Recover essential services
-   Support the organization's return to normal operations

### Important DR Concepts

-   Backups
-   Recovery locations
-   Restoration procedures
-   Recovery priorities
-   Testing

### Disaster Recovery Plan (DRP)

A **Disaster Recovery Plan (DRP)** documents how technology and services
will be restored following a disruption.

Existing ISC2 training includes DRP concepts such as:

-   Executive summary
-   Recovery guidelines
-   Technical recovery guidance
-   Copies for critical DR team members
-   Recovery checklists

------------------------------------------------------------------------

## BC vs. DR

  -----------------------------------------------------------------------
  Business Continuity (BC)            Disaster Recovery (DR)
  ----------------------------------- -----------------------------------
  Keeps **business functions**        Restores **technology and
  operating                           services**

  Focuses on continued operations     Focuses on recovery

  Broader organizational focus        More technology/recovery focused
  -----------------------------------------------------------------------

### Remember

**BC = Keep the business going.**\
**DR = Restore the technology.**

------------------------------------------------------------------------

# 2.3 Understand Security Awareness

## Security Awareness

Security awareness helps people understand their security
responsibilities and recognize common threats.

Security is not only a technical responsibility. People, leadership,
training, and organizational behavior all affect security.

------------------------------------------------------------------------

## Organizational Culture

A strong security culture makes security part of normal organizational
behavior.

The current outline specifically emphasizes:

-   **Importance of security**
-   **Security leadership**

### Importance of Security

Employees should understand:

-   Why information and systems need protection
-   Their individual security responsibilities
-   Why organizational security requirements matter
-   Why suspicious activity should be reported

### Security Leadership

Leadership helps establish security as an organizational priority.

Security leadership can influence:

-   Expectations
-   Accountability
-   Awareness
-   Training
-   Security-conscious behavior

> **Exam idea:** Security culture starts with the organization, not only
> the security team.

------------------------------------------------------------------------

# Common Security Awareness Concepts

## Social Engineering

**Social engineering** uses manipulation or deception to influence a
person into performing an action or revealing information.

Attackers may exploit:

-   Trust
-   Fear
-   Urgency
-   Authority
-   Curiosity

### Key Idea

Social engineering targets **people** rather than relying only on
technical vulnerabilities.

------------------------------------------------------------------------

## Phishing

**Phishing** is a social engineering technique that uses deceptive
communications to trick a person into taking an unsafe action.

Examples may include attempts to make a user:

-   Click a malicious link
-   Open a malicious attachment
-   Reveal credentials
-   Provide sensitive information
-   Perform an unauthorized action

### Remember

**Social engineering** = broad category of manipulating people.\
**Phishing** = a common social engineering technique using deceptive
communications.

------------------------------------------------------------------------

## Password Protection

Security awareness includes protecting passwords and authentication
information.

Important behaviors include:

-   Do not share passwords
-   Protect credentials from disclosure
-   Follow organizational password requirements
-   Report suspected credential compromise

------------------------------------------------------------------------

# 2.4 Measure Cybersecurity Effectiveness

Organizations need measurements to understand whether cybersecurity
activities are working and whether risk is changing.

------------------------------------------------------------------------

## Key Metrics

A **metric** is a measurable value used to track activity, performance,
or effectiveness.

Metrics help organizations:

-   Measure security activity
-   Track performance
-   Identify trends
-   Support decision-making
-   Communicate results

### Easy Way to Remember

**Metric = something measurable.**

------------------------------------------------------------------------

## Key Risk Indicators (KRIs)

A **Key Risk Indicator (KRI)** is a measurement or indicator used to
show changes in an organization's level of risk.

KRIs can help identify when risk is:

-   Increasing
-   Decreasing
-   Approaching an unacceptable level

### Metric vs. KRI

  Metric                             KRI
  ---------------------------------- --------------------------------
  Measures activity or performance   Indicates risk level or change
  Broad measurement                  Specifically risk-focused

**Metric = What are we measuring?**\
**KRI = What is the measurement telling us about risk?**

------------------------------------------------------------------------

## Dashboards

A **dashboard** presents important cybersecurity information in an
easily understood format.

Dashboards can help stakeholders quickly see:

-   Security measurements
-   Trends
-   Risk indicators
-   Current status

### Remember

**Dashboard = quick view.**

------------------------------------------------------------------------

## Scorecards

A **scorecard** organizes measurements to communicate performance
against objectives.

Scorecards help show whether cybersecurity performance is meeting
expected goals or targets.

### Remember

**Scorecard = performance against objectives.**

------------------------------------------------------------------------

## Reports

**Reports** communicate cybersecurity information to stakeholders and
decision-makers.

Reports may communicate:

-   Metrics
-   Risk information
-   Trends
-   Security performance
-   Findings

### Remember

**Report = detailed communication of security information.**

------------------------------------------------------------------------

# Metrics vs. KRIs vs. Dashboards vs. Scorecards vs. Reports

  Concept         Think
  --------------- -----------------------------------
  **Metric**      A measurement
  **KRI**         A risk-focused indicator
  **Dashboard**   Quick visual/current view
  **Scorecard**   Performance against objectives
  **Report**      Communicated security information

------------------------------------------------------------------------

# Current ISC2 AI Guidance for Domain 2

> **Source note:** The following material comes from ISC2's current
> online 2026 CC exam guidance. It expands on the concise Domain 2
> bullets in the PDF exam outline.

ISC2's current guidance integrates foundational AI security concepts
across the CC domains.

For **Domain 2**, know these high-level ideas:

-   AI can make social engineering and phishing attacks more convincing
    or scalable.
-   Security awareness training should account for AI-assisted threats.
-   AI-driven tools can assist with early identification and reporting
    of security incidents.
-   Continuity and recovery planning may need to protect the
    configurations and datasets that power AI services.
-   **Model drift** can create a BC/DR risk if declining AI performance
    affects critical operations.
-   Organizations may track **AI-specific KRIs** through dashboards and
    reports.

### Model Drift

**Model drift** refers to declining or changing AI model performance as
real-world conditions or data change.

For CC purposes, connect it to **continuity and resilience**: if an
organization depends on an AI service and its performance degrades,
critical operations may be affected.

> Keep this at a foundational level. CC is an entry-level certification.

------------------------------------------------------------------------

# What Moved Out of Domain 2?

## Incident Response

The previous CC structure placed Incident Response with Business
Continuity and Disaster Recovery.

The September 2026 refresh moved Incident Response into:

**Domain 5 --- Security Operations and Incident Response**

So your older ISC2 Incident Response material is **still useful**, but
study it with **Domain 5**, not Domain 2.

The current Domain 5 specifically includes:

-   Implementing an Incident Response Plan (IRP)
-   Incident Response exercises
    -   Testing
    -   Tabletop exercises

> **Do not delete your old IR notes. Move/reuse them when we build
> Domain 5.**

------------------------------------------------------------------------

# Domain 2 Quick Recall

  -----------------------------------------------------------------------
  Term                                Remember
  ----------------------------------- -----------------------------------
  **GRC**                             Governance, Risk, Compliance

  **Governance**                      Direction, accountability,
                                      oversight

  **Risk**                            Managing uncertainty

  **Compliance**                      Meeting requirements

  **Redundancy**                      Extra resources/components to avoid
                                      a single failure causing an outage

  **BC**                              Keep critical business functions
                                      operating

  **DR**                              Restore systems and services

  **Security awareness**              People understand responsibilities
                                      and threats

  **Social engineering**              Manipulating people

  **Phishing**                        Deceptive communication used to
                                      trick people

  **Metric**                          Measurement

  **KRI**                             Risk-focused indicator

  **Dashboard**                       Quick view of security information

  **Scorecard**                       Performance against objectives

  **Report**                          Security information communicated
                                      to stakeholders
  -----------------------------------------------------------------------

------------------------------------------------------------------------

# Active Recall

Answer these without looking at the notes:

1.  What does GRC stand for?
2.  What is the purpose of governance?
3.  How is compliance different from risk management?
4.  Why do organizations use GRC frameworks and tools?
5.  What is redundancy?
6.  How does redundancy support availability?
7.  What is the main purpose of Business Continuity?
8.  What is the main purpose of Disaster Recovery?
9.  What is the easiest way to distinguish BC from DR?
10. What is a BCP?
11. What is a DRP?
12. Why does organizational culture matter to cybersecurity?
13. What role does security leadership play?
14. What is social engineering?
15. How is phishing related to social engineering?
16. Why is password protection part of security awareness?
17. What is a cybersecurity metric?
18. What is a KRI?
19. How is a KRI different from a general metric?
20. What is the purpose of a dashboard?
21. What is the purpose of a scorecard?
22. What is the purpose of a report?
23. What is model drift, at a high level?
24. Why could model drift become a continuity risk?
25. Which domain now contains Incident Response?

------------------------------------------------------------------------

# Final Exam Checklist

Before considering Domain 2 complete, make sure you can explain:

-   [ ] GRC and its purpose
-   [ ] Why GRC is important
-   [ ] Why organizations use GRC frameworks and tools
-   [ ] Redundancy
-   [ ] Business Continuity
-   [ ] Disaster Recovery
-   [ ] BC vs. DR
-   [ ] Organizational security culture
-   [ ] Importance of security
-   [ ] Security leadership
-   [ ] Social engineering
-   [ ] Password protection
-   [ ] Phishing
-   [ ] Key metrics
-   [ ] Key Risk Indicators
-   [ ] Dashboards
-   [ ] Scorecards
-   [ ] Reports
-   [ ] Foundational AI considerations ISC2 associates with Domain 2
-   [ ] Why Incident Response belongs with Domain 5 in the refreshed
    outline

------------------------------------------------------------------------

## Source Basis

This study guide was rebuilt from:

1.  **ISC2 CC Certification Exam Outline --- effective September 1,
    2026** (authoritative scope and organization)
2.  **ISC2 CC Domain Refresh --- effective September 1, 2026**
    (old-to-new mapping)
3.  **Existing ISC2 CC training material** (foundational BC/DR
    explanations and planning concepts)
4.  **Your existing Domain 2 notes** (concise definitions and study
    structure)
5.  **ISC2's current online 2026 CC guidance** (AI-security integration)

The exam outline controls the organization of these notes. Existing
training material is retained where it helps explain current objectives
rather than being discarded simply because the domain structure changed.


---

# Audit Note

The 2026 exam outline is the controlling scope for Domain 2. The AI section is included because ISC2's current 2026 online guidance explicitly explains how foundational AI concepts are integrated into Domain 2.
