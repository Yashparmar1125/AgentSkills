# Accessibility Audit Report Template

## Target: [Page / Component URL or Path]
- **Audit Standard**: WCAG 2.2 Level AA

---

## 1. Compliance Matrix

| Checkpoint | Requirement | Status (Pass/Fail/Warn) | Observed Issue | Remediation Action |
| :--- | :--- | :---: | :--- | :--- |
| **1.4.3** | Contrast (Minimum) | [Pass/Fail] | Text contrast is 3.2:1 | Change text color to `slate-700` (5.8:1) |
| **2.1.1** | Keyboard Navigation | [Pass/Fail] | Modal traps focus properly | Retain focus management |
| **2.4.7** | Focus Visible | [Pass/Fail] | Missing focus ring on tab | Add `focus-visible:ring-2` |
| **4.1.2** | Name, Role, Value | [Pass/Fail] | Close button has no label | Add `aria-label="Close modal"` |
