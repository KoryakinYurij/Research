# [Agent Name]
> **Status**: [Active / Deprecated]
> **Version**: 1.0.0

## 1. Mission
**Single, clear objective:**
[Describe the specific mission here. MUST be a single responsibility. Example: "Extract financial data from PDF invoices and return structured JSON."]

**Non-goals:**
- [List what this agent explicitly does NOT do.]

---

## 2. Agentic Loop Implementation

### 2.1 Perception
**Inputs:**
- [List inputs. Example: PDF file stream, User query string]
**Tools:**
- [List tools. Example: `read_pdf`, `ocr_scan`]
**Context:**
- [What context does it need? Example: Current date, Vendor list]

### 2.2 Planning
**Strategy:**
- [How does it break down the task? Example: 1. Validate file. 2. Extract text. 3. Parse fields. 4. Validate totals.]

### 2.3 Action
**Execution Flow:**
- [Describe the execution logic or step-by-step process.]

### 2.4 Reflection
**Self-Correction Mechanism:**
- [How does it verify its own work? Example: "Compare extracted Total against sum of Line Items."]
- [What happens on error? Example: "Retry with different OCR mode."]

### 2.5 Stop / Continue
**Stop Conditions:**
- [Success: Valid JSON generated.]
- [Failure: Unreadable file after 3 attempts.]

---

## 3. Design Pattern Mapping
> **Mandatory Reference**: `Agentic_Design_Patterns.pdf`

| Pattern Name | Loop Stage | Implementation Details | Violation Criteria |
| :--- | :--- | :--- | :--- |
| **[Example: Reflection]** | Reflection | Implements a "Critique-Revise" loop before final output. | Outputting without a validation step. |
| **[Example: Tool Use]** | Perception/Action | Uses specific OCR tools via MCP. | Hallucinating text instead of using the tool. |

---

## 4. Interfaces

### Input Schema
```json
{
  "key": "value_type"
}
```

### Output Schema
```json
{
  "key": "value_type"
}
```

---

## 5. Failure Modes & Drift Prevention
**Known Failure Modes:**
- [Example: Blurry images result in low confidence scores.]

**Drift Boundaries:**
- [Example: This agent MUST NOT attempt to *pay* the invoice, only *read* it.]

---

## 6. Audit Log
> Managed by Meta-Agents

- **Date:** [YYYY-MM-DD]
- **Auditor:** [Meta-Agent Name]
- **Result:** [Pass/Fail]
- **Notes:** [Comments]
