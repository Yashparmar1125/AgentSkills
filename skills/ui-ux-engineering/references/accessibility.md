# Accessibility & WCAG 2.2 Compliance Guide

## 1. The 4 Principles of Accessibility (POUR)
- **Perceivable**: Text alternatives for images, high color contrast, visible focus indicators.
- **Operable**: Full keyboard accessibility (Tab, Enter, Space, Escape, Arrows), zero keyboard traps.
- **Understandable**: Clear error messages, predictable navigation, plain language labels.
- **Robust**: Clean semantic HTML (`<button>`, `<main>`, `<nav>`, `<dialog>`), valid ARIA roles.

## 2. Key WCAG 2.2 Checkpoints
- **Focus Appearance (2.4.13)**: Focus rings must have $\ge 2\text{px}$ thickness and $\ge 3:1$ contrast against adjacent background.
- **Target Size Minimum (2.5.8)**: Interactive elements must measure $\ge 24\text{px} \times 24\text{px}$ (preferably $44\text{px} \times 44\text{px}$).
- **Accessible Names (4.1.2)**: Icon-only buttons must have `aria-label="Close dialog"` or visually hidden text.
- **Reduced Motion (2.3.3)**: Honor `prefers-reduced-motion` media queries for animations.
