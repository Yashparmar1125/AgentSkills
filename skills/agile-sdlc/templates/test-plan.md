# QA Test Plan & Edge-Case Matrix Template

## 1. Feature Under Test
- **Module**: [Module Name]
- **Target Version**: [vX.Y.Z]

---

## 2. Test Execution Matrix

| Test ID | Category | Scenario Description | Inputs / Setup | Expected Outcome | Verification Status |
| :--- | :--- | :--- | :--- | :--- | :---: |
| **TC-01** | Happy Path | Successful creation with valid inputs | Valid payload | HTTP 201 + record created | [ ] |
| **TC-02** | Validation | Reject missing required fields | Empty body | HTTP 400 + field errors | [ ] |
| **TC-03** | Boundary | Max length / limit overflow | 1001 items (limit 1000) | HTTP 422 limit exceeded | [ ] |
| **TC-04** | Security | Unauthorized role access | Non-admin token | HTTP 403 Forbidden | [ ] |
| **TC-05** | IDOR | Cross-tenant record modification | User A token on User B ID | HTTP 404/403 Rejected | [ ] |
| **TC-06** | State | UI duplicate submit prevention | Fast double click | Only 1 request dispatched | [ ] |
| **TC-07** | Resilience | Network failure & retry | Mock 500 error | Error card + retry works | [ ] |

---

## 3. Automated Test Command Reference
```bash
# Backend suite
npm test

# Frontend suite
npm test

# Production build
npm run build
```
