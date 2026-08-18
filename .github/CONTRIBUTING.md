# Contributing to JLDN Backlog Schema

Thank you for contributing to the **JLDN Backlog Schema**! Please review the guidelines below before submitting pull requests.

---

## 1. Schema Invariants

1. **Acyclic DAG Integrity:** Any relational task additions or modifications must strictly preserve directed acyclic graphs (`child_of`, `prerequisite`).
2. **Generational Versioning:** All specification modifications must be registered in `.dev/[GEN]/backlog.json` and follow GVS (`[YYMM].[SUBVERSION].[REVISION]-[TAG]`).
3. **JSON Formatting:** Datasets must be formatted with 2-space indentation and UTF-8 encoding.

---

## 2. Commit & Versioning Conventions

- All pull requests and commits adhere to standard Conventional Commits or JLDN task taxonomy (`Fix PROJ-TODO-XX: ...`).
- Direct-to-main branching protocol is standard for core maintainers.
