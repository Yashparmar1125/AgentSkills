# Design System Benchmark & Token Architecture Guide

## Purpose
This guide defines standards for auditing existing design systems and constructing extensible design token architectures.

---

## 1. The Design Token Hierarchy

Design tokens bridge design decisions and codebase implementation across three tiers:

```text
[Global / Primitive Tokens]  (e.g., color.blue.600: #2563eb, font.sans: Inter)
            ↓
[Semantic / Alias Tokens]     (e.g., color.brand.primary: color.blue.600, color.surface.card: color.slate.50)
            ↓
[Component-Scoped Tokens]   (e.g., button.primary.bg: color.brand.primary, table.row.border: color.border.subtle)
```

---

## 2. Token Auditing in Codebases

When inspecting a project:
1. **Color Tokens**: Check `tailwind.config.js` or CSS custom properties for primary, surface, text, border, and semantic alert tokens (`success`, `warning`, `danger`, `info`).
2. **Typography Scale**: Verify base font size (`16px`), scale ratio (e.g., Major Second `1.125` or Minor Third `1.2`), and line-height pairings.
3. **Spacing Rhythm**: Enforce a strict 4px / 8px grid (`4px`, `8px`, `12px`, `16px`, `24px`, `32px`, `48px`, `64px`).
4. **Elevation & Shadows**: Verify light and dark mode elevation levels (`shadow-sm`, `shadow-md`, `shadow-xl`, `shadow-2xl`).
