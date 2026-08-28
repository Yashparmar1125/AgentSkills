# User Story & Acceptance Criteria Template

### Story ID: US-[NUMBER]
**Title**: [Short Action-Oriented Title]

---

### 1. User Story Statement
**As a** [specific user role],  
**I want to** [execute an action or access a capability],  
**So that** [I achieve a specific outcome or business value].

---

### 2. Preconditions & Assumptions
- **Preconditions**: [e.g., User is authenticated with TEACHER role, exam pack exists]
- **Assumptions**: [e.g., File upload size is capped at 10MB]

---

### 3. Acceptance Criteria (Given-When-Then)

#### Scenario 1: Successful Primary Flow (Happy Path)
- **Given** [initial state and context]
- **When** [user performs action]
- **Then** [expected result and feedback]

#### Scenario 2: Validation Failure
- **Given** [user enters invalid data]
- **When** [user attempts submission]
- **Then** [field error displayed, form not submitted]

#### Scenario 3: Unauthorized Access Attempt
- **Given** [unauthorized user role or unauthenticated session]
- **When** [request is dispatched]
- **Then** [HTTP 401/403 returned, access denied]

#### Scenario 4: Network & State Resilience
- **Given** [request is in-flight]
- **When** [user clicks submit]
- **Then** [button enters loading state, duplicate submission blocked]
