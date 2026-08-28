# Tool & MCP Discovery for UI/UX Engineering

## Purpose
This guide outlines how to dynamically discover, inspect, and leverage specialized Model Context Protocol (MCP) servers and native tools to elevate UI/UX design and verification.

---

## 1. The MCP Discovery Workflow

When a UI/UX task is initiated, the agent evaluates available environment tools:

```text
[UI/UX Task Initiated]
          ↓
[Inspect Available Tools / MCP Servers]
          ↓
┌─────────────────────────────────────────────────────────────┐
│ Category 1: Design Systems & Component Generation (Stitch) │
│ Category 2: Live Browser DOM & Visual Inspection (Playwright)│
│ Category 3: Image Generation & Concept Mockups (ImageGen)   │
│ Category 4: Web Search & Competitor Research (WebSearch)    │
└─────────────────────────────────────────────────────────────┘
          ↓
[Execute Multi-Source Intelligence Stream]
```

---

## 2. Supported MCP Tool Categories

### 2.1 Design System & Screen Generation (e.g., `StitchMCP`)
- **Capabilities**:
  - `create_design_system` / `create_design_system_from_design_md`: Generate standardized design token models (colors, typography, radii, spacing).
  - `generate_screen_from_text`: Convert UX briefs directly into structured screen layouts and component trees.
  - `generate_variants`: Produce layout, density, and color theme variations for comparative evaluation.
  - `apply_design_system`: Enforce unified design tokens across multiple screens.

### 2.2 Live Browser & Runtime DOM Inspection (e.g., Playwright / Puppeteer MCP)
- **Capabilities**:
  - Render the application at standard breakpoints (375px mobile, 768px tablet, 1280px desktop, 1920px widescreen).
  - Inspect computed CSS styles, layout shift (CLS), and real contrast ratios.
  - Execute automated accessibility tree audits (aXe-core integration).

### 2.3 Visual Synthesis & Multi-Modal Concepting
- **Capabilities**:
  - `generate_image`: Create UI concept art, high-fidelity mockups, banner assets, and empty-state illustrations.
  - Image analysis: Compare implemented UI screenshots against target design specifications.
