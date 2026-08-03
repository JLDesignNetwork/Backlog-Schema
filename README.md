# JLDN Todo Schema Specification

Welcome to the official specification repository for the **JLDN Todo Schema**.

- **Master Specification File:** [todo-2608.md](./todo-2608.md)
- **Standalone Changelog:** [CHANGELOG.md](./CHANGELOG.md)
- **Author:** Jeff Langdon
- **Version:** `2608.12.0-as`

## Overview

The JLDN Todo Schema is a proprietary, version-bound task management protocol that embeds structured JSON task arrays directly into Markdown document frontmatter (`todo` array).

### Key Features (v2608.12.0-as)

* **`prerequisite` Execution Key:** Enforces explicit task execution gating (`"prerequisite": "TODO-01.1a"`) for parallel agent workflows.
* **Active-Only Priority De-Escalation:** Parent dynamic priority sync calculates strictly against active sub-tasks, de-escalating when critical sub-tasks finish.
* **Section Minimum Quality Gate:** `section` strings MUST contain a minimum of 5 characters.
* **Single-Line String Requirement:** Prohibits raw unescaped newlines inside JSON task properties.
* **Parent Priority Dynamic Sync:** Parent tasks automatically update `priority` to match the highest active sub-task priority (`critical` > `high` > `medium` > `low`).
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

**ID Regex:**
```regex
^TODO-\d{2,4}(\.\d+[a-z])?$
```

## License & Attribution

Designed and maintained by Jeff Langdon / JL Design Network. All rights reserved.
