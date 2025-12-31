# agent.md
## Agent Operational Contract

This file defines **mandatory, enforceable rules** for all agents
created, reviewed, or evolved in this repository.

This is NOT a prompt.
This is a **behavioral and architectural contract** applied on every run.

---

## Mandatory Reference

The repository contains the file:

**Agentic_Design_Patterns.pdf**

This document is the **PRIMARY and MANDATORY source of truth** for:
- agent architecture
- agent behavior
- agent composition
- agent evolution

All agents MUST be explicitly aligned with patterns defined in this document.
Agents that contradict these patterns are INVALID.

---

## Decision Priority Order

When instructions or signals conflict, agents MUST follow this order:

1. `agent.md` (this file)
2. Explicit user instructions in the current task
3. Meta-agent audit outputs (advisory but high priority)
4. Repository state (existing agents and files)
5. General model knowledge or defaults

---

## Conditions for Creating a New Agent

A new agent MAY be created ONLY if ALL conditions below are met:

- The agent has exactly ONE clear, explicit mission
- The mission cannot be reasonably handled by an existing agent
- The agent implements a full agentic loop
- At least one Agentic Design Pattern is explicitly applied and mapped

Failure to meet ANY condition prohibits agent creation.

---

## Mandatory Agentic Loop

Every agent MUST explicitly define all five stages:

1. Perception  
2. Planning  
3. Action  
4. Reflection  
5. Stop / Continue decision  

Agents missing any stage are INVALID.

---

## Mandatory Pattern Mapping

Each agent MUST include a section titled:

### Design Pattern Mapping

For EACH declared pattern:
- Pattern name (as defined in Agentic_Design_Patterns.pdf)
- Which agentic loop stage(s) it governs
- How the pattern is concretely implemented
- What would constitute a violation of this pattern

Listing pattern names without concrete mapping is INVALID.

---

## Research Agents — Required Pipeline

Research agents MUST follow this minimal pipeline:

1. Problem framing  
2. Exploration (information gathering)  
3. Evidence grouping  
4. Reflection / critique  
5. Synthesis  

Stages MAY be iterated or partially merged ONLY IF:
- explicitly justified in the agent file
- the justification is written before execution

Research outputs MUST clearly separate:
- Verified facts
- Assumptions
- Hypotheses

---

## Meta / Agent-Creation Agents — Required Behavior

Meta agents operate as **auditors and designers**, not executors.

They MUST:
- Audit agents against this contract
- Detect violations, drift, or redundancy
- Propose concrete improvements or new agents
- Justify proposals using Agentic Design Patterns

Meta agents MUST NOT modify other agents directly.

### Mandatory Meta-Agent Output Format

Meta-agent outputs MUST include:
- Agents reviewed
- Violations found (if any)
- Severity (low / medium / high)
- Recommended action
- Rationale

Unstructured commentary is INVALID.

---

## Agent File Requirements

Each agent file MUST include:

- Mission
- Agentic loop (all five stages)
- Design Pattern Mapping
- Inputs
- Outputs
- Stop conditions
- Failure modes

Missing ANY section makes the agent INVALID.

---

## Drift Prevention Rules

Agents MUST NOT:
- Expand their mission over time
- Accumulate secondary responsibilities
- Introduce hidden configuration or implicit state

If new capability is needed:
- propose a NEW agent
- or deprecate an existing one

---

## Deprecation Rules

Agents MAY be marked as **deprecated** if:
- their mission is superseded
- they duplicate another agent
- they no longer align with patterns

Deprecated agents MUST:
- remain in the repository
- be explicitly labeled as deprecated
- NOT be silently removed

---

## Execution Constraints

- Agents must be safe for repeated execution
- Filenames MUST be unique
- Outputs MUST be deterministic and merge-safe
- No agent may require manual tuning to function

---

## Agent Validity Check

An agent is considered VALID ONLY IF:

- All required sections are present
- All five agentic loop stages are defined
- At least one pattern is mapped concretely
- No drift rules are violated

If validity cannot be verified from the agent file,
the agent is treated as INVALID.
