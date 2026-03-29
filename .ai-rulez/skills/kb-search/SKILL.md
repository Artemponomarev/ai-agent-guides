---
priority: high
description: "Use Dora to search the AI agent guides knowledge base before answering platform, skills, tools, or installation questions."
---

# KB Search

Use this skill when the task is about understanding AI agent platforms, skills marketplaces, installation methods, or safety considerations.

## Goal

Answer from the AI agent guides knowledge base first, using Dora as the primary retrieval tool.

## Retrieval Order

1. Search `guides/` with Dora.
2. Open the most relevant guide with Dora.
3. Fall back to browsing guide files directly if Dora returns no results.

## Dora Workflow

Use these commands from the repo root:

```bash
dora docs search "skills marketplace"
dora docs search "install agent"
dora docs search "safety"
dora docs show guides/skillhub-club.md --content
dora docs show guides/agency-agents.md --content
```

If the KB was just rebuilt and Dora looks stale:

```bash
dora index --skip-scip
```

## Search Strategy

- Start with terms from the user request:
  - `skills`
  - `marketplace`
  - `install`
  - `Claude Code`
  - `Cursor`
  - `safety`
  - `pricing`
  - `agents`
- Open the specific document returned by Dora rather than scanning many files manually.

## Important Notes

- `guides/` is the current source of truth.
- Dora may lock under parallel access in this workspace, so sequential searches are safer.
