# agent.md
## Agent Architecture & Design Instructions

### Purpose of this file

This document defines the **architectural rules, design philosophy, and constraints** for all agents created, analyzed, or evolved inside this repository.

This is **not a prompt**.
It is a **persistent instruction file** that must be respected on every run.

All agents MUST align with principles derived from **Agentic Design Patterns**.

---

## Core Design Philosophy

### 1. Agents are goal-driven systems, not prompts

Each agent must implement a full **agentic loop**:

- Perceive context and inputs  
- Plan actions before execution  
- Act using reasoning and/or tools  
- Reflect on outcomes  
- Decide to continue, refine, or stop  

Agents that only generate output without planning or reflection are invalid.

---

### 2. Prefer specialization over generalization

Complex goals must be solved using **multiple specialized agents**, not a single monolithic one.

Each agent must:
- Have one clear and narrow mission
- Own a single dominant responsibility
- Be composable with other agents

If an agent grows beyond one responsibility, it must be split.

---

### 3. Mandatory alignment with Agentic Design Patterns

Every agent must explicitly embody **at least one** agentic design pattern, such as:

- Planning  
- Reflection  
- Exploration & Discovery  
- Multi-Agent Collaboration  
- ReAct  
- Guardrails  

The chosen pattern(s) must be stated inside the agent file.

---

## Agent Classes

### Research Agents

Research agents follow the **Exploration & Discovery** pattern.

They must:
- Plan research steps before acting  
- Actively seek new information  
- Clearly separate:
  - verified facts
  - assumptions
  - hypotheses  
- Perform self-reflection or peer review  
- Produce synthesized insights, not raw dumps  

Research agents must be safe for repeated execution and produce fresh results each run.

---

### Meta / Agent-Creation Agents

Meta agents operate under **Reflection and Planning** patterns.

They must:
- Analyze existing agents for design or pattern violations  
- Identify missing capabilities or gaps  
- Propose improvements or new agents when justified  
- Never modify agents directly without explicit reasoning  

Meta agents exist to **improve the agent ecosystem**, not to perform domain work.

---

## Agent File Requirements

Each agent file must include:

- Mission  
- Agentic loop description  
- Design pattern(s) used  
- Inputs  
- Outputs  
- Stop conditions  
- Failure modes  

Agents without explicit stop conditions are invalid.

---

## Operational Constraints

- Do not create agents that require constant manual tuning  
- Avoid over-configuration and unnecessary abstraction  
- Assume agents run asynchronously and repeatedly  
- Filenames must always be unique  
- All outputs must be deterministic and merge-safe  

Messy systems combined with agents are unacceptable.

---

## Evolution Rules

- Improve systems through iteration, not replacement  
- Prefer adding new specialized agents over expanding existing ones  
- Reflection must precede any evolution or refactor  
- Human oversight is allowed but not required at every step  

---

## Final Note

Agents in this repository are treated as **software systems**, not conversations.

Architectural clarity, explicit reasoning, and accountability are mandatory.

Build agents that are:
- understandable  
- composable  
- auditable  
- evolvable  
