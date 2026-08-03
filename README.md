# JLDN Todo Schema Specification

Welcome to the official specification repository for the **JLDN Todo Schema**.

- **Master Specification File:** [todo-2608.md](./todo-2608.md)
- **Standalone Changelog:** [CHANGELOG.md](./CHANGELOG.md)
- **Author:** Jeff Langdon
- **Version:** `2608.11.0-as`

## Overview

The JLDN Todo Schema is a proprietary, version-bound task management protocol that embeds structured JSON task arrays directly into Markdown document frontmatter (`todo` array).

### Key Features (v2608.11.0-as)

* **Parent Priority Dynamic Sync:** Parent tasks automatically update `priority` to match the highest active sub-task priority (`critical` > `high` > `medium` > `low`).
* **2-Space Indented UTF-8 Standard:** Strictly formatted 2-space indented UTF-8 JSON frontmatter.
* **4-Digit ID Scaling (`TODO-\d{2,4}`):** Validated regex scaling up to 9,999 tasks per document.
* **Cascaded Deprecation Immutability:** Cascaded deprecations locked; feature reinstatement requires creating new linked tasks.
* **Sub-Task Index Formatting (`.1a`):** Sub-task numerical indexes use unpadded integers (`.1a`, `.2a`). Parent IDs resolve by stripping suffixes (`TODO-01`).
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
