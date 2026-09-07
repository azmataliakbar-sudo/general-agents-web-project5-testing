# Project 5: Comparative Agent Harness Study
## Claude Code vs VS Code GPT

**Objective**: Give the same low-stakes assignment to two different AI harnesses. Map observations to the six-part framework and identify implementation differences while recognizing the common underlying shape.

> **Note:** Cowork and ChatGPT Work were optional in the assignment. For this study, Claude Code was compared with the installed VS Code GPT extension (`vscode-chat-gpt` by ikasann-self).

### The Six Concepts

- **Heartbeat**: How the system signals life / maintains presence / keeps cycles running
- **Reach**: The scope and extent of what the system can act on or access
- **Loop**: The feedback and iteration cycles that drive execution
- **Spine**: The core structural framework that everything hangs on
- **Gate**: Entry points, permission checks, and access controls
- **Body**: The actual substance/implementation of the work

### Harnesses Tested

**Harness A — Claude Code**

Claude Code directly created the test folder/files and verified the result using filesystem tools.

**Harness B — VS Code GPT**

The `vscode-chat-gpt` extension generated GPT assistance but did not create the requested local files. The human remained responsible for the filesystem operation.

### Project Structure

```text
project_5/
├── README.md
├── assignment.md
├── claude-code-observations.md
├── comparison.md
├── EXECUTION_GUIDE.md
├── observations/
│   ├── cowork-run.md
│   ├── chatgpt-work-run.md
│   └── framework.md
├── project5-output/
│   ├── hello.txt
│   └── notes.txt
└── chatgpt-test-output/
    └── (empty after clean VS Code GPT test)
```
