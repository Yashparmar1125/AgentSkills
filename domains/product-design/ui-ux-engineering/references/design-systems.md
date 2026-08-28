# Design Systems & Component Governance Guide

## 1. Atomic Design Hierarchy
```text
[Tokens] (Color, Typography, Spacing, Elevation)
   ↓
[Atoms] (Button, Input, Badge, Avatar, Icon)
   ↓
[Molecules] (SearchBar, FormField, StatCard, Breadcrumb)
   ↓
[Organisms] (TableWithFilter, Navbar, ModalPortal, ProctoringCard)
   ↓
[Templates / Layouts] (DashboardLayout, ExamHallLayout)
   ↓
[Pages] (AdminReportsPage, StudentExamPage)
```

## 2. Component Contract Standard
Every design system component must export:
- Strict TypeScript props interface.
- Controlled and uncontrolled state support where applicable.
- Full accessibility attributes (`aria-expanded`, `aria-controls`, `role`).
