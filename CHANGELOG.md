# Changelog - JLDN Todo Schema Specification

All notable changes to the JLDN Todo Schema Specification will be documented in this file.

The versioning follows the [JLDN Generational Versioning Schema](https://github.com/JLDesignNetwork/Generational-Versioning-Schema) format (`[YYMM].[SUBVERSION].[REVISION]-[TAG]`).

---

## Generation 2608

### 2608.10.0-as (2026-08-03) - Public Alpha Release

**Public Alpha release applying Round 6 Red Team Audit fixes: Sub-Task Numerical Index Formatting (`.1a`), Parent Deprecation Cascade Rule, Empty Array Validity (`"todo": []`), and Pre-Validation String Trimming.**

#### Added
- **Sub-Task Numerical Index Formatting (`.1a`):** Codified that sub-task numerical indexes use unpadded integers (`.1a`, `.2a`, `.10a`), and parsing engines MUST strip sub-task suffixes to resolve parent IDs (`TODO-01`).
- **Parent Deprecation Cascade Rule:** Codified rule requiring all active/pending child sub-tasks to automatically cascade to `deprecated` status whenever their parent task transitions to `deprecated`.
- **Empty Array Validity (`"todo": []`):** Explicitly codified that an empty array (`"todo": []`) is valid JSON frontmatter representing zero active tasks.
- **Pre-Validation String Trimming:** Codified requirement for ingestion engines to trim leading/trailing whitespace prior to regex evaluation.

---

### 2608.9.0-as (2026-08-03) - Public Alpha Release

**Public Alpha release applying Round 5 Red Team Audit fixes: Parent-Child Blocker Propagation, Strict Target Existence Validation, Priority Validation Regex, and Pair Owner Formatting Standard.**

---

### 2608.8.0-as (2026-08-03) - Public Alpha Release

**Public Alpha release integrating the `child_of` vertical ancestry key and decoupled `relates_to` horizontal association key.**

---

### 2608.7.0-as (2026-08-03) - Public Alpha Release

**Public Alpha release applying Round 4 Red Team Audit fixes: Single-letter sub-task limit (`a`-`z`), primary key uniqueness enforcement, title/details quality thresholds, and DAG relational link rules.**

---

### 2608.6.0-as (2026-08-03) - Public Alpha Release

**Public Alpha release applying Round 3 Red Team Audit fixes: Sub-Task Letter Parts (`TODO-01.1a`), strict local document isolation, conditional `reason` requirement, and priority escalation rules.**

---

### 2608.5.0-as (2026-08-03) - Public Alpha Release

**Public Alpha release applying Round 2 Red Team Audit fixes: Mandatory `priority` property, `relates_to` relational linking key, parent completion on terminal child states, section heading resilience, and numeric ID parsing.**

---

### 2608.4.0-as (2026-08-03) - Public Alpha Release

**Public Alpha release applying Round 1 Red Team Audit fixes: Unblock Recovery Pathway, `reason` & `owner` properties, Sub-Task Dot Notation, and Trivial Fast-Track vs. Complex Audit rules.**

---

### 2608.3.0-as (2026-08-03) - Public Alpha Release

**Major Specification Update introducing the Colon-Delimited `[STATE]:[PHASE]` Syntax Standard.**

---

### 2608.2.0-as (2026-08-03) - Public Alpha Release

**Major Release introducing the 11-State Task Matrix and Review vs. Audit phase distinction.**

---

### 2608.1.0-s (2026-08-03) - Stable Release

**Initial Stable Release of the official JLDN Todo Schema Specification.**
