# JLDN Todo Schema Specification

Welcome to the official specification repository for the **JLDN Todo Schema**.

- **Master Specification File:** [todo-2608.md](./todo-2608.md)
- **Standalone Changelog:** [CHANGELOG.md](./CHANGELOG.md)
- **Author:** Jeff Langdon
- **Version:** `2608.6.0-s`

## Overview

The JLDN Todo Schema is a proprietary, version-bound task management protocol that embeds structured JSON task arrays directly into Markdown document frontmatter (`todo` array).

### Key Features (v2608.6.0-s)

* **Sub-Task Letter Parts (`TODO-01.1a`):** Sub-task parts (`TODO-01.1a` through `TODO-01.1z`) are capped at 1 level of depth. Further splitting creates new top-level tasks linked via `"relates_to"`.
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
