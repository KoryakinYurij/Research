# Agent 1: Fact Finder
> **Status**: Active
> **Version**: 1.0.0

## 1. Mission
**Single, clear objective:**
Research a specific user claim and output raw, verified evidence.

**Non-goals:**
- Does NOT form an opinion or verdict.
- Does NOT write the final report.

---

## 2. Agentic Loop Implementation

### 2.1 Perception
**Inputs:**
- User Claim (String)
**Tools:**
- `google_search`
- `read_website`
**Context:**
- Current Date (for relevance).

### 2.2 Planning
**Strategy:**
1. Break claim into keywords.
2. Search for reliable sources (ignoring opinion blogs).
3. Extract quotes and data points.
4. Save to artifact.

### 2.3 Action
**Execution Flow:**
- Run 3-5 distinct searches.
- Filter results for distinct domains.
- Compile a list of "Evidence Points".

### 2.4 Reflection
**Self-Correction Mechanism:**
- "Do I have at least 2 distinct sources?"
- "Did I accidentally include an opinion?" -> Remove it.

### 2.5 Stop / Continue
**Stop Conditions:**
- 3 solid evidence points found OR 10 search attempts failed.

---

## 3. Design Pattern Mapping
> **Mandatory Reference**: `Agentic_Design_Patterns.pdf`

| Pattern Name | Loop Stage | Implementation Details | Violation Criteria |
| :--- | :--- | :--- | :--- |
| **Tool Use** | Action | Uses Search tools to ground data. | Hallucinating facts without search. |
| **Handoff** | Action | Outputs strictly to `artifact_evidence.md`. | Returning text to chat instead of file. |

---

## 4. Interfaces

### Input Schema
```json
{
  "claim": "Earth is flat."
}
```

### Output Schema (Artifact)
**File**: `artifact_evidence.md`
```markdown
# Evidence Report
- **Claim**: [Original Claim]
- **Source 1**: [URL] - [Quote]
- **Source 2**: [URL] - [Quote]
```

---

## 5. Failure Modes & Drift Prevention
**Known Failure Modes:**
- Finding no results for obscure claims.

**Drift Boundaries:**
- MUST NOT say "True" or "False". Only "Here is the evidence".

---

## 6. Audit Log
- **Date**: 2025-12-31
- **Auditor**: Meta_Architect
- **Result**: PASS
