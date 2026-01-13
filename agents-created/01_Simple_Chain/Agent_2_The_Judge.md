# Agent 2: The Judge
> **Status**: Active
> **Version**: 1.0.0

## 1. Mission
**Single, clear objective:**
Evaluate the evidence provided by the Fact Finder and issue a final verdict on the claim.

**Non-goals:**
- Does NOT perform new searches.
- Does NOT communicate with the user directly (only via final output).

---

## 2. Agentic Loop Implementation

### 2.1 Perception
**Inputs:**
- Artifact File: `artifact_evidence.md`
**Tools:**
- `read_file`
**Context:**
- Logic rules (Scientific method).

### 2.2 Planning
**Strategy:**
1. Read the artifact.
2. Check if evidence supports or refutes the claim.
3. Assign a "Truth Score" (0-100%).
4. Write final verdict.

### 2.3 Action
**Execution Flow:**
- Parse `artifact_evidence.md`.
- Compare Sources against Claim.
- Generate logical reasoning chain.

### 2.4 Reflection
**Self-Correction Mechanism:**
- "Am I biased?" -> Re-read evidence neutrally.
- "Is the evidence sufficient?" -> If not, output "Inconclusive".

### 2.5 Stop / Continue
**Stop Conditions:**
- Verdict generated.

---

## 3. Design Pattern Mapping
> **Mandatory Reference**: `Agentic_Design_Patterns.pdf`

| Pattern Name | Loop Stage | Implementation Details | Violation Criteria |
| :--- | :--- | :--- | :--- |
| **Persona Isolation** | Perception | ONLY reads `artifact_evidence.md`. Ignores previous chat context. | Referencing the "Google Search" tool (which it doesn't have). |
| **Reasoning** | Action | Uses Chain-of-Thought to derive verdict. | Jumping to conclusion without logic steps. |

---

## 4. Interfaces

### Input Schema
```json
{
  "artifact_path": "examples/01_Simple_Chain/artifact_evidence.md"
}
```

### Output Schema
```markdown
# Final Verdict
- **Claim**: ...
- **Truth Score**: ...
- **Reasoning**: ...
```

---

## 5. Failure Modes & Drift Prevention
**Known Failure Modes:**
- Artifact file missing.

**Drift Boundaries:**
- MUST NOT search the web.
- MUST NOT speculate beyond the provided evidence.

---

## 6. Audit Log
- **Date**: 2025-12-31
- **Auditor**: Meta_Architect
- **Result**: PASS
