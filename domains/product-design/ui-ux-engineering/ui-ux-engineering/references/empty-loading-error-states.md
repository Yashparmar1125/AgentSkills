# Empty, Loading & Error State Design Guide

## 1. Skeleton Loaders vs. Spinners
- **Never use full-screen blocking spinners** for standard data-fetching pages.
- Use animated pulse skeletons (`bg-slate-200 animate-pulse rounded-xl`) matching the exact visual footprint of cards, KPI blocks, and table rows to eliminate Cumulative Layout Shift (CLS).

## 2. Empty State Formulation
Every empty state MUST provide 3 elements:
1. **Contextual Icon & Title**: Explaining what is missing (e.g., "No Exams Found").
2. **Explanatory Subtitle**: Clarifying why it is empty (e.g., "Try adjusting your search criteria or create a new exam pack").
3. **Primary Action**: Direct button (e.g., "Create Exam Pack" or "Clear All Filters").

## 3. Error Resilience & Inline Retries
- Wrap widgets in Section Error Boundaries with a styled red-50 card, `FiAlertTriangle` icon, human-readable error description, and a "Retry" button.
