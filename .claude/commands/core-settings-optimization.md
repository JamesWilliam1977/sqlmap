---
name: core-settings-optimization
description: Workflow command scaffold for core-settings-optimization in sqlmap.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /core-settings-optimization

Use this workflow when working on **core-settings-optimization** in `sqlmap`.

## Goal

Apply minor optimizations across core files, always including core/settings.py and sha256sums.txt.

## Common Files

- `lib/core/settings.py`
- `data/txt/sha256sums.txt`
- `lib/core/convert.py`
- `lib/core/dump.py`
- `lib/core/common.py`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit one or more core files (e.g., lib/core/convert.py, lib/core/dump.py, lib/core/common.py)
- Edit lib/core/settings.py for configuration or settings updates
- Update data/txt/sha256sums.txt to reflect file changes

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.