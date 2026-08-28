# Forms & Form Ergonomics Guide

## 1. High-Conversion Form Patterns
- **Single-Column Alignment**: Stack form labels above inputs for fastest vertical scanning.
- **Inline Validation Timing**:
  - Validate on blur for required fields.
  - Validate eagerly during typing *only after* an initial error was shown.
  - Avoid noisy validation on the first keystroke.
- **Accessible Error Linking**: Always link inputs to error copy via `aria-describedby="field-error-id"`.

## 2. Preventing Duplicate Submissions
- Disable submit buttons immediately upon click and render an inline loading spinner.
- Re-enable buttons with error banners if the API returns a failure.
