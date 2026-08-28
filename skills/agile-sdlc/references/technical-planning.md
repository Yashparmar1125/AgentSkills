# Technical Planning & Impact Analysis Guide

## Purpose
This guide defines the Tech Lead methodology for performing repository discovery, architectural impact analysis, data modeling, and task breakdown before writing code.

---

## 1. Full-Stack Trace Analysis

Before authoring an implementation plan, the agent must trace the feature end-to-end through the existing codebase:

```text
[Frontend Route / Page]
        ↓
[Feature Hooks & TanStack Query State]
        ↓
[Typed API Client / Axios Layer]
        ↓
[Backend Express / Fastify Route Definitions]
        ↓
[Auth, RBAC, Rate-Limit & Validation Middleware]
        ↓
[Controller Handler]
        ↓
[Service Layer & Business Domain Logic]
        ↓
[Database Repository / Prisma / ORM Model]
        ↓
[Database Schema, Indexes & Foreign Keys]
```

---

## 2. Impact Assessment Matrix

| Layer | Impact Area | Questions to Inspect in Codebase |
| :--- | :--- | :--- |
| **Database** | Schema, Migrations | Are new tables, columns, enums, or relations required? Is the migration non-destructive? Are foreign keys indexed? |
| **Backend API** | Endpoints, Schemas | What routes are added/modified? Are Zod/Joi validation schemas defined? Are responses sanitized? |
| **Security** | Auth, RBAC, IDOR | Which roles can access each route? Is cross-tenant isolation verified? Are inputs parameterized? |
| **Frontend State** | React Query, Redux | How is server state cached? What is the invalidation key? Are loading and error states handled? |
| **UI Components** | Modals, Forms, Views | Are existing reusable components (`StateContainer`, `LoadingButton`, `ErrorBoundary`) reused? |
| **Testing** | Suites, Fixtures | What integration tests are needed? Are factories or mock handlers updated? |

---

## 3. Technical Task Breakdown Standard

Technical tasks must be grouped logically by dependency order:

1. **Phase 1: Database & Data Modeling** (Prisma schema, migrations, seed data).
2. **Phase 2: Backend Services & API Endpoints** (Validation schemas, controllers, service logic, routes).
3. **Phase 3: Backend Automated Tests** (Vitest integration suites, RBAC verification).
4. **Phase 4: Frontend API Layer & Hooks** (DTO types, API clients, TanStack Query hooks).
5. **Phase 5: Frontend Components & Views** (UI forms, skeletons, modals, error boundaries).
6. **Phase 6: Frontend Automated Tests & Build** (Component tests, production build verification).
