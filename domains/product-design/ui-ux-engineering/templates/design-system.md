# Design System Specification Template

## 1. Design Tokens Dictionary
```json
{
  "color": {
    "brand": { "primary": "#4f46e5", "secondary": "#6366f1" },
    "surface": { "canvas": "#f8fafc", "card": "#ffffff", "subtle": "#f1f5f9" },
    "text": { "primary": "#0f172a", "secondary": "#475569", "muted": "#94a3b8" },
    "semantic": {
      "success": "#10b981", "warning": "#f59e0b", "danger": "#ef4444", "info": "#0ea5e9"
    }
  },
  "radius": { "sm": "4px", "md": "8px", "lg": "12px", "xl": "16px", "2xl": "24px" },
  "spacing": { "grid": "4px", "unit": "8px" }
}
```

## 2. Global Component Standards
- Standard Button Variants: `primary`, `secondary`, `danger`, `ghost`, `link`.
- Standard Input States: `default`, `focused`, `invalid`, `disabled`, `loading`.
