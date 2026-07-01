```markdown
# sqlmap Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and workflows used in the `sqlmap` Python codebase. You'll learn the project's coding conventions, how to contribute optimizations or patches to core logic, and how to maintain consistency with settings and integrity tracking. The guide also covers typical testing patterns and provides handy commands for common tasks.

## Coding Conventions

- **File Naming:**  
  Files use camelCase naming, e.g., `coreSettings.py`, `controllerChecks.py`.

- **Import Style:**  
  Relative imports are preferred.  
  **Example:**
  ```python
  from .common import someFunction
  from ..core.settings import DEFAULTS
  ```

- **Export Style:**  
  Named exports are used; functions and classes are explicitly defined and imported as needed.  
  **Example:**
  ```python
  def runCheck():
      pass

  class SettingsManager:
      pass
  ```

- **Commit Messages:**  
  Freeform, typically concise (~23 characters), with or without prefixes.

## Workflows

### Core Settings Checks Update
**Trigger:** When you want to optimize or patch core logic related to settings and controller checks.  
**Command:** `/update-core-settings-checks`

1. Edit `lib/controller/checks.py` to modify or optimize controller check logic.
2. Edit `lib/core/settings.py` to update settings or configuration as needed.
3. Update `data/txt/sha256sums.txt` to reflect any changes for integrity or tracking.

**Example:**
```python
# lib/controller/checks.py
def newCheck():
    # Improved check logic
    pass

# lib/core/settings.py
NEW_SETTING = True

# After changes, update sha256sums.txt accordingly
```

---

### Core Settings Optimization
**Trigger:** When you want to optimize core functionality or refactor core modules.  
**Command:** `/optimize-core`

1. Edit one or more core files, such as:
   - `lib/core/convert.py`
   - `lib/core/dump.py`
   - `lib/core/common.py`
2. Edit `lib/core/settings.py` for any configuration or settings updates.
3. Update `data/txt/sha256sums.txt` to reflect all file changes.

**Example:**
```python
# lib/core/convert.py
def optimizedConvert():
    # Refactored conversion logic
    pass

# lib/core/settings.py
CONVERT_OPTIMIZED = True

# Update sha256sums.txt after making changes
```

## Testing Patterns

- **Framework:** Unknown (not explicitly detected).
- **File Pattern:** Test files are named with the pattern `*.test.*`.
  - Example: `convert.test.py`, `settings.test.py`
- **Style:** Tests are likely written in Python, matching the main codebase language.

## Commands

| Command                        | Purpose                                                            |
|--------------------------------|--------------------------------------------------------------------|
| /update-core-settings-checks   | Apply optimizations or patches to core settings and controller checks. |
| /optimize-core                 | Optimize or refactor core files and update settings/integrity tracking. |

```