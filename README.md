# Project 5: Comparative Agent Harness Study
## Claude Code vs VS Code GPT

**Objective**: Give the same low-stakes assignment to two different AI harnesses. Map observations to the six-part framework and identify implementation differences while recognizing the common underlying shape.

> **Note:** Cowork and ChatGPT Work were optional in the assignment and were never tested (unfilled templates moved to `observations/not-used/`). For this study, Claude Code was compared with the installed VS Code GPT extension (`vscode-chat-gpt` by ikasann-self).

### Evidence status — two different kinds, do not conflate

| Comparison | Status |
|---|---|
| Claude Code vs VS Code GPT extension | **Tested by Claude Code** — real tool calls, files created and read back to verify (Test 1: `claude-code-observations.md`; Test 2: `claude-code-test/agent-test-observations.md`) |
| Plain ChatGPT chatbot conversation | **Manually observed by the human**, not tool-verified, not yet added — will get its own cited section later, and is not "Harness B" |

### The Six Concepts

- **Heartbeat**: How the system signals life / maintains presence / keeps cycles running
- **Reach**: The scope and extent of what the system can act on or access
- **Loop**: The feedback and iteration cycles that drive execution
- **Spine**: The core structural framework that everything hangs on
- **Gate**: Entry points, permission checks, and access controls
- **Body**: The actual substance/implementation of the work

### Harnesses Tested

**Harness A — Claude Code**

Claude Code directly created the test folder/files and verified the result using filesystem tools. Tested twice:
- **Test 1**: simple create + write (`project5-output/`, `claude-code-observations.md`)
- **Test 2**: plan → execute → verify → correct (`claude-code-test/`, `claude-code-test/agent-test-observations.md`)

**Harness B — VS Code GPT**

The `vscode-chat-gpt` extension generated GPT assistance but did not create the requested local files. The human remained responsible for the filesystem operation. Evidence: `chatgpt-test-output/` stayed empty after the request.

**Not Harness B — plain ChatGPT chatbot**

A plain ChatGPT chatbot conversation is a separate reference comparison the human ran manually, outside this tool. It is not tool-verified and is not yet added to `comparison.md`; when it is, it will be clearly cited as human-observed, not tool-tested.

### Project Structure

```text
project_5/
├── README.md
├── assignment.md
├── claude-code-observations.md        ← Test 1 narration (Claude Code)
├── comparison.md
├── EXECUTION_GUIDE.md
├── observations/
│   ├── framework.md                   ← generic unfilled template (Cowork/ChatGPT Work), kept for reference
│   └── not-used/
│       ├── README.md                  ← why these are unused
│       ├── cowork-run.md              ← unfilled, Cowork never tested
│       └── chatgpt-work-run.md        ← unfilled, ChatGPT Work never tested
├── project5-output/                   ← Test 1 deliverables (Claude Code)
│   ├── hello.txt
│   └── notes.txt
├── chatgpt-test-output/               ← Test 1 (VS Code GPT) — stayed empty, that's the evidence
├── claude-code-test/                  ← Test 2: plan→execute→verify→correct (Claude Code only)
│   ├── agent-test-observations.md
│   └── agent-test-output/
│       ├── task-plan.md
│       ├── hello.txt
│       └── notes.md
└── Project_5_Summary.docx             ← not regenerated this pass; rebuilt separately
```
