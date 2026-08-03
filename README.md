# JLDN Todo Schema Specification

Welcome to the official specification repository for the **JLDN Todo Schema**.

- **Master Specification File:** [todo-2608.md](./todo-2608.md)
- **Standalone Changelog:** [CHANGELOG.md](./CHANGELOG.md)
- **Author:** Jeff Langdon
- **Version:** `2608.10.0-as`

## Overview

The JLDN Todo Schema is a proprietary, version-bound task management protocol that embeds structured JSON task arrays directly into Markdown document frontmatter (`todo` array).

### Key Features (v2608.10.0-as)

* **Sub-Task Index Formatting (`.1a`):** Sub-task numerical indexes use unpadded integers (`.1a`, `.2a`). Parent IDs resolve by stripping suffixes (`TODO-01`).
* **Parent Deprecation Cascade:** Deprecating a parent task automatically cascades `deprecated` status to all active child sub-tasks.
* **Empty Array Validity (`"todo": []`):** Valid frontmatter representing zero active tasks.
* **Pre-Validation String Trimming:** Whitespace trimmed prior to regex and schema evaluation.
* **Parent-Child Blocker Propagation:** Parent tasks immediately transition to `blocked` when any active child task locks.
* **Strict Target Key Validation:** `child_of` and `relates_to` MUST reference valid, existing local task IDs.
* **11-State Modular Task Matrix (`[STATE]:[PHASE]`):**
  * **Initial Work:** `pending`, `in-progress`
  * **Surface Review:** `pending:review`, `in-progress:review`
  * **Deep Audit:** `pending:audit`, `in-progress:audit`
  * **Refactoring:** `pending:refactor`, `in-progress:refactor`
  * **Terminal & Control:** `completed`, `blocked`, `deprecated`

### Validation Regular Expressions

**Status Regex:**
```regex
^(pending|in-progress|pending:review|in-progress:review|pending:audit|in-progress:audit|pending:refactor|in-progress:refactor|completed|blocked|deprecated)$
```

**Priority Regex:**
```regex
^(critical|high|medium|low)$
```

## License & Attribution

Designed and maintained by Jeff Langdon / JL Design Network. All rights reserved.
