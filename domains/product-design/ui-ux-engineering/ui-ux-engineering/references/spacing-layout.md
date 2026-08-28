# Spacing, Layout & Grid Systems Guide

## 1. 8-Point Spacing Grid
| Spacing Token | Pixels | Tailwind Class | Common Usage |
| :--- | :--- | :--- | :--- |
| `0.5` | 2px | `gap-0.5` / `p-0.5` | Border offsets, tight badge padding |
| `1` | 4px | `gap-1` / `p-1` | Icon-to-text gap, input internal offsets |
| `2` | 8px | `gap-2` / `p-2` | Button padding, list item gaps |
| `3` | 12px | `gap-3` / `p-3` | Compact card padding, toolbar spacing |
| `4` | 16px | `gap-4` / `p-4` | Standard mobile padding, form field gaps |
| `6` | 24px | `gap-6` / `p-6` | Standard desktop card padding, widget gaps |
| `8` | 32px | `gap-8` / `p-8` | Section separators, grid container spacing |
| `12` | 48px | `gap-12` / `p-12`| Major page section spacing |

## 2. Container Max Widths
- Standard Application Shell: `max-w-7xl mx-auto px-4 sm:px-6 lg:px-8`.
- Focused Reader / Exam View: `max-w-4xl mx-auto`.
- Narrow Form / Auth Modal: `max-w-md w-full`.
