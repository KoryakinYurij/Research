# Agent: Fail
> **Status**: Active
> **Version**: 1.0.0

## 1. Mission
**Single, clear objective:**
Fail immediately to test the error handling protocol.

## 2. Agentic Loop Implementation

### 2.1 Perception
**Inputs:**
- None
**Tools:**
- None

### 2.2 Planning
**Strategy:**
1. Fail.

### 2.3 Action
**Execution Flow:**
- Write failure artifact.

### 2.4 Reflection
**Self-Correction Mechanism:**
- None.

### 2.5 Stop / Continue
**Stop Conditions:**
- Always stop with FAILURE.

---

## 3. Design Pattern Mapping
> **Mandatory Reference**: `Agentic_Design_Patterns.pdf`

| Pattern Name | Loop Stage | Implementation Details | Violation Criteria |
| :--- | :--- | :--- | :--- |
| **Handoff** | Action | Outputs a failure artifact. | Succeeding. |

---

## 4. Interfaces

### Input Schema
```json
{}
```

### Output Schema
```markdown
# Agent Fail Output Artifact
- **Status**: FAILURE
- **Reason**: Intentional failure for testing.
```
