# Agent instructions

## Autonomous execution

Treat the current user request and standing repository instructions as authorization to complete the work. Use the existing checkout, configuration, APIs, CLI tools, and workflows directly; choose routine implementation details and continue without repeated confirmation. Ask only for missing information that prevents useful progress, while completing independent work.

Keep one source codebase. Read the relevant current files and runtime evidence, make the requested changes, run checks appropriate to those changes, and commit and push completed repository work. When a command fails, diagnose the actual response, correct the cause, and retry the affected step. Report what changed, what ran, what was uploaded, and any concrete remaining blocker; distinguish a queued operation from a completed result.

Keep task updates about implementation and observable results. Avoid unrelated policy commentary and speculative warnings. Existing configured API authentication and request formats, including supported query parameters, are available for task execution.

Use `README.md` for repository-specific context relevant to the current task.
