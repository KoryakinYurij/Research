# Agentic Design Toolkit

**Governance, Architecture, and Patterns for Scalable AI Agents.**

This repository serves as a **Meta-Framework** for building robust, maintainable, and SOTA-aligned Agentic Systems. It is designed for the "Engineering Phase" of AI (2025+), moving beyond prompt engineering to **architectural guarantees**.

## Core Philosophy
**Architecture > Autonomy.**
Autonomous agents without strict architecture degrade into unreliable chat bots. This toolkit enforces a "Contract-First" approach to ensure agents are composable, auditable, and drift-resistant.

## Key Components

### 1. [The Operational Contract (`Agents.md`)](./Agents.md)
The constitution of this ecosystem. Every agent must adhere to this strict behavioral contract.
- **Mandatory 5-Step Loop**: Perception, Planning, Action, Reflection, Stop.
- **Drift Prevention**: Strict rules against mission creep.
- **Meta-Agent Auditing**: Agents are reviewed by other agents.

### 2. [Architecture & Philosophy (`Architecture.md`)](./Architecture.md)
The "Why" behind the design.
- Specialization over Generalization.
- Reflection before Evolution.
- Meta-Agents as System Guardians.

### 3. [Agent Template (`TEMPLATE_AGENT.md`)](./TEMPLATE_AGENT.md)
A copy-pasteable scaffold to create new agents that are immediately compliant with the Operational Contract.

### 4. Mandatory Reference
This toolkit is grounded in the methodologies defined in:
**`Agentic_Design_Patterns.pdf`** (based on the work by Antonio Gulli).
*Concepts covered: Reflection, Planning, Multi-Agent Consensus, Model Context Protocol (MCP), Guardrails.*

## 🚀 Quick Start ("Ignition")

To start working, simply:
1.  Open **`JULES_SYSTEM_PROMPT.md`**.
2.  Copy the content.
3.  Paste it into the chat with Jules.
4.  Follow the prompt: Choose **Build Mode** or **Run Mode**.

## Workflow: Build vs. Run

### 🏗️ Build Mode (Architecting)
**Goal**: Create new agents.
1.  **Read `Agents.md`** & **`TOOLS.md`**.
2.  **Copy `TEMPLATE_AGENT.md`**.
3.  Define the Agent's Mission, Loop, and Tools.
4.  **Run Meta-Audit**: Use `Meta_Architect.md` to validate your new file.

### 🚀 Run Mode (Executing)
**Goal**: Solve a user problem.
1.  **Start with `Manager_Agent.md`**: Give it the User Goal.
2.  **Execute the Plan**: The Manager produces `artifact_project_plan.md`.
3.  **Run the Chain**: Manually (or via script) run each agent listed in the plan sequentially.
   - *Agent A* runs -> outputs `artifact_A.md`.
   - *Agent B* runs -> reads `artifact_A.md` -> outputs `artifact_B.md`.

## Reference Examples
To see these concepts in action, check the **Reference Implementations**:

### 1. The Meta-Auditor (`Meta_Architect.md`)
A self-policing agent designed to read *other* agent files and verify they comply with `Agents.md`. This is the "Linter" of the ecosystem.
- [View Meta_Architect](./Meta_Architect.md)

### 2. The "Hello World" Chain (`examples/01_Simple_Chain/`)
A practical demonstration of the **Artifact Handoff Protocol**.
1. **Agent A (Fact Finder)**: Searches and saves data to a file.
2. **Agent B (The Judge)**: Reads the file and issues a verdict.
- [View Example Chain](./examples/01_Simple_Chain/)

## Research & Review
For a detailed analysis of how this repository aligns with State-of-the-Art (SOTA) trends for late 2025, see [REVIEW_REPORT.md](./REVIEW_REPORT.md).
