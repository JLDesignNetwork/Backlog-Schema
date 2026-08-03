# JLDN Todo Schema Specification

Welcome to the official specification repository for the **JLDN Todo Schema**.

- **Master Specification File:** [todo-2608.md](./todo-2608.md)
- **Standalone Changelog:** [CHANGELOG.md](./CHANGELOG.md)
- **Author:** Jeff Langdon
- **Version:** `2608.13.0-as`

## Overview

The JLDN Todo Schema is a proprietary, version-bound task management protocol that embeds structured JSON task arrays directly into Markdown document frontmatter (`todo` array).

### Key Features (v2608.13.0-as)

* **Acyclic Prerequisite DAG Rule:** `prerequisite` chains MUST form a directed acyclic graph (prohibiting circular execution deadlocks).
* **Self-Reference Prohibition:** Self-referential IDs in `child_of`, `relates_to`, or `prerequisite` are strictly invalid.
* **Terminal Prerequisite Satisfaction:** Prerequisites are satisfied when a task reaches ANY terminal state (`completed` or `deprecated`).
* **Formal Priority Rank Order:** Strict 4-level hierarchy: `critical` (Rank 4) > `high` (Rank 3) > `medium` (Rank 2) > `low` (Rank 1).
* **`prerequisite` Execution Key:** Enforces explicit task execution gating (`"prerequisite": "TODO-01.1a"`) for parallel agent workflows.
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

**Priority Regex & Rank Order:**
```regex
^(critical|high|medium|low)$
```
* **Rank 4:** `critical`
* **Rank 3:** `high`
* **Rank 2:** `medium`
* **Rank 1:** `low`

**ID Regex:**
```regex
^TODO-\d{2,4}(\.\d+[a-z])?$
```

## License & Attribution

Designed and maintained by Jeff Langdon / JL Design Network. All rights reserved.
