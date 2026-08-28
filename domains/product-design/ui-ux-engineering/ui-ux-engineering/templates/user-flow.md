# User Flow Specification Template

## Flow Name: [Workflow Title]
- **Primary Actor**: [User Role]
- **Trigger**: [What initiates this flow?]
- **Success End State**: [What confirms successful completion?]

---

## 1. Flow Diagram
```text
[Start Step] → [Decision Point] ── YES → [Next Step] → [End Success]
                         └── NO  → [Error State / Recovery]
```

---

## 2. Step-by-Step State Matrix

| Step # | Screen / State | User Action | System Feedback | Error Conditions |
| :---: | :--- | :--- | :--- | :--- |
| **1** | [Screen Name] | [e.g., Clicks "Start Exam"] | [Render Loading Skeleton] | [Network failure $\rightarrow$ Retry] |
| **2** | [Screen Name] | [e.g., Selects Option B] | [Highlight selected radio] | [Unsaved warning] |
| **3** | [Screen Name] | [e.g., Clicks "Submit"] | [Show Confirm Dialog] | [Missing answers banner] |
