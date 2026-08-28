# Requirement Analysis & Discovery Guide

## Purpose
This guide defines the methodology for analyzing incoming client requests, legacy tickets, and feature descriptions before translating them into technical designs.

---

## 1. The 5 Dimensions of Requirement Discovery

When a client or stakeholder presents a requirement (e.g., *"We need bulk student enrollment with CSV validation"*), analyze across 5 essential dimensions:

```text
                     ┌── Business Objective (Why are we building this?)
                     ├── User Persona & Roles (Who needs this and what permissions apply?)
Requirement Discovery ┼── Functional Workflows (What exact happy & alternate paths exist?)
                     ├── Constraints & NFRs (Performance, security, regulatory, offline)
                     └── Out-of-Scope Boundaries (What are we explicitly NOT doing now?)
```

### 1.1 Business Objective
- What friction, inefficiency, or missing capability does this resolve?
- What is the definition of success from the business perspective?
- How does this feature impact existing workflows?

### 1.2 User Personas & RBAC Isolation
- **Primary Actor**: Who initiates the action (e.g., Admin, Teacher, Student)?
- **Secondary Actors**: Who consumes the downstream output (e.g., Reports, Notifications)?
- **Permissions**: What role checks must be enforced at the API route and UI levels?
- **Data Boundaries**: Can Actor A view Actor B's data? (IDOR / BOLA vulnerability prevention).

### 1.3 Functional Workflows & State Progression
- **Entry Point**: Where in the UI/API does the workflow start?
- **Inputs**: What fields are required, optional, formatted, or calculated?
- **Processing**: Synchronous response vs. background queue task?
- **Exit State**: What feedback (toast, modal, redirect, email) is delivered upon success or error?

### 1.4 Non-Functional Requirements (NFRs)
- **Latency & Concurrency**: Expected request volume and max allowable response time.
- **Data Volume**: How many records per batch or pagination page?
- **Integrity**: Database transaction atomicity (ACID rollbacks on partial failures).
- **Compliance**: DPDP / GDPR / CERT-In data handling requirements.

### 1.5 Out-of-Scope Boundaries
- Define what will **NOT** be included in this milestone to prevent scope creep.
- Example: *"CSV upload supports up to 1,000 records; automated SFTP sync is deferred to Phase 2."*

---

## 2. Requirement Clarification Protocol

When a requirement is ambiguous or underspecified:
1. **Never guess critical business rules** (e.g., pass/fail cutoffs, billing logic, permission bypasses).
2. **Make reasonable engineering assumptions** for standard technical patterns (e.g., loading spinners, standard pagination limits, input trimming) and document them explicitly.
3. **Group questions efficiently** in the implementation plan rather than asking repetitive, fragmented questions.
