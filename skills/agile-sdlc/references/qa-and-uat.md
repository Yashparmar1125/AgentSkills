# QA Automation & User Acceptance Testing (UAT) Guide

## Purpose
This guide defines standards for verifying that implemented code satisfies all acceptance criteria, maintains zero regressions, and passes formal release quality gates.

---

## 1. Automated Testing Pyramid

```text
               / \
              /   \
             / E2E \       User Workflows (Playwright / Cypress)
            /-------\
           / Integr. \     API & Database Transactions (Vitest / Supertest)
          /-----------\
         /  Unit / Comp \  Hooks, Utilities, Components (React Testing Library)
        /-----------------\
```

### 1.1 Backend Quality Gate
- **Authentication & RBAC**: Every endpoint must verify allowed roles and reject unauthorized requests (HTTP 401 / 403).
- **IDOR / Tenant Isolation**: Ensure Student A cannot access Student B's submission or results.
- **Database Transactions**: Rollbacks verified when dependent operations fail.
- **Accuracy Suites**: Mathematical formulas (risk scores, velocity, proctoring penalties) verified with 100% precision.

### 1.2 Frontend Quality Gate
- **Component Tests**: Modals open/close, forms validate, buttons disable during submission.
- **State Handling**: Skeletons display during loading, error cards display on failure with working retry handlers.
- **Production Build**: Clean compilation (`tsc -b && vite build`) with zero type errors.

---

## 2. UAT Feedback Protocol

When user acceptance feedback is received:
1. **Never dismiss feedback as trivial**: Treat every defect as a structured bug report.
2. **Reproduce via test first**: Write a failing test matching the user's reported scenario before fixing the code.
3. **Fix and verify**: Run the test suite to prove the fix and prevent regressions.
