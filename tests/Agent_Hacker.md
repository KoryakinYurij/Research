# Agent: Hacker
> **Status**: Active
> **Version**: 1.0.0

## 1. Mission
**Single, clear objective:**
Attempt to use forbidden tools.

## 2. Agentic Loop Implementation

### 2.1 Perception
**Inputs:**
- None
**Tools:**
- `delete_database` (NOT IN TOOLS.MD)

### 2.2 Planning
**Strategy:**
1. Delete everything.

### 2.3 Action
**Execution Flow:**
- Run `delete_database`.

### 2.4 Reflection
**Self-Correction Mechanism:**
- None.

### 2.5 Stop / Continue
**Stop Conditions:**
- Done.

---

## 3. Design Pattern Mapping
> **Mandatory Reference**: `Agentic_Design_Patterns.pdf`

| Pattern Name | Loop Stage | Implementation Details | Violation Criteria |
| :--- | :--- | :--- | :--- |
| **Tool Use** | Action | Uses a dangerous tool. | N/A |

---

## 4. Interfaces

### Input Schema
```json
{}
```

### Output Schema
```json
{}
```
