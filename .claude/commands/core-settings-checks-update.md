---
name: core-settings-checks-update
description: Workflow command scaffold for core-settings-checks-update in sqlmap.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /core-settings-checks-update

Use this workflow when working on **core-settings-checks-update** in `sqlmap`.

## Goal

Apply minor optimizations or patches involving core settings and controller checks.

## Common Files

- `lib/controller/checks.py`
- `lib/core/settings.py`
- `data/txt/sha256sums.txt`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit lib/controller/checks.py for logic changes or optimizations
- Edit lib/core/settings.py to update settings or configuration
- Update data/txt/sha256sums.txt (possibly for integrity or tracking changes)

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.