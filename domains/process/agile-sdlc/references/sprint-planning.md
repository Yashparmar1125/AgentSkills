# Sprint Planning & Work Breakdown Guide

## Purpose
This guide defines standards for scoping, sizing, and sequencing deliverables within Agile sprint iterations.

---

## 1. Sprint Sizing & Complexity Estimation

The agent evaluates feature complexity based on structural risk and dependencies:

| Complexity Tier | Characteristics | Typical Tasks |
| :--- | :--- | :--- |
| **Small (1-2 pts)** | Minor UI tweak, bug fix, single API field addition, new test case. | 1-2 files modified, minimal risk. |
| **Medium (3-5 pts)** | New CRUD endpoint, new modal component, custom React Query hook, validation schema. | 3-6 files modified, 1-2 test suites. |
| **Large (8-13 pts)** | New domain feature module, database migration with relation changes, multi-step exam wizard, security telemetry. | 7-15 files modified, end-to-end full-stack trace, multiple test suites. |
| **Epic (>13 pts)** | Architectural refactor, platform-wide state overhaul, new subsystem. | MUST be decomposed into smaller user stories. |

---

## 2. Dependency Ordering & Critical Path

When planning sprint execution:
1. **Never block frontend on backend**: Define typed DTO contracts (`types/dto.ts`) and mock data early so UI development can proceed concurrently.
2. **Execute Database $\rightarrow$ Backend $\rightarrow$ Frontend**: Ensures APIs are stable before UI integration.
3. **Continuous Verification**: Run test suites after each logical layer is completed rather than deferring all testing to the end.
