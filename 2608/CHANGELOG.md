# Changelog - JLDN Todo Schema Specification

All notable changes to the JLDN Todo Schema Specification will be documented in this file.

The versioning follows the [JLDN Generational Versioning Schema](https://github.com/JLDesignNetwork/Generational-Versioning-Schema) format (`[YYMM].[SUBVERSION].[REVISION]-[TAG]`).

---

## Generation 2608

### 2608.17.0-as (2026-08-04) - Public Alpha Release

**Public Alpha release codifying Target Metadata Keys (`target_version`, `target_file`, `target_component`, `target_repository`) in the task object schema (`TODO-15`).**

#### Added
- **Target Metadata Keys (`target_*`):** Codified optional target pointers (`target_version`, `target_file`, `target_component`, `target_repository`) to eliminate reference ambiguity in cross-version and project-wide task tracking datasets (such as root `todo.json`).
- **`TODO-15` Registered & Completed:** Registered task `TODO-15` in `2608/todo.json` tracking target metadata keys governance.

---

### 2608.16.0-as (2026-08-04) - Public Alpha Release

**Public Alpha release standardizing companion dataset filename (`todo.json` / `todo.yaml`) and eliminating redundant version numbers from filenames inside version directories.**

#### Added
- **Standard Companion Dataset Filenames:** Standardized default companion file naming to `todo.json` or `todo.yaml` within major version folders.
- **Non-Redundant Version Naming:** Standardized document naming inside version folders (`2608/vampire.md`, `2608/todo.json`), leaving version numbers exclusively to folder names (`2608/`).
- **`TODO-14` Registered:** Completed task `TODO-14` in frontmatter tracking standardized `todo.json` companion dataset governance.

---

### 2608.15.0-as (2026-08-04) - Public Alpha Release

**Public Alpha release formalizing Mode 2 Companion Dataset Storage Pattern and metadata pointer keys (`todo_file`, `changelog_file`).**

#### Added
- **Storage Modes Architecture:** Codified Mode 1 (Embedded Inline Frontmatter) and Mode 2 (Companion Dataset Storage Pattern) for repository architecture flexibility.
- **Metadata File Pointers:** Codified `"todo_file"` (referencing sibling dataset `<file>.todo.json`) and `"changelog_file"` (referencing sibling `CHANGELOG.md`) within document frontmatter headers.
- **`TODO-13` Registered:** Completed task `TODO-13` in frontmatter tracking Mode 2 companion dataset governance.

---

### 2608.14.0-as (2026-08-03) - Public Alpha Release

**Public Alpha release adding conditionally mandatory `*-since` Version Origin Keys (`existed_since`, `blocked_since`, `deprecated_since`) and the `protection` Governance Key for completed tasks.**

#### Added
- **`*-since` Version Origin Keys:** Codified conditionally mandatory version tracking keys (`existed_since` required on task creation; `blocked_since` required on `blocked` status; `deprecated_since` required on `deprecated` status).
- **`protection` Governance Key:** Codified architectural preservation key for `completed` tasks (`"protected"` vs `"open"`, defaulting to `"open"` when omitted). Protected items represent locked system elements requiring future tasks/refactors to build around them.
- **`protection` Regex Validation:** Added `^(protected|open)$` regular expression standard.

---

### 2608.13.0-as (2026-08-03) - Public Alpha Release

**Public Alpha release applying Round 9 Red Team Audit fixes: Acyclic DAG Prerequisite Rule, Self-Reference Prohibition, Terminal Prerequisite Satisfaction on Deprecated Tasks, and Formalized Priority Hierarchy Ranks.**

#### Added
- **Acyclic DAG Prerequisite Rule:** Codified rule requiring `prerequisite` relational chains to form a directed acyclic graph, strictly prohibiting circular prerequisite deadlocks.
- **Self-Reference Prohibition:** Codified explicit prohibition against self-referential task IDs in `child_of`, `relates_to`, or `prerequisite` keys (`"child_of": "TODO-01"` on `TODO-01`).
- **Terminal Prerequisite Satisfaction on Deprecated Tasks:** Clarified that prerequisite gating is satisfied whenever a prerequisite task reaches ANY valid terminal state (`completed` or `deprecated`).
- **Formal Priority Rank Order:** Formalized the 4-level numerical rank hierarchy: `critical` (Rank 4) > `high` (Rank 3) > `medium` (Rank 2) > `low` (Rank 1).

---

### 2608.12.0-as (2026-08-03) - Public Alpha Release

**Public Alpha release applying Round 8 Red Team Audit fixes: `prerequisite` Execution Key, Active-Only Parent Priority De-Escalation Sync, Section Minimum Quality Threshold, and Single-Line String Requirement.**

---

### 2608.11.0-as (2026-08-03) - Public Alpha Release

**Public Alpha release applying Round 7 Red Team Audit fixes: Parent Priority Dynamic Sync, 2-Space Indented UTF-8 JSON Formatting Standard, 4-Digit ID Scaling Regex (`TODO-\d{2,4}`), and Cascaded Deprecation Immutability.**

---

### 2608.10.0-as (2026-08-03) - Public Alpha Release

**Public Alpha release applying Round 6 Red Team Audit fixes: Sub-Task Numerical Index Formatting (`.1a`), Parent Deprecation Cascade Rule, Empty Array Validity (`"todo": []`), and Pre-Validation String Trimming.**

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
