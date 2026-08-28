---
name: indian-compliance-security
description: >-
  Production-grade security and compliance engineering process for software applications
  developed, deployed, or operated in India (DPDP Act, CERT-In, OWASP ASVS, RBI, UIDAI, SEBI).
  Use when asked to perform an Indian regulatory compliance review, security gap analysis,
  data inventory and flow mapping, privacy audit, or establish production security gates for Indian software.
license: MIT
---

# Skill: Indian Software Security & Compliance Engineering

## Purpose

This skill defines a production-grade security and compliance process for software applications developed, deployed, or operated in India.

The objective is NOT to blindly apply every security standard.

The objective is to:

1. Understand the existing application and architecture.
2. Identify the application's data, users, workflows, integrations, and infrastructure.
3. Determine which Indian laws, regulations, standards, and security practices actually apply.
4. Perform a security and compliance gap analysis.
5. Prioritize risks.
6. Create an implementation plan.
7. Implement applicable controls without unnecessarily damaging the existing architecture.
8. Validate that controls actually work.
9. Produce auditable documentation and evidence.
10. Establish a repeatable production-release security gate.

This skill must be applied to the EXISTING codebase rather than assuming a greenfield application.

---

# 1. Core Principle

NEVER start by modifying code.

The required sequence is:

DISCOVER
    ↓
UNDERSTAND
    ↓
CLASSIFY
    ↓
MAP REQUIREMENTS
    ↓
AUDIT
    ↓
IDENTIFY GAPS
    ↓
RISK RANK
    ↓
PLAN
    ↓
IMPLEMENT
    ↓
TEST
    ↓
VERIFY
    ↓
DOCUMENT
    ↓
PRODUCTION SECURITY GATE

Do not skip the discovery and assessment phases.

Do not assume that a requirement applies merely because the software is deployed in India.

Do not claim that the software is "compliant" unless there is sufficient evidence.

Use terminology such as:

- Implemented
- Partially implemented
- Not implemented
- Not applicable
- Requires legal confirmation
- Requires external audit
- Requires organizational process

when appropriate.

---

# 2. First Phase — Repository Discovery

Before making changes, inspect the complete repository.

Understand:

## Application structure

Identify:

- Frontend
- Backend
- Mobile applications
- APIs
- Workers
- Cron jobs
- Admin applications
- Internal tools
- Microservices
- Shared libraries
- Authentication services
- Payment services
- File storage
- Notification systems
- AI/ML components
- Third-party integrations

## Technology stack

Identify:

- Programming languages
- Frameworks
- Databases
- Caches
- Message queues
- Cloud provider
- Containerization
- CI/CD
- Reverse proxies
- Monitoring
- Logging
- Authentication providers
- Payment providers
- External APIs

## Infrastructure

Identify:

- Production environments
- Staging environments
- Development environments
- Domains
- DNS
- TLS
- Load balancers
- WAF
- Firewalls
- Security groups
- VPC/network structure
- Public/private services
- Database exposure
- Object storage
- Secrets management
- Backups
- Disaster recovery

Do NOT modify anything during this phase.

---

# 3. Application Data Inventory

Determine exactly what data the system processes.

Create a data inventory.

Classify data into categories such as:

### Public

Examples:

- Public event information
- Public documentation
- Public product information

### Internal

Examples:

- Internal operational information
- Non-public configuration

### Personal Data

Examples:

- Name
- Email
- Phone number
- Address
- User identifiers
- Account information
- Device information
- IP address
- Location information
- Education information

### Sensitive / High-Risk Data

Depending on the product:

- Financial information
- Authentication credentials
- Government identifiers
- Health-related information
- Biometric information
- Children's data
- Payment information
- Highly confidential business information

Do not automatically label every piece of information as sensitive.

Determine classification based on actual data and applicable law.

---

# 4. Data Flow Mapping

For every important data category, determine:

WHERE is it collected?
        ↓
WHY is it collected?
        ↓
WHERE is it processed?
        ↓
WHERE is it stored?
        ↓
WHO can access it?
        ↓
WHO is it shared with?
        ↓
HOW LONG is it retained?
        ↓
HOW is it deleted?

Create a data-flow map covering:

- Client
- API
- Backend
- Database
- Cache
- Object storage
- Logs
- Analytics
- Third-party services
- Backups

Pay special attention to personal data appearing unexpectedly in:

- Logs
- Error messages
- Analytics
- Debug output
- Database backups
- Third-party APIs

---

# 5. Determine Regulatory Applicability

Do NOT assume every law or standard applies.

Create an applicability matrix.

Example:

| Requirement | Applicable? | Reason | Evidence |
|---|---|---|---|
| DPDP Act | Yes/No/Review | Personal data processing | Data inventory |
| CERT-In requirements | Yes/No/Review | Entity/system characteristics | Infrastructure |
| OWASP ASVS | Recommended | Application security | Security audit |
| OWASP Top 10 | Recommended | Web application | Application audit |
| ISO 27001 | Optional/Customer requirement | ISMS | Organization |
| SOC 2 | Optional/Customer requirement | Enterprise SaaS | Customer requirements |
| PCI DSS | Yes/No | Cardholder data handling | Payment architecture |
| RBI | Yes/No | Financial/payment activity | Business model |
| SEBI | Yes/No | Securities-related activity | Business model |
| IRDAI | Yes/No | Insurance activity | Business model |
| UIDAI | Yes/No | Aadhaar-related processing | Integration |
| GDPR | Yes/No | EU personal data | User geography |

The agent must explicitly distinguish:

1. Legal requirement
2. Regulatory requirement
3. Contractual/customer requirement
4. Security best practice
5. Optional certification

Never represent an optional standard as mandatory law.

---

# 6. DPDP-Oriented Engineering Review

Where the DPDP framework applies, inspect the application for technical mechanisms supporting applicable obligations.

Review:

## Data collection

Determine:

- What personal data is collected?
- Is every field necessary?
- Are unnecessary fields being collected?

## Notice/transparency

Check whether the application provides appropriate information to users about personal-data processing.

## Consent / lawful basis mechanisms

Where applicable, determine whether the architecture can:

- Record user choices
- Store consent state
- Record timestamps
- Record relevant version information
- Withdraw consent
- Respect changed choices

Do NOT implement fake consent mechanisms merely to pass a checklist.

## Data access

Determine:

- Who can access personal data?
- Are roles enforced server-side?
- Can users access another user's data?
- Can administrators access more data than necessary?

## Data deletion

Verify whether the system can appropriately:

- Delete personal data
- Anonymize data
- Remove associated records
- Handle dependent records
- Handle files
- Handle caches
- Handle search indexes
- Handle applicable backups according to the organization's retention policy

## Data retention

Identify:

- Data retention periods
- Unnecessary indefinite retention
- Old accounts
- Old logs
- Old exports
- Old files

## Data breach handling

Determine whether the organization has:

- Incident detection
- Incident classification
- Escalation
- Evidence preservation
- Notification procedures where required

Do not claim legal compliance solely because a privacy policy exists.

---

# 7. OWASP Security Assessment

Use OWASP principles as the application-security baseline.

Review at minimum:

## Authentication

Check:

- Password hashing
- Password policy
- MFA where appropriate
- Login protection
- Brute-force protection
- Credential stuffing protection
- Session management
- Token expiration
- Refresh token security
- Password reset
- Email verification
- Account recovery
- Logout
- Concurrent sessions

## Authorization

Test:

- RBAC
- Resource ownership
- Admin permissions
- Faculty permissions
- Student permissions
- Organization-level isolation
- Tenant isolation

Pay particular attention to:

BOLA / IDOR vulnerabilities.

Example:

```text
GET /api/users/123
```

must not automatically mean:

```text
Any authenticated user
        ↓
Can access user 123
```

Authorization must be based on the requesting user's permissions.

## Input security

Review:

- SQL injection
- NoSQL injection
- Command injection
- XSS
- SSRF
- Path traversal
- Template injection
- Prototype pollution
- Malicious file uploads

## API security

Check:

- Authentication
- Authorization
- Rate limiting
- Request validation
- Response filtering
- Pagination
- Resource limits
- Error handling
- API versioning
- Sensitive endpoints

## File uploads

Check:

- File type validation
- MIME validation
- Extension validation
- File size limits
- Filename sanitization
- Storage isolation
- Malware scanning where appropriate
- Execution prevention
- Access control

## Security headers

Review appropriate:

- Content-Security-Policy
- Strict-Transport-Security
- X-Content-Type-Options
- Referrer-Policy
- Permissions-Policy
- Frame protection

Do not blindly add headers without checking application compatibility.

---

# 8. Secrets Management

Search the repository for:

- API keys
- Passwords
- Database credentials
- JWT secrets
- Private keys
- Cloud credentials
- OAuth secrets
- Payment secrets
- Firebase credentials
- Third-party credentials

Check:

- Source code
- .env files
- Git history
- Dockerfiles
- Docker Compose
- CI/CD configuration
- Logs
- Documentation

If a secret is discovered:

1. Do not expose it in output.
2. Determine whether it is active.
3. Recommend rotation.
4. Remove it from source control.
5. Move it to appropriate secret management.
6. Check Git history if necessary.
7. Review access logs where applicable.

Never print discovered secrets.

---

# 9. Database Security

Review:

- Database exposure
- Authentication
- Authorization
- Encryption
- Connection security
- Least privilege
- Application DB user permissions
- Migration strategy
- Backup strategy
- Backup encryption
- Database logging
- Sensitive data storage
- Indexes
- Query safety

Verify that production databases are NOT unnecessarily exposed to the public internet.

---

# 10. Infrastructure Security

Inspect:

## Network

- Public ports
- Private services
- Security groups
- Firewalls
- VPC
- Internal communication
- Database exposure
- Redis exposure
- SSH exposure

## Containers

Check:

- Root containers
- Privileged containers
- Host mounts
- Secret exposure
- Image vulnerabilities
- Outdated base images
- Unnecessary packages
- Container networking

## Cloud IAM

Check:

- Root account usage
- IAM roles
- Access keys
- Least privilege
- Service permissions
- Unused credentials
- Production access

## TLS

Verify:

- HTTPS
- Certificate validity
- HTTP → HTTPS redirect
- Secure TLS configuration
- Secure cookies

---

# 11. Logging and Monitoring

Review whether security-relevant events are logged.

Examples:

- Login
- Failed login
- Logout
- Password reset
- Permission changes
- Role changes
- Admin actions
- Data exports
- Account deletion
- Payment events
- Security events
- Configuration changes

Logs must NOT unnecessarily contain:

- Passwords
- Tokens
- API keys
- Full payment-card data
- Sensitive personal information

Check:

- Log integrity
- Access controls
- Retention
- Time synchronization
- Centralized logging
- Alerting

---

# 12. CERT-In-Oriented Review

Where applicable, assess the system and organization against relevant CERT-In requirements.

Review:

- Cybersecurity incident detection
- Incident response
- Incident reporting process
- Log retention requirements
- Time synchronization
- Point-of-contact responsibilities
- Security monitoring
- Evidence preservation

Do not invent deadlines, retention periods, or reporting requirements.

When exact legal/regulatory requirements matter:

1. Verify against the current official CERT-In material.
2. Record the source.
3. Record the date/version.
4. Flag requirements requiring legal/compliance confirmation.

---

# 13. Secure SDLC

The project must implement security throughout development.

Recommended pipeline:

```text
Developer
    ↓
Pre-commit checks
    ↓
Code Review
    ↓
SAST
    ↓
Dependency Scan
    ↓
Secret Scan
    ↓
Build
    ↓
Container Scan
    ↓
Integration Tests
    ↓
DAST
    ↓
Security Tests
    ↓
Deployment
    ↓
Monitoring
```

Security checks should fail the pipeline for clearly defined critical issues.

Do not make every informational warning block deployment.

Define severity thresholds.

---

# 14. Dependency Security

Inspect:

- npm
- pip
- Maven/Gradle
- Flutter packages
- Docker images
- OS packages
- GitHub Actions
- Third-party SDKs

Identify:

- Critical vulnerabilities
- High vulnerabilities
- Unsupported dependencies
- Deprecated packages
- Unmaintained packages
- Known vulnerable versions

Before upgrading a dependency:

1. Check compatibility.
2. Check breaking changes.
3. Run tests.
4. Review application behavior.

Never blindly run a massive dependency upgrade in production code.

---

# 15. Security Testing

Security testing must include:

## Static

- SAST
- Secret scanning
- Dependency scanning

## Dynamic

- DAST
- API testing

## Manual

- Authentication testing
- Authorization testing
- BOLA/IDOR testing
- Business logic testing
- Session testing
- File upload testing
- Rate-limit testing
- Privilege escalation testing

## Infrastructure

- Port exposure
- TLS configuration
- Container security
- Cloud configuration

For high-risk applications, recommend independent VAPT/penetration testing.

---

# 16. Test Cases

Security controls must have tests.

Examples:

### Authorization

```text
Student A requests Student B's data
→ Must be rejected
```

### Admin privilege

```text
Normal user requests admin endpoint
→ Must be rejected
```

### Rate limiting

```text
Repeated login attempts
→ Rate limit / protection triggered
```

### Password reset

```text
Expired reset token
→ Must be rejected
```

### Token

```text
Expired JWT
→ Must be rejected
```

### File upload

```text
Executable disguised as image
→ Must be rejected
```

### Tenant isolation

```text
Tenant A requests Tenant B resource
→ Must be rejected
```

### Injection

```text
Malicious input
→ Must not execute as SQL/command/script
```

---

# 17. Payment Security

If payments are involved:

Determine:

- Who collects payment?
- Does the application process card data?
- Is a payment gateway used?
- Does the application store payment credentials?
- Are webhooks authenticated?
- Are webhook signatures verified?
- Are payment states validated server-side?
- Can payment status be manipulated from the client?

Never trust:

```text
Frontend:
paymentSuccessful = true
```

The backend must independently verify payment status.

Prefer payment architectures that minimize the application's exposure to cardholder data.

Determine whether PCI DSS or other payment requirements apply.

---

# 18. Third-Party Integration Security

For every external service:

Create:

| Service | Data Sent | Purpose | Credentials | Risk |
| ------- | --------- | ------- | ----------- | ---- |

Examples:

- AWS
- Firebase
- Razorpay
- Google
- Microsoft
- Sentry
- Analytics
- Email providers
- SMS providers
- AI APIs

Review:

- API authentication
- Data minimization
- Data exposure
- Secrets
- Webhook security
- Vendor access
- Retention
- Failure behavior

---

# 19. Backup and Disaster Recovery

Verify:

- Automated backups
- Backup frequency
- Encryption
- Access control
- Off-site/independent backup where appropriate
- Backup retention
- Restoration procedure
- Restoration testing

Define:

RPO and RTO based on business requirements.

A backup strategy is incomplete until restoration has been tested.

---

# 20. Incident Response

The project/organization should have a documented process:

```text
Detect
  ↓
Classify
  ↓
Contain
  ↓
Investigate
  ↓
Preserve Evidence
  ↓
Notify Appropriate Parties
  ↓
Recover
  ↓
Root Cause Analysis
  ↓
Prevent Recurrence
```

Define:

- Who is responsible?
- Who can declare an incident?
- Who has production access?
- Who contacts infrastructure providers?
- Who handles customers?
- Who handles regulators?
- Who preserves evidence?

Do not invent organizational roles. Identify missing ownership.

---

# 21. Risk Scoring

Every finding should receive:

### Severity

- Critical
- High
- Medium
- Low
- Informational

### Impact

Consider:

- Confidentiality
- Integrity
- Availability
- Privacy
- Financial impact
- Regulatory impact
- Reputation

### Likelihood

Consider:

- Exploitability
- Exposure
- Attacker access
- Existing controls

Prioritize findings based on actual risk rather than the number of findings.

---

# 22. Compliance Gap Report

Generate a report containing:

## Executive Summary

Overall security posture.

## Application Overview

Architecture and technology stack.

## Data Classification

What data is processed.

## Regulatory Applicability

Applicable and non-applicable requirements.

## Security Findings

| ID | Finding | Severity | Risk | Status |
| -- | ------- | -------- | ---- | ------ |

## Compliance Findings

| Requirement | Status | Evidence | Gap | Action |
| ----------- | ------ | -------- | --- | ------ |

## Recommended Remediation

Prioritized by:

P0 — Production blocker

P1 — Critical before broad rollout

P2 — Important

P3 — Improvement

---

# 23. Production Security Gate

Before production release, verify:

## Code

- [ ] No critical security vulnerabilities
- [ ] No exposed secrets
- [ ] Dependency vulnerabilities reviewed
- [ ] Security tests passing
- [ ] Code review completed

## Authentication

- [ ] Secure password storage
- [ ] Authentication protected
- [ ] Session/token security verified
- [ ] Password reset secure

## Authorization

- [ ] RBAC tested
- [ ] BOLA/IDOR tested
- [ ] Privilege escalation tested
- [ ] Tenant isolation tested where applicable

## API

- [ ] Validation implemented
- [ ] Rate limiting implemented
- [ ] Sensitive responses reviewed
- [ ] Error responses sanitized

## Infrastructure

- [ ] HTTPS
- [ ] Database private
- [ ] Firewall configured
- [ ] IAM reviewed
- [ ] Secrets secured
- [ ] Containers reviewed

## Data

- [ ] Data inventory completed
- [ ] Retention defined
- [ ] Deletion process defined
- [ ] Privacy requirements reviewed
- [ ] Third-party data flows reviewed

## Operations

- [ ] Logging
- [ ] Monitoring
- [ ] Alerting
- [ ] Backup
- [ ] Restore test
- [ ] Incident response

## Compliance

- [ ] Applicability matrix completed
- [ ] Legal review obtained where necessary
- [ ] Regulatory requirements identified
- [ ] Required external audit completed where applicable

---

# 24. Definition of Done

A security/compliance task is NOT complete merely because code was changed.

It is complete only when:

1. Requirement is identified.
2. Applicability is established.
3. Existing implementation is understood.
4. Gap is identified.
5. Risk is assessed.
6. Implementation is completed.
7. Tests are added.
8. Tests pass.
9. Security behavior is verified.
10. Documentation is updated.
11. Evidence is recorded.

---

# 25. Evidence Collection

For each important control, record evidence.

Examples:

```text
Control:
Database must not be publicly accessible.

Evidence:
AWS security group configuration
+
Network architecture
+
Connectivity test
```

Another example:

```text
Control:
Unauthorized user cannot access another user's record.

Evidence:
Authorization integration test
+
API test result
```

Evidence should allow another engineer or auditor to understand WHY the control is considered implemented.

---

# 26. Architecture Preservation Rule

Do not rewrite working architecture simply to make the code appear more compliant.

Prefer:

- Minimal changes
- Incremental hardening
- Reusable security middleware
- Centralized policies
- Existing infrastructure improvements
- Automated controls

Before introducing a new security service, determine whether existing infrastructure can provide the requirement.

Avoid unnecessary:

- Framework migrations
- Database migrations
- Authentication rewrites
- Cloud migrations
- Service splitting

unless the existing architecture creates a material security or compliance risk.

---

# 27. Code Quality Requirements

Security implementation must maintain code quality.

Avoid:

- Duplicated authorization logic
- Hardcoded roles everywhere
- Security checks scattered across controllers
- Giant middleware files
- Giant authentication services
- Giant configuration files
- Duplicate validation
- Temporary security bypasses
- TODO-based security controls

Prefer reusable abstractions such as:

```text
auth/
authorization/
security/
validation/
audit/
rate-limit/
crypto/
```

depending on the existing architecture.

Follow the project's existing architectural conventions unless there is a strong security reason to change them.

---

# 28. Do Not Overclaim Compliance

Never say:

"Application is fully DPDP compliant."

unless the required legal, organizational, technical and operational assessment has actually been completed.

Instead say:

"Technical controls identified for the applicable DPDP requirements have been implemented, subject to legal/compliance validation."

Similarly:

"OWASP ASVS controls assessed: 87% implemented."

is preferable to:

"OWASP compliant."

When certification or independent audit is required, explicitly state that code-level implementation cannot substitute for certification/audit.

---

# 29. Current-Law Verification

Security and compliance requirements can change.

When determining legal or regulatory requirements:

- Prefer official Indian government sources.
- Prefer official regulator sources.
- Verify current versions.
- Record source/date.
- Do not rely solely on blogs.
- Do not assume old compliance guidance remains current.

For example, verify against appropriate official sources such as:

- CERT-In
- MeitY
- Government of India
- RBI
- SEBI
- IRDAI
- UIDAI
- Other applicable regulators

If the requirement is ambiguous, flag it for legal/compliance review instead of guessing.

---

# 30. Final Output Required

After assessment, produce:

## A. Architecture Summary

What exists today.

## B. Data Inventory

What data the application processes.

## C. Regulatory Applicability Matrix

What applies and why.

## D. Security Assessment

Current security posture.

## E. Findings

Prioritized vulnerabilities and gaps.

## F. Remediation Plan

Exact changes required.

## G. Implementation

Implement approved technical changes.

## H. Security Tests

Tests proving controls work.

## I. Compliance Evidence

Evidence for implemented controls.

## J. Production Gate

Final PASS / CONDITIONAL PASS / BLOCKED decision.

---

# 31. Operating Philosophy

Think like:

- Security Engineer
- Application Security Engineer
- Cloud Security Engineer
- Privacy Engineer
- DevSecOps Engineer
- Compliance Engineer

but do not pretend to be legal counsel.

The objective is not:

"Add security features."

The objective is:

"Build an application whose security controls, privacy controls, infrastructure controls, operational procedures, and compliance requirements are systematically identified, implemented, tested, monitored, and auditable."

Always prioritize:

SECURITY
+
PRIVACY
+
RELIABILITY
+
AUDITABILITY
+
MAINTAINABILITY

over superficial checklist completion.

---

# 32. Mandatory First Action

When this skill is invoked on an existing repository:

DO NOT immediately modify code.

First perform a complete discovery and assessment.

Return:

1. Repository structure
2. Architecture
3. Data flows
4. Authentication model
5. Authorization model
6. Infrastructure
7. Third-party integrations
8. Data categories
9. Applicable regulations/standards
10. Current security controls
11. Security gaps
12. Compliance gaps
13. Risk ranking
14. Proposed remediation plan

Only after this assessment should implementation begin.

The agent must ask for clarification ONLY when a missing business/legal requirement materially affects the assessment.

Otherwise, make reasonable engineering assumptions, clearly document them, and continue.

The final objective is a production-ready security and compliance posture, not merely a collection of security-related code changes.
