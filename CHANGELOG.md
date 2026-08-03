# Changelog - JLDN Todo Schema Specification

All notable changes to the JLDN Todo Schema Specification will be documented in this file.

The versioning follows the [JLDN Generational Versioning Schema](https://github.com/JLDesignNetwork/Generational-Versioning-Schema) format (`[YYMM].[SUBVERSION].[REVISION]-[TAG]`).

---

## Generation 2608

### 2608.4.0-s (2026-08-03) - Stable Release

**Public Alpha release applying Round 1 Red Team Audit fixes: Unblock Recovery Pathway, `reason` & `owner` properties, Sub-Task Dot Notation, and Trivial Fast-Track vs. Complex Audit rules.**

#### Added
- **Unblock Recovery Pathway:** Codified unblock recovery transitions allowing `blocked` tasks to resume their exact previous active state immediately upon blocker resolution.
- **`reason` Property:** Added optional `"reason"` string metadata property to document root causes for `blocked` and `deprecated` tasks.
- **`owner` Property:** Added optional `"owner"` string property to claim task ownership and prevent multi-agent execution collisions.
- **Sub-Task Dot Notation (`TODO-01.1`):** Codified sub-task hierarchy branching for multi-issue audit findings, requiring child sub-task resolution before parent completion.
- **Trivial Fast-Track vs. Complex Audit Rules:** Permitted trivial typo/formatting tasks to fast-track directly from `in-progress` to `completed`, while enforcing mandatory audit/review loops for structural changes.

---

### 2608.3.0-s (2026-08-03) - Stable Release

**Major Specification Update introducing the Colon-Delimited `[STATE]:[PHASE]` Syntax Standard.**

#### Added
- **Colon-Delimited `[STATE]:[PHASE]` Syntax:** Replaced hyphenated slugs with colon delimiters (`pending:review`, `in-progress:review`, `pending:audit`, `in-progress:audit`, `pending:refactor`, `in-progress:refactor`).
- **Updated Validation Regular Expression:** Codified regex `^(pending|in-progress|pending:review|in-progress:review|pending:audit|in-progress:audit|pending:refactor|in-progress:refactor|completed|blocked|deprecated)$`.

---

### 2608.2.0-s (2026-08-03) - Stable Release

**Major Release introducing the 11-State Task Matrix and Review vs. Audit phase distinction.**

#### Added
- **11-State Modular Task Matrix:** Formally codified `pending`, `in-progress`, `pending-review`, `in-progress-review`, `pending-audit`, `in-progress-audit`, `pending-refactor`, `in-progress-refactor`, `completed`, `blocked`, and `deprecated`.
- **Review vs. Audit Phase Distinction:** `review` (surface presentation/flair) vs. `audit` (deep mechanical analysis & loopholes).

---

### 2608.1.0-s (2026-08-03) - Stable Release

**Initial Stable Release of the official JLDN Todo Schema Specification.**

#### Added
- **Core Document-Bound Architecture:** Storing task lists inside Markdown JSON frontmatter (`todo` array).
- **Task Object Schema Definition:** Specified `id`, `section`, `title`, `status`, and `details` fields.
