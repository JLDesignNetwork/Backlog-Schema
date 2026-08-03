# JLDN Todo Schema Specification

Welcome to the official specification repository for the **JLDN Todo Schema**.

- **Master Specification File:** [todo-2608.md](./todo-2608.md)
- **Standalone Changelog:** [CHANGELOG.md](./CHANGELOG.md)
- **Author:** Jeff Langdon
- **Version:** `2608.8.0-s`

## Overview

The JLDN Todo Schema is a proprietary, version-bound task management protocol that embeds structured JSON task arrays directly into Markdown document frontmatter (`todo` array).

### Key Features (v2608.8.0-s)

* **`child_of` Vertical Ancestry:** Establishes immutable parent-child lineage (e.g. `"child_of": "TODO-01"`) guaranteeing an acyclic graph (DAG) while preserving parent task immutability.
* **`relates_to` Horizontal Association:** Provides lightweight correlation for independent tasks sharing mechanical context.
* **Sub-Task Letter Parts (`TODO-01.1a`):** Capped at single letters (`a`-`z`). Exceeding `'z'` forces new top-level tasks with `"child_of"`.
* **Strict Document Isolation:** Task lists are strictly local to their document and **CAN NEVER** reference external files.
* **Mandatory `priority` & Priority Escalation:** `priority` is required (`"critical"`, `"high"`, `"medium"`, `"low"`) and escalates upon audit discoveries.
* **Conditional `reason` Property:** Mandatory when status is `blocked` or `deprecated`.
* **11-State Modular Task Matrix (`[STATE]:[PHASE]`):**
  * **Initial Work:** `pending`, `in-progress`
  * **Surface Review:** `pending:review`, `in-progress:review`
  * **Deep Audit:** `pending:audit`, `in-progress:audit`
  * **Refactoring:** `pending:refactor`, `in-progress:refactor`
  * **Terminal & Control:** `completed`, `blocked`, `deprecated`

### Validation Regular Expression

```regex
^(pending|in-progress|pending:review|in-progress:review|pending:audit|in-progress:audit|pending:refactor|in-progress:refactor|completed|blocked|deprecated)$
```

## License & Attribution

Designed and maintained by Jeff Langdon / JL Design Network. All rights reserved.
