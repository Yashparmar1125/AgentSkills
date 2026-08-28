# Acceptance Criteria & Given-When-Then Specification Guide

## Purpose
This guide defines how to write unambiguous, testable acceptance criteria using the **Given-When-Then (Gherkin)** standard to drive automated test development.

---

## 1. The Given-When-Then Format

Every Acceptance Criterion (AC) must establish:
- **GIVEN**: The initial context, user role, session state, and existing database preconditions.
- **WHEN**: The specific user action, event trigger, or API call that occurs.
- **THEN**: The observable outcome, state mutation, feedback, and database persistence.

```gherkin
Scenario: [Descriptive Scenario Name]
  Given [initial state, authenticated user role, existing records]
  When [user executes an action, clicks button, or submits form]
  Then [expected UI feedback, status code, data mutation, or redirection]
```

---

## 2. Standard Acceptance Criteria Coverage

For any feature, the agent must define acceptance criteria covering the **4 Pillars of UI/API State**:

```text
                             ┌── 1. Happy Path (Valid submission & success feedback)
                             ├── 2. Validation & Edge Cases (Invalid inputs, boundary limits)
Acceptance Criteria Matrix ──┼── 3. Security & Authorization (RBAC, unauthenticated, IDOR)
                             └── 4. State & Resilience (Loading skeleton, error banner, retry)
```

### 2.1 Happy Path Scenario
```gherkin
Scenario: Teacher successfully creates a new exam
  Given an authenticated user with role "TEACHER"
  And the user is on the Create Exam page
  When the user enters a valid title, duration (60 mins), and 20 questions
  And clicks "Publish Exam"
  Then the exam status is persisted as "PUBLISHED" in the database
  And a success toast "Exam published successfully" is displayed
  And the user is redirected to the Teacher Dashboard
```

### 2.2 Input Validation & Boundary Scenario
```gherkin
Scenario: Reject exam creation with zero duration or missing title
  Given an authenticated user with role "TEACHER"
  When the user submits the form with an empty title or duration = 0
  Then the API returns HTTP 400 Bad Request with field validation errors
  And the UI displays inline error banners beneath the invalid fields
  And the submit button remains enabled for correction
```

### 2.3 Security & Role-Based Access Scenario
```gherkin
Scenario: Prevent students from accessing teacher exam creation API
  Given an authenticated user with role "STUDENT"
  When the user sends a POST request to "/api/exams"
  Then the server rejects the request with HTTP 403 Forbidden
  And no exam record is created in the database
```

### 2.4 State Management & Duplicate Prevention Scenario
```gherkin
Scenario: Disable submit button during active API request
  Given an authenticated user submits the exam form
  When the network request is in-flight
  Then the "Publish Exam" button transitions to a disabled loading state with a spinner
  And repeated clicks do NOT generate duplicate API requests
```
