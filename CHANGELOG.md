# Changelog - JLDN Todo Schema Specification

All notable changes to the JLDN Todo Schema Specification will be documented in this file.

The versioning follows the [JLDN Generational Versioning Schema](https://github.com/JLDesignNetwork/Generational-Versioning-Schema) format (`[YYMM].[SUBVERSION].[REVISION]-[TAG]`).

---

## Generation 2608

### 2608.2.0-s (2026-08-03) - Stable Release

**Major Release introducing the 11-State Task Matrix, Review vs. Audit phase distinction, and standard `[STATE]-[PHASE]` syntax.**

#### Added
- **11-State Modular Task Matrix:** Formally codified `pending`, `in-progress`, `pending-review`, `in-progress-review`, `pending-audit`, `in-progress-audit`, `pending-refactor`, `in-progress-refactor`, `completed`, `blocked`, and `deprecated`.
- **Review vs. Audit Phase Distinction:**
  - `review`: Surface-level inspection focusing on presentation, formatting, aesthetic flair, and initial appeal.
  - `audit`: In-depth, semantic, and structural analysis focusing on core mechanics, math balance, edge cases, exploits, and loopholes.
- **`[STATE]-[PHASE]` Syntax Standard:** Enforced strict prefix state + suffix phase naming format.
- **Updated Validation Regular Expression:** Codified regex `^(pending|in-progress|pending-review|in-progress-review|pending-audit|in-progress-audit|pending-refactor|in-progress-refactor|completed|blocked|deprecated)$`.

---

### 2608.1.0-s (2026-08-03) - Stable Release

**Initial Stable Release of the official JLDN Todo Schema Specification.**

#### Added
- **Core Document-Bound Architecture:** Established rules for storing structured task lists directly inside Markdown JSON frontmatter (`todo` array).
- **Task Object Schema Definition:** Specified `id`, `section`, `title`, `status`, and `details` fields.
