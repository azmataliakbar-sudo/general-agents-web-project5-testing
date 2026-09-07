# Project 5 — One Task, Two Harnesses

## Task

Both harnesses were given the same low-stakes task: create `hello.txt` and `notes.txt` in the project test directory and complete the task.

## Harnesses

- **Harness A:** Claude Code
- **Harness B:** VS Code GPT extension (`vscode-chat-gpt` by ikasann-self)

## Six-Part Shape

| Part | Claude Code | VS Code GPT |
|---|---|---|
| **Heartbeat** | Discrete progress signals during tool execution. | Discrete GPT response. |
| **Reach** | Direct filesystem access; created and read project files. | No direct filesystem creation observed. |
| **Loop** | Create → write → verify executed autonomously. | No autonomous filesystem loop; human had to perform the file operation. |
| **Spine** | Maintained task sequence across tool calls. | Maintained the request/response context but did not execute a multi-step filesystem sequence. |
| **Gate** | Filesystem operation proceeded through available tool permissions. | Human was required to create/copy the files locally. |
| **Body** | Agent + filesystem tools (Bash/Write). | VS Code GPT code-generation utility. |

## Three Implementation Differences

### 1. Reach

Claude Code could directly reach the local filesystem and create the requested files. The VS Code GPT extension did not demonstrate direct filesystem access during the test.

### 2. Loop

Claude Code executed the complete create → write → verify sequence. VS Code GPT stopped at generating assistance, so the human had to perform the local file operation.

### 3. Gate

Claude Code's available tools allowed the task to proceed without the human manually creating the files. With VS Code GPT, the human remained the execution gate.

## Conclusion

The implementation differs substantially, but the same six-part shape remains visible underneath:

**Heartbeat → Reach → Loop → Spine → Gate → Body**

The comparison is therefore about the **harness and its capabilities**, not simply about which model produced the text.
