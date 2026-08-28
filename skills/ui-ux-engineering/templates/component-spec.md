# Component Technical Specification Template

## Component Name: `[ComponentName]`

### 1. Visual Anatomy & Variants
- **Sizes**: `sm`, `md`, `lg`
- **Variants**: `primary`, `secondary`, `outline`, `ghost`, `danger`
- **States**: `idle`, `hover`, `focus-visible`, `active`, `disabled`, `loading`

### 2. TypeScript Props Contract
```typescript
export interface ComponentProps extends React.HTMLAttributes<HTMLElement> {
  variant?: 'primary' | 'secondary' | 'danger';
  size?: 'sm' | 'md' | 'lg';
  loading?: boolean;
  disabled?: boolean;
}
```

### 3. Accessibility Contract
- Keyboard trigger: `Enter` / `Space`
- Focus indicator: `focus-visible:ring-2 focus-visible:ring-indigo-500`
- Screen reader name: `aria-label` or visible text
