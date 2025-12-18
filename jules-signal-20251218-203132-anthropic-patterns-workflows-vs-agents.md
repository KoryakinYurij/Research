# Context
Anthropic Agentic Design Patterns (Community Formalization)

# Observation
The emergence of a canonical set of 7+ agentic "patterns" documented by the community based on official Anthropic documentation. A key architectural distinction is made between **Workflows** (where control flow is managed by code) and **Autonomous Agents** (where control flow is determined by the LLM).

# Reason
As the complexity of agentic systems grew, there was a need to formalize recurring architectural solutions. The distinction between 'Workflows' and 'Agents' allows developers to more precisely choose the degree of LLM autonomy, instead of a binary 'agent/not an agent' approach. This solves the problem of excessive or insufficient control over the LLM.

# Implication
Reduced cognitive load when designing agentic systems. Instead of inventing their own architectures, developers can now use a ready-made, proven "vocabulary" of patterns. This speeds up development and makes systems more predictable and maintainable. The trend towards hybrid systems is strengthening, where some tasks are solved by strictly defined 'Workflows' and others by flexible 'Autonomous Agents'.

# Sources
- [Community-Sourced GitHub Repository of Anthropic Patterns](https://github.com/ThibautMelen/agentic-ai-systems)
- [Original Anthropic Engineering Blog Post](https://www.anthropic.com/engineering/building-effective-agents)
