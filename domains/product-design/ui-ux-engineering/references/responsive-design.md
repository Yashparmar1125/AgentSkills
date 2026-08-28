# Responsive Design & Mobile Ergonomics Guide

## 1. Breakpoint Strategy
- **Mobile (`< 640px`)**: Single-column layout (`grid-cols-1`), mobile card stacks, bottom navigation bars, full-width modal sheets.
- **Tablet (`640px - 1024px`)**: 2-column layout (`sm:grid-cols-2`), compact sidebars, multi-column forms.
- **Desktop (`1024px+`)**: Full persistent sidebar, multi-column dashboards (`lg:grid-cols-3` or `lg:grid-cols-4`), data tables with sticky headers.

## 2. Touch Ergonomics
- Minimum interactive target size: **44px $\times$ 44px** (iOS HIG / Android Material standard).
- Primary actions placed in the natural "thumb zone" at the bottom third of mobile screens.
