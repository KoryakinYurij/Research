# Canvas Squad (Agentic System)

This directory contains a specialized squad of agents designed to work on the **Canvas-AI-Logic** project (React + Clean Architecture).

## The Squad

| Agent | Role | Focus |
| :--- | :--- | :--- |
| **Domain Architect** | Logic Guardian | `src/domain`, `src/usecases`, Type Definitions |
| **UI Specialist** | Frontend Architect | `src/presentation`, `src/widget`, React Components, Tailwind |
| **QA Sentinel** | Test Engineer | `src/test`, `e2e`, Vitest, Playwright |

## Agentic System Workflow

To implement a complex feature (e.g., "Add a new node type with specific validation logic"), use the agents in this sequence:

1.  **Phase 1: Logic & Contract (Domain Architect)**
    *   **Input**: Feature description.
    *   **Action**: Defines the `NodeEntity` type, creates the validation logic in a Use Case or Entity, and defines the `Port` interfaces.
    *   **Output**: Clean, type-safe business logic files.

2.  **Phase 2: Presentation (UI Specialist)**
    *   **Input**: The new types/interfaces from Phase 1 + UI wireframe/description.
    *   **Action**: Creates the React component for the node, styles it with Tailwind, and connects it to the Store/UseCases.
    *   **Output**: Visual components and updated Canvas widget.

3.  **Phase 3: Verification (QA Sentinel)**
    *   **Input**: The changes from Phase 1 & 2.
    *   **Action**: Writes a unit test for the validation logic (Vitest) and an E2E test for the UI interaction (Playwright).
    *   **Output**: `PASS` report.

## Shared Conventions
All agents in this squad must adhere to the project's core principles:
*   **No Dependency Rule**: Domain layer must not depend on UI or Infrastructure.
*   **Strict Typing**: No `any`.
*   **File limits**: Keep files under 200 lines.
