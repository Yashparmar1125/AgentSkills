# Example: End-to-End Feature Lifecycle Walkthrough

## Scenario: Client Requests "Question Bank Management"

---

### Step 1: Requirement Discovery (BA / PM Mode)
- **Client Request**: *"Add a question bank to the exam app so teachers can reuse questions."*
- **Scoping**:
  - Who can create question banks? $\rightarrow$ Teachers & Admins.
  - Can students view banks? $\rightarrow$ No (Strict RBAC).
  - Are question banks private or shared across teachers in an organization? $\rightarrow$ Organization-level sharing.

---

### Step 2: Repository Impact Analysis (Architect Mode)
- **Trace existing codebase**:
  - `backend/prisma/schema.prisma`: `Question` model exists, linked directly to `Exam`. Need a new `QuestionBank` model with 1-to-many `Question` relation.
  - `backend/src/routes/`: Add `/api/v1/question-banks` protected by `verifyToken` and `requireRole(['TEACHER', 'ADMIN'])`.
  - `frontend/src/features/`: Add modular package `features/question-banks/` with `useQuestionBanksData` hook and presentational components.

---

### Step 3: User Stories & Acceptance Criteria (PM Mode)
```gherkin
Feature: Question Bank Management

  Scenario: Teacher creates a new question bank
    Given an authenticated user with role "TEACHER"
    When the teacher sends POST "/api/v1/question-banks" with title "JLPT N5 Grammar"
    Then the bank is created in the database with status "ACTIVE"
    And the response returns HTTP 201 with the created bank object

  Scenario: Student cannot access question bank API
    Given an authenticated user with role "STUDENT"
    When the student sends GET "/api/v1/question-banks"
    Then the server returns HTTP 403 Forbidden
```

---

### Step 4: Implementation Plan & Review Gate (Tech Lead Mode)
- Created `implementation_plan.md` detailing:
  - Prisma migration for `QuestionBank` model.
  - Express controller and Zod validation schemas.
  - Vitest integration test suite.
  - React Query hooks and UI views.
- **Obtain User Approval**: STOP and wait for confirmation before writing code.

---

### Step 5: Implementation & Automated Testing (Dev / QA Mode)
- Applied non-destructive Prisma migration.
- Implemented backend controller and services with Zod validation.
- Authored Vitest integration suite $\rightarrow$ 100% tests passed.
- Built React views with `StateContainer` and `SkeletonDashboard`.
- Ran frontend test suite and `npm run build` $\rightarrow$ clean build in 6.8s.

---

### Step 6: Production Release Gate (Release Mode)
- Synchronized version across all 4 files (`v2.4.0`).
- Updated `backend/CHANGELOG.md` and `frontend/CHANGELOG.md`.
- Merged `dev` into `main`, tagged `v2.4.0`, pushed to remote, and switched back to `dev`.
