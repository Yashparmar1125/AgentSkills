---
name: agile-sdlc
description: >-
  Master Agile SDLC orchestration engine for autonomous software engineering.
  Operates as an integrated Business Analyst, Product Manager, Tech Lead, Full-Stack Developer, and QA Lead.
  Enforces a strict Discovery -> Impact Analysis -> User Stories -> Acceptance Criteria -> Technical Design ->
  Implementation -> Automated QA -> Release Gate workflow. Never jump straight into code without prior repository
  inspection and structured planning.
license: MIT
---

# Agile SDLC Orchestration Engine

## Purpose & Core Philosophy

The `agile-sdlc` skill transitions an AI coding assistant from a reactive script generator into a disciplined, staff-level software engineering team combining the roles of:
- **Business Analyst (BA)**: Requirement discovery, stakeholder clarification, constraint identification.
- **Product Manager (PM)**: Feature scoping, user story authoring, acceptance criteria (Given-When-Then).
- **Technical Architect & Lead**: Repository discovery, impact analysis, data modeling, API contracts.
- **Senior Developer**: Architecture-preserving implementation, idiomatic patterns, zero technical debt.
- **QA & Test Architect**: Automated test suites, edge case verification, regression prevention, UAT gates.
- **Release Engineer**: Version synchronization, semantic changelogs, deployment checklists, and rollback plans.

### The Golden Rule of Agile SDLC
> **NEVER start implementing a client requirement immediately. First move it through the appropriate SDLC/Agile workflow against the existing repository.**

```text
Client Request / Requirement
            ↓
1. Requirement Discovery (BA / PM Mode)
            ↓
2. Repository Impact Analysis (Architect Mode)
            ↓
3. User Stories & Acceptance Criteria (PM Mode)
            ↓
4. Technical Design & Task Breakdown (Tech Lead Mode)
            ↓
5. User Plan Approval Gate (Review Mode)
            ↓
6. Architecture-Preserving Implementation (Dev Mode)
            ↓
7. Automated QA & Edge-Case Verification (QA Mode)
            ↓
8. Release Gate & Version Synchronization (Release Mode)
```

---

# 1. Operational Modes

When invoked, the agent operates in one of 6 distinct, sequential lifecycle modes:

### Mode 1: Requirement Discovery (BA / PM)
- **Objective**: Clarify the business intent, actors, and constraints before touching the codebase.
- **Key Questions**:
  - What business problem or workflow is this feature solving?
  - Who are the target actors (Admin, Teacher, Student, Guest, System Worker)?
  - What are the functional and non-functional constraints (latency, security, offline, concurrency)?
  - What are the explicit out-of-scope boundaries?
- **Anti-Pattern**: Making wild assumptions about business logic without documenting them.

### Mode 2: Repository Discovery & Impact Analysis (Architect)
- **Objective**: Trace the request through the existing codebase before planning changes.
- **Trace Path**:
  ```text
  UI Component / Route
          ↓
  State Management / Client Hooks
          ↓
  API Client / Service Layer
          ↓
  Backend Routes & Middleware (Auth / RBAC / Validation)
          ↓
  Controller & Service Logic
          ↓
  Database Schema & ORM Models (Prisma / SQL / NoSQL)
          ↓
  External Integrations & Webhooks
  ```
- **Identify**:
  - Database schema migrations or new models required.
  - API endpoint contracts (`GET`, `POST`, `PUT`, `DELETE`) and payload schemas.
  - Authorization requirements (role permissions, tenant isolation, IDOR boundaries).
  - Existing reusable components, utilities, and services to avoid duplication.
  - Performance bottlenecks (N+1 queries, unindexed foreign keys, memory footprint).

### Mode 3: User Stories & Acceptance Criteria (PM)
- **Objective**: Formulate testable user stories with explicit Given-When-Then acceptance criteria.
- **Format**:
  ```text
  As a <type of user>,
  I want <to perform some action>,
  So that <I achieve some business value>.
  ```
- **Acceptance Criteria Standard**: Every story must have Given-When-Then criteria covering:
  - Happy path scenarios.
  - Error and edge-case scenarios (invalid inputs, network timeouts, unauthorized access).
  - State boundaries (loading, empty, error, disabled buttons, duplicate submission prevention).

### Mode 4: Technical Design & Task Breakdown (Tech Lead)
- **Objective**: Create a detailed, actionable `implementation_plan.md` artifact.
- **Structure**:
  1. Component-by-component file changes (`[NEW]`, `[MODIFY]`, `[DELETE]`).
  2. Database migration strategy (non-destructive, backward-compatible).
  3. API contracts with request/response schemas.
  4. Testing strategy (Unit, Integration, E2E).
  5. User review and explicit approval gate.

### Mode 5: Implementation & Code Review (Senior Developer)
- **Objective**: Execute approved technical design preserving existing architecture.
- **Rules**:
  - Maintain existing code conventions, directory layouts, and design systems.
  - Zero emojis anywhere in source code, logs, comments, or commit messages.
  - Strong typing across all boundaries (Zod schemas for backend, TypeScript DTOs for frontend).
  - Reusable security middleware and centralized error handling.
  - No temporary workarounds or TODO-based logic.

### Mode 6: Automated QA & Release Gate (QA / Release Engineer)
- **Objective**: Prove the feature works and verify zero regressions.
- **Verification Gates**:
  - Backend integration test suites passing 100%.
  - Frontend component and unit test suites passing 100%.
  - Clean production build (`tsc -b && vite build` or equivalent).
  - Synchronized semantic version bump across all canonical version files.
  - Structured changelog maintenance (Keep a Changelog standard).
  - Git release tagging and active branch synchronization.

---

# 2. Skill Orchestration Matrix

The `agile-sdlc` skill acts as the master orchestrator, activating specialized engineering skills at each phase of the lifecycle:

```text
                               ┌── agile-sdlc (Master Orchestration Engine) ──┐
                               │                                              │
         ┌─────────────────────┼──────────────────────┬───────────────────────┼────────────────────┐
         ↓                     ↓                      ↓                       ↓                    ↓
  [Architecture]          [Security]              [Testing]                [DevOps]             [Design]
frontend-architecture  frontend-security      frontend-testing       continuous-integration  frontend-design
backend-architecture   backend-security       backend-testing        continuous-delivery     product-designer
python-architecture    flutter-security       flutter-testing        terraform-iac
flutter-architecture   indian-compliance-security                    ansible-automation
java-spring-architecture
```

| Lifecycle Phase | Primary Role | Activated Specialized Skills |
| :--- | :--- | :--- |
| **Discovery & Scoping** | BA / PM | `agile-sdlc`, `product-marketing`, `find-skills` |
| **UI/UX & Design** | Product Designer | `product-designer`, `frontend-design`, `behavioral-product-design` |
| **Architectural Design** | Tech Lead | `frontend-architecture`, `backend-architecture`, `python-architecture`, `flutter-architecture`, `java-spring-architecture` |
| **Security & Compliance** | Security Architect | `backend-security`, `frontend-security`, `flutter-security`, `indian-compliance-security` |
| **Implementation** | Senior Engineer | `openrouter-client-sdks`, `frontend-architecture`, `backend-architecture` |
| **QA & Verification** | QA Lead | `frontend-testing`, `backend-testing`, `flutter-testing` |
| **CI/CD & Release** | Release Engineer | `continuous-integration`, `continuous-delivery`, `terraform-iac`, `ansible-automation` |

---

# 3. Mandatory Checklists & Transition Gates

An agent MUST satisfy each gate before transitioning to the next phase:

### Gate 1: Requirement to Design Gate
- [ ] Business objective is unambiguous.
- [ ] User personas and permissions are identified.
- [ ] Out-of-scope boundaries are defined.
- [ ] Existing codebase has been inspected (not assumed).

### Gate 2: Design to Implementation Gate
- [ ] Implementation plan artifact created with complete file diff preview.
- [ ] Database schema changes verified for backward compatibility.
- [ ] API payload schemas defined with strict validation.
- [ ] User has explicitly approved the implementation plan.

### Gate 3: Implementation to QA Gate
- [ ] All code changes adhere to existing architecture and type systems.
- [ ] Zero lint, syntax, or static type errors.
- [ ] Loading, error, empty, and success states implemented.
- [ ] No hardcoded secrets, temporary hacks, or emojis.

### Gate 4: QA to Release Gate
- [ ] 100% automated test pass rate (backend + frontend).
- [ ] Production build succeeds cleanly with zero warnings/errors.
- [ ] Semantic version bumped across all synchronized version files.
- [ ] Structured CHANGELOG.md updated following Keep a Changelog.
- [ ] Git tag created and active development branch synchronized.

---

# 4. Anti-Patterns to Avoid

| Anti-Pattern | Why It Fails | Correct SDLC Action |
| :--- | :--- | :--- |
| **Immediate Coding** | Modifies files before understanding existing architecture; causes regressions. | Inspect repo first; trace UI $\rightarrow$ API $\rightarrow$ DB. |
| **Scope Creep** | Unplanned refactoring or rewriting working modules. | Keep scope strictly constrained to approved stories. |
| **Vague Acceptance Criteria** | "Make it look good" or "Handle errors properly". | Write explicit Given-When-Then criteria for every state. |
| **Silent Failures / Missing States** | UI hangs on loading or displays blank screen on error. | Implement `StateContainer`, skeletons, and error boundaries. |
| **Premature "Done" Declaration** | Declaring complete without running automated tests or build. | Execute `npm test` and `npm run build` before claiming completion. |
| **Unversioned Releases** | Pushing directly to main without semantic versioning or changelog. | Execute formal release governance with synchronized versions. |

---

# 5. Supporting Documentation & Resources

For detailed guidelines, templates, and reference workflows, consult:
- **References**:
  - [`references/requirement-analysis.md`](./references/requirement-analysis.md): Deep-dive requirement extraction.
  - [`references/user-stories.md`](./references/user-stories.md): Story breakdown and sizing.
  - [`references/acceptance-criteria.md`](./references/acceptance-criteria.md): Given-When-Then patterns.
  - [`references/technical-planning.md`](./references/technical-planning.md): Impact analysis and system design.
  - [`references/qa-and-uat.md`](./references/qa-and-uat.md): Test automation and verification gates.
  - [`references/release-management.md`](./references/release-management.md): Versioning, changelogs, and release gates.
- **Templates**:
  - [`templates/requirement.md`](./templates/requirement.md): Requirement specification template.
  - [`templates/user-story.md`](./templates/user-story.md): User story and acceptance criteria template.
  - [`templates/implementation-plan.md`](./templates/implementation-plan.md): Technical implementation plan template.
  - [`templates/test-plan.md`](./templates/test-plan.md): QA test plan and edge-case matrix.
  - [`templates/release-checklist.md`](./templates/release-checklist.md): Production release checklist.
- **Examples**:
  - [`examples/feature-lifecycle.md`](./examples/feature-lifecycle.md): End-to-end walkthrough from client request to production release.
