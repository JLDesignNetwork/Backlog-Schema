# Changelog - JLDN Todo Schema Specification

All notable changes to the JLDN Todo Schema Specification will be documented in this file.

The versioning follows the [JLDN Generational Versioning Schema](https://github.com/JLDesignNetwork/Generational-Versioning-Schema) format (`[YYMM].[SUBVERSION].[REVISION]-[TAG]`).

---

## Generation 2608

### 2608.6.0-s (2026-08-03) - Stable Release

**Public Alpha release applying Round 3 Red Team Audit fixes: Sub-Task Letter Parts (`TODO-01.1a` through `TODO-01.1z`), strict local document isolation, conditional `reason` requirement, and priority escalation rules.**

#### Added
- **Sub-Task Letter Parts (`TODO-01.1a`):** Codified sub-task letter parts (`TODO-01.1a` to `TODO-01.1z`) with a hard single-level cap. Prohibited sub-sub-task splitting; required creating new top-level tasks with `"relates_to"` when further breakdown is needed.
- **Strict Local Document Isolation for `relates_to`:** Codified that todo items are strictly document-bound and can never reference external files or contain todo data for other files.
- **Conditional `reason` Property:** Updated property type to Conditional (mandatory if `blocked` or `deprecated`; optional otherwise).
- **Priority Escalation Rules:** Codified mutable priority rules allowing immediate escalation to `critical` or `high` when deep audits uncover critical flaws.

---

### 2608.5.0-s (2026-08-03) - Stable Release

**Public Alpha release applying Round 2 Red Team Audit fixes: Mandatory `priority` property, `relates_to` relational linking key, parent completion on terminal child states, section heading resilience, and numeric ID parsing.**

#### Added
- **Mandatory `priority` Property:** Made `priority` a required property on all task objects.
- **`relates_to` Relational Linking Key:** Added optional `"relates_to"` property referencing prior local task IDs.
- **Immutable Completion Rule:** Formally prohibited re-opening `completed` tasks.

---

### 2608.4.0-s (2026-08-03) - Stable Release

**Public Alpha release applying Round 1 Red Team Audit fixes: Unblock Recovery Pathway, `reason` & `owner` properties, Sub-Task Dot Notation, and Trivial Fast-Track vs. Complex Audit rules.**

---

### 2608.3.0-s (2026-08-03) - Stable Release

**Major Specification Update introducing the Colon-Delimited `[STATE]:[PHASE]` Syntax Standard.**

---

### 2608.2.0-s (2026-08-03) - Stable Release

**Major Release introducing the 11-State Task Matrix and Review vs. Audit phase distinction.**

---

### 2608.1.0-s (2026-08-03) - Stable Release

**Initial Stable Release of the official JLDN Todo Schema Specification.**
