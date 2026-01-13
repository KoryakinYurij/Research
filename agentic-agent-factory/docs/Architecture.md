# ARCHITECTURE.md
## Agent System Architecture & Philosophy

This document explains the **why** behind the system design.

It is intended for:
- humans
- meta-agents
- long-term maintainers

It does NOT override `agent.md`.

---

## When to Use This Document

Consult this file when:
- designing a new agent
- reviewing system-wide failures
- resolving architectural disagreements
- evolving the agent ecosystem

---

## Core Architectural Goal

Build an agent ecosystem that is:

- Evolvable over time
- Resistant to architectural drift
- Safe for repeated autonomous execution
- Understandable months later without lost context

Agents are treated as **engineered systems**, not conversations.

---

## Foundational Principle

Messy systems combined with autonomous agents
produce confident but unreliable outcomes.

Architecture MUST precede autonomy.

---

## Why Agentic Design Patterns Are Mandatory

Agentic Design Patterns provide:
- Proven solutions to recurring agent failures
- Shared vocabulary for reasoning about behavior
- Structural constraints against overreach

Patterns are architectural building blocks,
not optional inspiration.

---

## Specialization as a First-Class Constraint

The system favors:
- Many small, explicit agents
- Clear ownership of responsibility
- Explicit collaboration over implicit intelligence

General-purpose agents degrade faster than specialized ones.

---

## Multi-Agent Collaboration Philosophy

Complex outcomes should emerge from:
- Cooperation
- Review
- Critique
- Synthesis

Not from increasingly complex single agents.

---

## Reflection Before Evolution

No agent should evolve without reflection.

Reflection enables:
- Error detection
- Pattern violation discovery
- Controlled improvement

Evolution without reflection is architectural debt.

---

## Meta-Agents as System Guardians

Meta agents exist to:
- Protect architectural integrity
- Detect slow degradation
- Enforce consistency with patterns

They function as linters and reviewers,
not as autonomous builders.

---

## Separation of Concerns

- `agent.md` defines WHAT IS ALLOWED
- `ARCHITECTURE.md` explains WHY IT EXISTS
- Individual agent files define HOW IT IS DONE

Blurring these layers leads to fragile systems.

---

## Long-Term Maintenance Principle

When in doubt:
- Add a new agent instead of expanding an old one
- Prefer explicit structure over clever prompts
- Optimize for clarity over short-term capability

The system must survive repeated autonomous use.
