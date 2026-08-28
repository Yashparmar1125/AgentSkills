# User Story Authoring & Decomposition Guide

## Purpose
This guide establishes standards for decomposing high-level requirements into atomic, value-driven User Stories.

---

## 1. The INVEST Criteria for User Stories

Every user story authored by the agent must adhere to the **INVEST** quality standard:

| Attribute | Meaning | Verification |
| :--- | :--- | :--- |
| **I - Independent** | Can be developed and delivered without hard dependencies on other in-flight stories. | No circular blocking relationships. |
| **N - Negotiable** | Captures the *what* and *why*, leaving technical implementation details flexible. | Focuses on user outcome. |
| **V - Valuable** | Delivers clear value to a specific user persona or system operator. | Value statement is explicit. |
| **E - Estimable** | Scope and complexity are well understood so effort can be bounded. | Technical tasks are broken down. |
| **S - Small** | Sized to be implemented and tested within a single sprint or iteration. | Less than 3-5 days of effort. |
| **T - Testable** | Accompanied by unambiguous Given-When-Then acceptance criteria. | Verifiable via automated tests. |

---

## 2. Canonical User Story Structure

```markdown
### US-[ID]: [Feature Title]

**As a** [specific user persona / role],
**I want to** [perform a specific action or access a capability],
**So that** [I achieve a specific business benefit or outcome].

#### Context & Assumptions
- [Background context or prerequisites]
- [Key assumptions or constraints]

#### Acceptance Criteria (Given-When-Then)
- [Criteria 1: Happy path]
- [Criteria 2: Validation failure]
- [Criteria 3: Unauthorized access]
- [Criteria 4: System error state]
```

---

## 3. Story Decomposition Patterns

When a client requirement is too broad (an **Epic**), decompose using these proven patterns:

1. **Workflow Steps**: Break down a multi-step wizard into individual step stories (e.g., *Story 1: Batch Details -> Story 2: Student Enrollment -> Story 3: Confirmation*).
2. **Operations (CRUD)**: Separate Create/Read from Update/Delete when logic is complex.
3. **Data Variations**: Story 1 for standard single-item entry, Story 2 for bulk CSV import.
4. **Platform/Persona**: Story 1 for Student examination view, Story 2 for Teacher grading dashboard.
