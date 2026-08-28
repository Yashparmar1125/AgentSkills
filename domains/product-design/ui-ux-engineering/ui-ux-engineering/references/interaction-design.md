# Interaction Design & Micro-Interaction Guide

## 1. The 4 Stages of a Micro-Interaction
```text
[Trigger] (User clicks button / toggles switch)
    ↓
[Rules] (Validate payload, disable button, start spinner)
    ↓
[Feedback] (Button shows spinner, ripple effect, inline notification)
    ↓
[Loops & Modes] (Success state for 2s, transition back to idle or redirect)
```

## 2. Interaction Timing & Easing Curves
- **Micro-interactions (Hover, Press)**: 100ms - 150ms (`ease-out`).
- **Surface Transitions (Modals, Drawers)**: 200ms - 300ms (`cubic-bezier(0.16, 1, 0.3, 1)`).
- **Page Transitions**: 250ms - 350ms with subtle opacity and Y-axis offset.
