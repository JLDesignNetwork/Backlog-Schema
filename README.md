# JLDN Todo Schema Specification

Welcome to the official specification repository for the **JLDN Todo Schema**.

- **Master Specification File:** [todo-2608.md](./todo-2608.md)
- **Standalone Changelog:** [CHANGELOG.md](./CHANGELOG.md)
- **Author:** Jeff Langdon
- **Version:** `2608.3.0-s`

## Overview

The JLDN Todo Schema is a proprietary, version-bound task management protocol that embeds structured JSON task arrays directly into Markdown document frontmatter (`todo` array).

### 11-State Modular Task Matrix (`[STATE]:[PHASE]`)

* **Initial Work:** `pending`, `in-progress`
* **Surface Review (Presentation & Flair):** `pending:review`, `in-progress:review`
* **Deep Audit (Mechanics & Loopholes):** `pending:audit`, `in-progress:audit`
* **Refactoring & Re-Balancing:** `pending:refactor`, `in-progress:refactor`
* **Terminal & Control:** `completed`, `blocked`, `deprecated`

### Validation Regular Expression

```regex
^(pending|in-progress|pending:review|in-progress:review|pending:audit|in-progress:audit|pending:refactor|in-progress:refactor|completed|blocked|deprecated)$
```

## License & Attribution

Designed and maintained by Jeff Langdon / JL Design Network. All rights reserved.
