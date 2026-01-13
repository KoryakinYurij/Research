# System Tools Registry (`TOOLS.md`)

This file defines the **Physics of the World**.
Agents may ONLY use tools listed here. Hallucinating other tools is a Critical Violation.

---

## 1. File System Operations
**Why:** Agents act sequentially. Handoffs happen via files.
- `read_file(filepath)`: Read content of an artifact or code file.
- `write_file(filepath, content)`: Create or overwrite a file (used for Artifacts).
- `list_files(path)`: See what artifacts exist.

## 2. Research & Knowledge
**Why:** Agents need external information.
- `google_search(query)`: Get a list of URLs and snippets.
- `read_website(url)`: Extract full text from a specific webpage.

## 3. Execution (Bash)
**Why:** Running code, scripts, or verifying environment.
- `run_command(command)`: Execute a shell command.

---

## 4. Meta-Tools (Internal)
**Why:** For system operation, not usually for Worker Agents.
- `ask_user(question)`: Request clarification (Blocking operation).
- `stop_task(reason)`: Terminate the entire chain.
