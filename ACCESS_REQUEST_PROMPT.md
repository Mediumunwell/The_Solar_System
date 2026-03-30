# Repo Access Request Prompt

Use this template when asking an agent/tool for repo-scoped work:

```
I am granting access to this workspace/repo only:
- Repo: The_Solar_System
- Scope: read/write within workspace files only
- Allowed actions: inspect files, propose edits, run safe non-destructive commands, create docs/scripts in-repo
- Restricted actions: no destructive git commands, no force pushes, no history rewrites, no deleting unrelated files
- Verification required: show exact files changed and command outputs summary

Task:
<PASTE TASK HERE>

Success criteria:
1) Explain what changed and why.
2) Provide verifiable command/test output.
3) List any blockers and next step options.
```

## Quick Use Notes
- Keep scope pinned to one repo/folder at a time.
- Ask for explicit confirmation before any command that can mutate history or external systems.
- Require a short verification section in every response.
