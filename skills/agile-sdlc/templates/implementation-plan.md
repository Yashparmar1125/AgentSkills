# Technical Implementation Plan Template

## 1. Feature Overview
- **Feature Name**: [Name]
- **Target Release**: [vX.Y.Z]
- **Estimated Complexity**: [Small / Medium / Large]

---

## 2. User Review Required
> [!IMPORTANT]
> [Critical design decisions, breaking changes, or schema mutations requiring review]

---

## 3. Architecture & Impact Analysis

### 3.1 Data Flow Tracing
```text
[Frontend View] → [Custom Hook] → [Axios Client] → [Express Route] → [Controller] → [Service] → [Prisma DB]
```

### 3.2 Database Schema & Migrations
- [Describe any new tables, columns, enums, or foreign key indexes]

### 3.3 API Contracts & Payloads
- `METHOD /api/v1/[endpoint]`
  - Request Payload Schema: `ZodSchema`
  - Response Payload: `DTO`
  - Auth/RBAC: `[ROLES]`

---

## 4. Proposed File Changes

### Component / Module: [Name]
- `[NEW]` `path/to/new-file.ts` - [Purpose]
- `[MODIFY]` `path/to/existing-file.ts` - [Changes]
- `[DELETE]` `path/to/obsolete-file.ts` - [Rationale]

---

## 5. Verification Plan

### Automated Test Suites
- [Backend Vitest commands]
- [Frontend Vitest commands]
- [Build command]

### Manual Verification Scenarios
- [Step 1]
- [Step 2]
