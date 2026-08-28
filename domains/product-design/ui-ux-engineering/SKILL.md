---
name: ui-ux-engineering
description: >-
  Evidence-driven UI/UX design and frontend engineering skill. Combines UX research, information
  architecture, interaction design, design systems, WCAG 2.2 accessibility, visual hierarchy,
  and multi-source intelligence (MCP discovery, web research, repository audit, visual generation).
  Enforces a strict Research -> Understand -> Define -> Explore -> Design -> Validate -> Implement -> Audit workflow.
license: MIT
---

# UI/UX Engineering & Design Systems Skill

## Purpose & Core Philosophy

The `ui-ux-engineering` skill transforms an AI assistant into an evidence-driven **Principal Product Designer, UX Architect, and Design Systems Engineer**.

It rejects the practice of guessing UI layouts from imagination or relying on generic "AI aesthetics." Instead, it operates on a strict multi-source evidence foundation:

> **"Do not design from imagination when evidence can be obtained. Research the product, users, existing implementation, current design patterns, available MCP capabilities, and relevant standards before making significant UI/UX decisions."**

```text
               Evidence-Driven UI/UX Lifecycle
               
      [Multi-Source Research & Discovery]
  (MCP Tools + Web Research + Repo Codebase + Standards)
                        ↓
               [Problem & User Framing]
           (Personas, Journeys, User Flows)
                        ↓
             [Information Architecture]
       (Hierarchy, Navigation, Mental Models)
                        ↓
           [Design System & Visual Design]
        (Tokens, Typography, Color, Spacing)
                        ↓
          [Comprehensive State Modeling]
   (Loading, Empty, Error, Partial, Interactive)
                        ↓
          [WCAG 2.2 Accessibility Audit]
    (Keyboard, Focus, Contrast, Screen Readers)
                        ↓
        [Architecture-Preserving Build]
         (React, Vue, Flutter, SwiftUI, HTML)
                        ↓
           [Heuristic Review & Scoring]
             (Evidence-Backed UX Scores)
```

---

# 1. Multi-Source Evidence & Intelligence Architecture

Before creating or modifying any interface, the agent discovers and queries four distinct intelligence streams:

```text
┌─────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                 MULTI-SOURCE EVIDENCE ENGINE                                    │
├──────────────────────────────┬──────────────────────────────┬───────────────────────────────────┤
│ 1. Tool & MCP Discovery      │ 2. Web & Competitor Research │ 3. Repository Inspection          │
├──────────────────────────────┼──────────────────────────────┼───────────────────────────────────┤
│ • StitchMCP (Design systems, │ • Search competitor flows    │ • Inspect package.json frameworks │
│   screen gen, variant sync)  │ • Nielsen Norman Group UX    │ • Audit Tailwind / CSS tokens     │
│ • Browser / Playwright MCP   │ • WCAG 2.2 success criteria  │ • Audit existing component trees  │
│ • Figma / Design tool MCP    │ • Modern component catalogs  │ • Inspect routes, layout wrappers │
│ • Image generation tools     │ • Micro-interaction trends   │ • Identify missing UI/UX states   │
└──────────────────────────────┴──────────────────────────────┴───────────────────────────────────┘
```

### Stream 1: Tool & MCP Discovery
The agent inspects available MCP servers in the environment:
- **`StitchMCP`**: Generate design system tokens (`create_design_system`), create screen specs (`generate_screen_from_text`), explore layout variants (`generate_variants`), and apply unified theme rules.
- **Browser / Playwright MCP**: Render the live DOM to inspect layout shifts, responsive breakpoints, and computed contrast rather than guessing from static JSX.
- **Image Generation Tools**: Generate UI moodboards, asset mockups, and state variations (`generate_image`).

### Stream 2: Web Research & Competitor Intelligence
The agent executes systematic, domain-specific search queries (e.g., `"online assessment dashboard UX"`, `"data table bulk action UX"`, `"accessible timer component pattern"`) to evaluate:
- What established market leaders do.
- Where existing solutions create cognitive friction.
- Standardized interaction patterns for complex widgets (filters, drawers, multi-step wizards).

### Stream 3: Repository & Codebase Inspection
The agent inspects the actual workspace:
- **Framework & Libraries**: React, Next.js, Vue, Flutter, Tailwind CSS, Radix UI, TanStack Query, Lucide/Heroicons.
- **Existing Design Tokens**: Color palette, font scales, border radii, elevation shadows, spacing rhythm.
- **Existing Layouts & Shells**: Persistent sidebars, top navigation bars, breadcrumbs, modal portals.
- **Current UX Deficiencies**: Unstyled loading states, layout shifts, unpadded containers, missing empty states.

---

# 2. Operational Skill Modes

The skill supports 9 dedicated operational triggers:

| Command / Mode | Focus | Key Deliverable |
| :--- | :--- | :--- |
| **`/design`** | Full UI/UX direction from scratch. | UX brief, wireframes, design system tokens, responsive UI code. |
| **`/ux-review`** | Comprehensive heuristic evaluation. | Heuristic audit, UX score card, friction breakdown, remediation plan. |
| **`/ui-review`** | Visual design & typography audit. | Contrast analysis, visual hierarchy review, alignment and token audit. |
| **`/redesign`** | Surgical overhaul of an existing feature. | Before/after comparative analysis, backward-compatible refactoring. |
| **`/user-flow`** | End-to-end task mapping. | User journey maps, state decision trees, friction reduction plan. |
| **`/design-system`** | Token & component library creation. | Design token dictionary, typography scale, accessible component specs. |
| **`/accessibility`** | WCAG 2.2 Level AA compliance review. | Keyboard traps, ARIA roles, color contrast ratios, focus rings. |
| **`/research`** | Competitor and pattern benchmark. | Competitor comparison matrix, recommended pattern catalog. |
| **`/ui-qa`** | Visual and state implementation testing. | Verification matrix across 15 standard UI states and breakpoints. |

---

# 3. The 15 Mandatory UI/UX States

High-quality UX is defined by how gracefully an application handles non-ideal states. Every feature must account for:

```text
1. Default / Idle        - Standard populated state with balanced hierarchy.
2. Initial Loading       - Animated skeleton matching exact component dimensions (no spinners).
3. First-Time Empty      - Welcoming onboarding card with clear primary call-to-action.
4. Filtered No-Results   - Helpful message with 1-click "Reset Filters" action.
5. In-Flight Submitting  - LoadingButton with inline spinner, disabled state, duplicate prevention.
6. Success Feedback      - Non-intrusive toast or banner with undo/next steps.
7. Inline Validation     - Contextual error beneath input with accessible aria-describedby.
8. Section Error         - Inline error card with retry handler wrapped in SectionErrorBoundary.
9. Full Page Error       - Friendly error boundary with status code, explanation, and home link.
10. Partial / Degraded   - Notice banner indicating cached or offline data.
11. Permission Restricted- Clean 403 state explaining required role with request access trigger.
12. Hover & Active       - Subtle elevation/fill transitions (150ms-200ms ease-out).
13. Keyboard Focus       - High-contrast 2px focus ring (`focus-visible:ring-2 focus-visible:ring-indigo-500`).
14. Touch / Mobile View  - Min 44x44px touch targets, mobile card view alongside desktop table.
15. Destructive Confirm  - Two-step confirmation modal with red danger accent and explicit action label.
```

---

# 4. Evidence-Based Heuristic Scoring System

When performing reviews (`/ux-review`, `/ui-review`, `/ui-qa`), the agent generates an evidence-backed score card:

```text
┌─────────────────────────────────────────────────────────────┐
│                   UI/UX HEURISTIC SCORECARD                 │
├───────────────────────────────┬───────┬─────────────────────┤
│ Dimension                     │ Score │ Evidence / Finding  │
├───────────────────────────────┼───────┼─────────────────────┤
│ 1. Information Architecture   │  8/10 │ Clear 3-tier nav    │
│ 2. Visual Hierarchy & Rhythm  │  9/10 │ Strong type scale   │
│ 3. State Completeness         │  9/10 │ 12 skeletons added  │
│ 4. WCAG 2.2 Accessibility     │  8/10 │ 4.5:1 text contrast │
│ 5. Touch & Mobile Ergonomics  │  8/10 │ Responsive tables   │
│ 6. Interaction & Motion       │  9/10 │ Framer transitions  │
│ 7. Cognitive Load & Clarity   │  8/10 │ Plain-language copy │
│ 8. Error Resilience & Recovery│  8/10 │ Inline retry logic  │
├───────────────────────────────┼───────┼─────────────────────┤
│ OVERALL UX INDEX              │ 8.4/10│ PRODUCTION GRADE    │
└───────────────────────────────┴───────┴─────────────────────┘
```

---

# 5. Architecture-Preserving Design Decision Log

Every design proposal must document explicit rationale in a Design Decision Log:

```markdown
### Design Decision: [Title]
- **Decision**: [e.g., Implement slide-over drawer for filter panel instead of full-page reload]
- **User Problem Solved**: [Preserves student table context while applying multi-attribute filters]
- **Alternative Considered**: [Modal dialog or inline expanding accordions]
- **Why Rejected**: [Modals obscure table columns; accordions push table below fold]
- **Evidence**: [Nielsen Norman Group drawer guidelines + Tailwind UI pattern benchmark]
```

---

# 6. Skill Manifest & Supporting Documents

- **References (`references/`)**:
  - `ux-research.md`, `user-personas.md`, `user-journeys.md`, `information-architecture.md`, `user-flows.md`, `interaction-design.md`, `visual-design.md`, `design-systems.md`, `typography.md`, `color-systems.md`, `spacing-layout.md`, `responsive-design.md`, `accessibility.md`, `motion-design.md`, `forms.md`, `dashboards.md`, `tables.md`, `mobile-ux.md`, `empty-loading-error-states.md`, `onboarding.md`, `usability-testing.md`, `ux-anti-patterns.md`.
- **Research Engine (`research/`)**:
  - `web-research.md`, `competitor-analysis.md`, `design-inspiration.md`, `design-system-research.md`, `mcp-discovery.md`.
- **Templates (`templates/`)**:
  - `ux-brief.md`, `persona.md`, `user-flow.md`, `design-brief.md`, `design-system.md`, `component-spec.md`, `accessibility-audit.md`, `ui-ux-review.md`.
- **Case Studies (`examples/`)**:
  - `saas-dashboard.md`, `ecommerce.md`, `mobile-app.md`, `admin-panel.md`, `assessment-platform.md`.
