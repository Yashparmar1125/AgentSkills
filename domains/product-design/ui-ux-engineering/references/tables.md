# Data Tables & List Ergonomics Guide

## 1. Enterprise Table Standards
- **Desktop**: Full `<table>` layout with sticky headers, explicit column widths, sortable columns, and hover highlights.
- **Mobile (< 640px)**: Hide full table (`hidden sm:block`) and render stacked card summaries (`sm:hidden`) to eliminate horizontal scroll fatigue.
- **Bulk Action Bar**: Floating bottom action bar with selection counters (`3 selected`), clear selection button, and batch action triggers.

## 2. Empty & Filter States in Tables
- If zero rows match active search/filters, render a centered empty state card with a "Reset Filters" action button instead of a bare blank table.
