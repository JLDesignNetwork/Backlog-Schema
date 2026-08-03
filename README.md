# JLDN Todo Schema Specification

Welcome to the official specification repository for the **JLDN Todo Schema**.

- **Master Specification File:** [todo-2608.md](./todo-2608.md)
- **Standalone Changelog:** [CHANGELOG.md](./CHANGELOG.md)
- **Author:** Jeff Langdon
- **Version:** `2608.1.0-s`

## Overview

The JLDN Todo Schema is a proprietary, version-bound task management protocol that embeds structured JSON task arrays directly into Markdown document frontmatter (`todo` array).

### 5 Formalized Task Lifecycle Stages

1. `pending`: Initial state, task queued for execution.
2. `in-progress`: Task currently under active development.
3. `completed`: Task fully implemented, tested, and verified.
4. `completed-pending-follow-up`: Task completed but awaiting audit or review.
5. `pending-refactor`: Task flagged for refactoring or architectural optimization.

### Validation Regular Expression

```regex
^(pending|in-progress|completed|completed-pending-follow-up|pending-refactor)$
```

## License & Attribution

Designed and maintained by Jeff Langdon / JL Design Network. All rights reserved.
