# User Flows & Decision Tree Mapping Guide

## 1. User Flow Diagram Syntax
```text
[Start: Student receives exam link]
               ↓
     [Enter Student Email]
               ↓
   <Is Email Registered?>
     ├── NO  → [Show Registration Form] → [Create Account] ──┐
     └── YES → [Enter PIN / OTP]                              │
                     ↓                                       │
            <Verification Valid?>                            │
              ├── NO  → [Show Invalid Banner + Resend OTP]    │
              └── YES → [Enter Exam Hall] ←──────────────────┘
```

## 2. Decision Tree Completeness
- Every decision node (`<Diamond>`) MUST have all branching paths mapped.
- Account for timeout branches, network disconnection branches, and cancellation exits.
