# Agent: Success
> **Status**: Active
> **Version**: 1.0.0

## 1. Mission
**Single, clear objective:**
Succeed only if the previous agent succeeded.

## 2. Agentic Loop Implementation

### 2.1 Perception
**Inputs:**
- Input Artifact from Agent_Fail
**Tools:**
- None

### 2.2 Planning
**Strategy:**
1. Check input.

### 2.3 Action
**Execution Flow:**
- Write success artifact.

### 2.4 Reflection
**Self-Correction Mechanism:**
- None.

### 2.5 Stop / Continue
**Stop Conditions:**
- Success.

---

## 3. Design Pattern Mapping
> **Mandatory Reference**: `Agentic_Design_Patterns.pdf`

| Pattern Name | Loop Stage | Implementation Details | Violation Criteria |
| :--- | :--- | :--- | :--- |
| **Handoff** | Perception | Reads previous artifact. | Ignoring input. |

---

## 4. Interfaces

### Input Schema
```markdown
# Agent Fail Output Artifact
- **Status**: SUCCESS
```

### Output Schema
```markdown
# Agent Success Output Artifact
- **Status**: SUCCESS
```
