# Changelog - JLDN Todo Schema Specification

All notable changes to the JLDN Todo Schema Specification will be documented in this file.

The versioning follows the [JLDN Generational Versioning Schema](https://github.com/JLDesignNetwork/Generational-Versioning-Schema) format (`[YYMM].[SUBVERSION].[REVISION]-[TAG]`).

---

## Generation 2608

### 2608.1.0-s (2026-08-03) - Stable Release

**Initial Stable Release of the official JLDN Todo Schema Specification.**

#### Added
- **Core Document-Bound Architecture:** Established rules for storing structured task lists directly inside Markdown JSON frontmatter (`todo` array).
- **Formalized 5 Task Lifecycle Stages:** Codified `pending`, `in-progress`, `completed`, `completed-pending-follow-up`, and `pending-refactor` stages.
- **Task Object Schema Definition:** Specified `id`, `section`, `title`, `status`, and `details` fields.
- **Validation Regular Expression:** Codified regex `^(pending|in-progress|completed|completed-pending-follow-up|pending-refactor)$` for automated CI/CD pipeline validation.
- **Workflow State Transition Diagram:** Modeled task progression from `pending` through review and refactor cycles.
