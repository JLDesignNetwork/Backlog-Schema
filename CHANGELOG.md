# Changelog - JLDN Todo Schema Specification

All notable changes to the JLDN Todo Schema Specification will be documented in this file.

The versioning follows the [JLDN Generational Versioning Schema](https://github.com/JLDesignNetwork/Generational-Versioning-Schema) format (`[YYMM].[SUBVERSION].[REVISION]-[TAG]`).

---

## Generation 2608

### 2608.8.0-s (2026-08-03) - Stable Release

**Public Alpha release integrating the `child_of` vertical ancestry key and decoupled `relates_to` horizontal association key.**

#### Added
- **`child_of` Property:** Added optional `"child_of"` string property establishing immutable vertical task lineage (e.g. `"child_of": "TODO-01"`), mathematically guaranteeing an acyclic directed graph (DAG) while preserving parent task immutability.
- **Decoupled `relates_to` Property:** Refined `"relates_to"` to serve strictly as a horizontal correlation key for tasks sharing context without parent-child ancestry.
- **Sub-Task Single Letter Hard Limit:** Enforced hard cap on single-letter sub-task parts (`TODO-01.1a` through `TODO-01.1z`), forcing new top-level tasks with `"child_of"` if letter parts exceed `'z'`.

---

### 2608.7.0-s (2026-08-03) - Stable Release

**Public Alpha release applying Round 4 Red Team Audit fixes: Single-letter sub-task limit (`a`-`z`), primary key uniqueness enforcement, title/details quality thresholds, and DAG relational link rules.**

---

### 2608.6.0-s (2026-08-03) - Stable Release

**Public Alpha release applying Round 3 Red Team Audit fixes: Sub-Task Letter Parts (`TODO-01.1a`), strict local document isolation, conditional `reason` requirement, and priority escalation rules.**

---

### 2608.5.0-s (2026-08-03) - Stable Release

**Public Alpha release applying Round 2 Red Team Audit fixes: Mandatory `priority` property, `relates_to` relational linking key, parent completion on terminal child states, section heading resilience, and numeric ID parsing.**

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
