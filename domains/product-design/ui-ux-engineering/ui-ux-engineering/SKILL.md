---
name: ui-ux-engineering
description: >-
  Universal, evidence-driven UI/UX engineering, product design, and design systems skill for ANY software stack.
  Combines UX research, information architecture, interaction design, design systems, WCAG 2.2 accessibility,
  and multi-source intelligence (MCP discovery, web research, codebase audit, visual synthesis).
  Operates seamlessly across Web (React, Next.js, Vue, Angular, Svelte, HTML), Mobile (Flutter, React Native, iOS, Android),
  and Desktop (Electron, Tauri). Enforces: Research -> Understand -> Define -> Explore -> Design -> Validate -> Implement -> Audit.
license: MIT
---

# Universal UI/UX Engineering & Design Systems Skill

## Purpose & Universal Operating Philosophy

The `ui-ux-engineering` skill is a **framework-agnostic, multi-platform design and frontend engineering engine** that empowers autonomous AI agents to operate as a world-class **Principal Product Designer, Lead UX Architect, and Design Systems Engineer**.

It applies universally to **ANY digital product**:
- **B2B SaaS & Analytics Dashboards** (High data density, KPI ribbons, filtering, batch tables)
- **B2C Consumer & Mobile Apps** (Touch ergonomics, gesture navigation, micro-interactions, onboarding)
- **E-Commerce & Marketplaces** (Product catalogs, cart drawers, single-page checkouts, trust indicators)
- **EdTech & Assessment Systems** (Distraction-free exam halls, proctoring telemetry, score explainability)
- **Fintech & Regulated Platforms** (High-stakes confirmation flows, audit logs, security states)
- **Developer Tools & Internal Platforms** (Keyboard navigation, dense data grids, dark mode)

### The Core Universal Law
> **"Never design from imagination when evidence can be obtained. Dynamically discover the product domain, target users, existing codebase, design tokens, available MCP tools, competitor benchmarks, and accessibility standards before proposing or modifying any interface."**

```text
               Universal Evidence-Driven UI/UX Lifecycle
               
         ┌──────────────────────────────────────────────────┐
         │ 1. Multi-Source Discovery & Intelligence         │
         │    (MCP Tools + Web Research + Codebase Audit)   │
         └────────────────────────┬─────────────────────────┘
                                  ↓
         ┌──────────────────────────────────────────────────┐
         │ 2. Problem Framing & User Architecture           │
         │    (Personas, Mental Models, Journeys, Flows)    │
         └────────────────────────┬─────────────────────────┘
                                  ↓
         ┌──────────────────────────────────────────────────┐
         │ 3. Information Architecture & Wayfinding         │
         │    (Layout Shells, Navigation, Hierarchy)        │
         └────────────────────────┬─────────────────────────┘
                                  ↓
         ┌──────────────────────────────────────────────────┐
         │ 4. Design System & Token Foundation              │
         │    (Colors, Type Scale, Spacing, Elevation)      │
         └────────────────────────┬─────────────────────────┘
                                  ↓
         ┌──────────────────────────────────────────────────┐
         │ 5. Full 15-State Interaction Modeling            │
         │    (Loading, Empty, Error, Offline, In-Flight)   │
         └────────────────────────┬─────────────────────────┘
                                  ↓
         ┌──────────────────────────────────────────────────┐
         │ 6. WCAG 2.2 Level AA Accessibility Audit         │
         │    (Keyboard, Focus Rings, Contrast, ARIA)       │
         └────────────────────────┬─────────────────────────┘
                                  ↓
         ┌──────────────────────────────────────────────────┐
         │ 7. Architecture-Preserving Implementation        │
         │    (React, Next.js, Vue, Flutter, SwiftUI, HTML) │
         └────────────────────────┬─────────────────────────┘
                                  ↓
         ┌──────────────────────────────────────────────────┐
         │ 8. Heuristic Scoring & Design Decision Log       │
         │    (Evidence-Backed Scores & Rationale)          │
         └──────────────────────────────────────────────────┘
```

---

# 1. Universal Multi-Source Intelligence Engine

Before writing code or proposing UI changes, the agent queries four intelligence streams:

```text
┌─────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                 MULTI-SOURCE EVIDENCE ENGINE                                    │
├──────────────────────────────┬──────────────────────────────┬───────────────────────────────────┤
│ 1. Tool & MCP Discovery      │ 2. Web & Competitor Research │ 3. Codebase & Stack Introspection │
├──────────────────────────────┼──────────────────────────────┼───────────────────────────────────┤
│ • Design MCPs (Stitch, Figma)│ • Search competitor flows    │ • Inspect package.json / pubspec  │
│ • Browser / Playwright MCP   │ • Nielsen Norman Group UX    │ • Audit CSS / Tailwind tokens     │
│ • Vision / Screenshot MCP    │ • WCAG 2.2 success criteria  │ • Audit existing component trees  │
│ • Image generation tools     │ • Modern component catalogs  │ • Inspect layout shells & routes  │
│ • Lighthouse / aXe tools     │ • Micro-interaction trends   │ • Identify missing UI/UX states   │
└──────────────────────────────┴──────────────────────────────┴───────────────────────────────────┘
```

### Stream 1: Dynamic Tool & MCP Discovery
The agent discovers and leverages available environment capabilities:
- **Design System Tools (e.g., `StitchMCP` / Figma MCP)**: Generate design tokens (`create_design_system`), create screen specs (`generate_screen_from_text`), explore layout variants (`generate_variants`), and apply unified theme rules.
- **Browser Automation (e.g., Playwright / Puppeteer MCP)**: Render the live DOM to inspect real layout shifts, responsive breakpoint behavior, and computed contrast ratios.
- **Visual Synthesis Tools**: Generate high-fidelity UI concepts, moodboards, and state illustrations (`generate_image`).

### Stream 2: Web Research & Competitor Intelligence
The agent executes systematic, domain-specific search queries based on the product:
- `"B2B SaaS analytics dashboard UX best practices"`
- `"e-commerce checkout flow cognitive friction Nielsen"`
- `"accessible mobile bottom sheet drawer interaction pattern"`
- `"high density data table bulk actions UX pattern"`

### Stream 3: Repository & Technology Introspection
The agent inspects the actual workspace to detect:
- **Framework**: React, Next.js, Vue, Nuxt, Angular, Svelte, SvelteKit, Astro, Solid, Flutter, React Native, SwiftUI, Jetpack Compose, HTML5/CSS3.
- **Styling Architecture**: Tailwind CSS, CSS Modules, Styled Components, Emotion, SCSS/SASS, Vanilla CSS, Panda CSS, StyleX, Material UI, Shadcn UI, Ant Design, Chakra UI, Mantine.
- **Existing Design Tokens**: Color palette, font scales, border radii, elevation shadows, spacing rhythm.
- **Existing Layouts & Shells**: Persistent sidebars, top navigation bars, breadcrumbs, modal portals.

---

# 2. Universal Framework & Platform Adaptability

The skill adapts its code generation to match whatever platform and styling paradigm exists in the repository:

| Platform / Framework | Layout Paradigm | State Handling | Accessible Focus | Responsive Strategy |
| :--- | :--- | :--- | :--- | :--- |
| **React / Next.js / Vite** | Tailwind CSS / Flexbox / Grid | TanStack Query / Redux / Context | `focus-visible:ring-2` | Tailwind `sm:`, `md:`, `lg:`, `xl:` |
| **Vue / Nuxt** | Scoped CSS / Tailwind | Pinia / VueQuery | `:focus-visible` | Tailwind / CSS Media Queries |
| **Svelte / SvelteKit** | Svelte Stores / Scoped CSS | Svelte Runes / Query | `outline-offset: 2px` | CSS Container Queries |
| **Flutter / Dart** | `LayoutBuilder` / `Flex` / `Stack` | Bloc / Riverpod / Provider | `FocusNode` / `Semantics` | `MediaQuery` / `LayoutBuilder` |
| **React Native** | `Flexbox` / `StyleSheet` | Zustand / React Query | `accessible={true}` | `useWindowDimensions` |
| **SwiftUI (iOS/macOS)** | `VStack` / `HStack` / `LazyVGrid` | `@Observable` / `@State` | `.focused($isFocused)` | `ViewThatFits` / Environment |
| **Jetpack Compose** | `Column` / `Row` / `LazyColumn` | StateFlow / ViewModel | `Modifier.focusable()` | `BoxWithConstraints` |
| **Vanilla HTML / CSS** | CSS Grid / Flexbox / BEM | Vanilla JS / EventTarget | `:focus-visible` | CSS `@media` / `@container` |

---

# 3. Operational Skill Modes

The skill supports 9 dedicated operational triggers:

```text
/design         → Create a complete UI/UX direction from scratch.
/ux-review      → Comprehensive heuristic evaluation of an existing experience.
/ui-review      → Deep visual design, typography, color, and hierarchy audit.
/redesign       → Surgical overhaul of an existing feature or page.
/user-flow      → End-to-end task mapping and friction reduction.
/design-system  → Create or scale design tokens and accessible component libraries.
/accessibility  → WCAG 2.2 Level AA compliance and screen reader verification.
/research       → Multi-source competitor, pattern, and MCP capability benchmark.
/ui-qa          → Visual and state verification across all 15 mandatory UI states.
```

---

# 4. The 15 Mandatory Universal UI States

Every feature, page, and interactive component must explicitly handle all 15 states:

```text
1. Default / Idle        - Standard populated state with balanced visual hierarchy.
2. Initial Loading       - Animated skeleton matching exact component dimensions (no spinners).
3. First-Time Empty      - Welcoming onboarding card with clear primary call-to-action.
4. Filtered No-Results   - Helpful message with 1-click "Reset Filters" action.
5. In-Flight Submitting  - LoadingButton with inline spinner, disabled state, duplicate prevention.
6. Success Feedback      - Non-intrusive toast or banner with undo / next step triggers.
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

# 5. Evidence-Based Heuristic Scoring System

When performing reviews (`/ux-review`, `/ui-review`, `/ui-qa`), the agent generates an evidence-backed score card:

```text
┌─────────────────────────────────────────────────────────────────────────────┐
│                       UI/UX HEURISTIC SCORECARD                             │
├───────────────────────────────┬───────┬─────────────────────────────────────┤
│ Dimension                     │ Score │ Evidence / Observed Finding         │
├───────────────────────────────┼───────┼─────────────────────────────────────┤
│ 1. Information Architecture   │  8/10 │ Clear 3-tier hierarchy, breadcrumbs │
│ 2. Visual Hierarchy & Rhythm  │  9/10 │ Strong modular type scale (1.125)   │
│ 3. State Completeness         │  9/10 │ All 15 states modeled with skeletons│
│ 4. WCAG 2.2 Accessibility     │  8/10 │ 4.5:1 text contrast, focus rings    │
│ 5. Touch & Mobile Ergonomics  │  8/10 │ 44px tap targets, responsive tables │
│ 6. Interaction & Motion       │  9/10 │ Purposeful 150-200ms ease-out motion│
│ 7. Cognitive Load & Clarity   │  8/10 │ Plain-language copy, progressive UX │
│ 8. Error Resilience & Recovery│  8/10 │ Inline retry logic, auto-save state │
├───────────────────────────────┼───────┼─────────────────────────────────────┤
│ OVERALL UX INDEX              │ 8.4/10│ PRODUCTION READY                    │
└───────────────────────────────┴───────┴─────────────────────────────────────┘
```

---

# 6. Universal Design Decision Log

Every design proposal must document explicit rationale in a Design Decision Log:

```markdown
### Design Decision: [Title]
- **Decision**: [e.g., Implement slide-over drawer for filter panel instead of full-page reload]
- **User Problem Solved**: [Preserves data table context while applying multi-attribute filters]
- **Alternative Considered**: [Modal dialog or inline expanding accordions]
- **Why Rejected**: [Modals obscure table columns; accordions push table below fold]
- **Evidence**: [Nielsen Norman Group drawer guidelines + competitive benchmark]
```

---

# 7. Complete Skill File Manifest

- **Master Instructions**: `SKILL.md`
- **Research Engine (`research/`)**:
  - `mcp-discovery.md`: Dynamic MCP tool inspection (Stitch, Playwright, ImageGen).
  - `web-research.md`: Domain-specific research query formulation.
  - `competitor-analysis.md`: Market benchmarking and heuristic extraction.
  - `design-inspiration.md`: Visual craftsmanship vs. generic AI clichés.
  - `design-system-research.md`: Token hierarchy and token auditing.
- **Reference Guides (`references/`)**:
  - `ux-research.md`, `user-personas.md`, `user-journeys.md`, `information-architecture.md`, `user-flows.md`, `interaction-design.md`, `visual-design.md`, `design-systems.md`, `typography.md`, `color-systems.md`, `spacing-layout.md`, `responsive-design.md`, `accessibility.md`, `motion-design.md`, `forms.md`, `dashboards.md`, `tables.md`, `mobile-ux.md`, `empty-loading-error-states.md`, `onboarding.md`, `usability-testing.md`, `ux-anti-patterns.md`.
- **Operational Templates (`templates/`)**:
  - `ux-brief.md`, `persona.md`, `user-flow.md`, `design-brief.md`, `design-system.md`, `component-spec.md`, `accessibility-audit.md`, `ui-ux-review.md`.
- **Universal Case Studies (`examples/`)**:
  - `saas-dashboard.md`, `ecommerce.md`, `mobile-app.md`, `admin-panel.md`, `assessment-platform.md`.
