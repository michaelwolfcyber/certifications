# Domain 5 — Security Operations and Incident Response

**Exam weight: 17.3%**

## 5.1 Data Security

### Data Handling

Know the purpose of:
- Classification
- Labeling
- Masking
- Sanitization

### Classification

Classify information according to its sensitivity and required protection.

### Labeling

Labels communicate the classification or handling requirements of information.

### Masking

Masking obscures part or all of sensitive information.

### Sanitization

Sanitization removes or destroys data so it cannot be recovered through normal means.

---

## 5.2 Cryptography

### Symmetric Encryption

Uses the same key for encryption and decryption.

**Strength:** Efficient for large amounts of data.

**Challenge:** Secure key distribution.

### Asymmetric Encryption

Uses a key pair:
- Public key
- Private key

### Hashing

A hash function produces a fixed-length value from data.

Hashing is commonly used for integrity verification and password-related security mechanisms.

**Important:** Hashing is not the same as encryption.

### Quantum-Resistant Cryptography

Quantum-resistant cryptography is designed to remain secure against attacks from sufficiently capable quantum computers.

---

## 5.3 Security Operations

### Logging and Monitoring

Security logs provide records of system and security activity.

Monitoring helps identify unusual or suspicious behavior.

### Security Event Triage

Triage involves evaluating security events and determining their priority and significance.

Important concepts:
- Incident use cases
- Prioritization
- Correlation

### Threat Actors

Threat actors are individuals or groups that may intentionally or unintentionally create security threats.

Understand that threat actors can have different:
- Types
- Capabilities
- Resources
- Motivations

### Cyber Threat Intelligence (CTI)

CTI is information about threats that can help organizations understand, detect, and respond to adversary activity.

### Threat Frameworks

Threat frameworks provide structured ways to describe, categorize, or analyze adversary behavior and security threats.

---

## 5.4 Incident Response

### Incident Response Plan (IRP)

An IRP provides an organized approach for responding to security incidents.

Know the purpose and major components of an incident response process.

### Incident Response Exercises

Organizations can test their response capabilities through exercises such as:
- Tabletop exercises
- Testing
- Simulated scenarios

Exercises help identify weaknesses before a real incident occurs.

---

## 5.5 Asset Protection

### Asset Lifecycle Management

Assets move through a lifecycle that can include:
- Acquisition
- Deployment
- Maintenance
- Retirement
- Disposal

### End of Life (EOL)

End-of-life software or devices may no longer receive vendor support or security updates.

### Configuration Management

Configuration management helps maintain systems in known, controlled states.

### Baselines

A baseline represents an approved configuration against which changes can be compared.

### Updates and Patches

Updates and patches can address vulnerabilities, bugs, and other issues.

### Change Management

Changes should be controlled and documented.

Typical concepts:
- Documentation
- Approval
- Testing
- Implementation
- Rollback

---

## 5.6 Security Testing

### Security Readiness Testing

Know the general roles of:

- **Blue team:** Defensive security
- **Red team:** Simulated adversary/offensive security
- **Purple team:** Collaboration between offensive and defensive teams

### Vulnerability Scanning

Automated or systematic identification of potential vulnerabilities.

### Static Analysis

Analyzes software without executing it.

### Dynamic Analysis

Analyzes software while it is executing.

### Threat Modeling

Identifies potential threats and attack paths so security controls can be considered during design.

### Physical Penetration Testing

Can test physical security through activities such as:
- Phishing
- Tailgating
- Impersonation

---

## Quick Recall

- Classification = determine sensitivity
- Labeling = communicate handling category
- Masking = obscure data
- Sanitization = remove/destroy recoverable data
- Symmetric = same key
- Asymmetric = key pair
- Hashing = one-way transformation used for integrity/security purposes
- Triage = evaluate and prioritize events
- CTI = information about threats
- IRP = organized incident response plan
- EOL = end of vendor/product lifecycle
- Baseline = approved configuration
- Blue = defense
- Red = adversary simulation
- Purple = collaboration
- Static = analyze without running
- Dynamic = analyze while running
