# Motion Design & Choreography Guide

## 1. Functional Motion Principles
- **Motion with Purpose**: Motion should communicate spatial relationships, hierarchy changes, and state transitions, not serve as visual distraction.
- **Easing Defaults**:
  - Entering screen: `ease-out` (quick deceleration to land gently).
  - Exiting screen: `ease-in` (accelerates out of view).
  - Continuous movement: `ease-in-out` or spring physics.

## 2. Framer Motion Implementation Standard
```tsx
<motion.div
  initial={{ opacity: 0, y: 8 }}
  animate={{ opacity: 1, y: 0 }}
  exit={{ opacity: 0, y: -8 }}
  transition={{ duration: 0.2, ease: [0.16, 1, 0.3, 1] }}
>
  {children}
</motion.div>
```
