# JLDN Local Agent Rules: Backlog Schema

> [!IMPORTANT]
> **Universal Governance:** Universal JLDN rules apply to this workspace. Local rules are defined below:
> - **Generational Hub:** `.dev/` (active Generation `2608`)
> - **Specification Source of Truth:** `docs/specification.md` and `docs/`

## Project Invariants
1. **Schema Integrity:** Any modification to task schema keys, lifecycle states, or validation regular expressions must be updated in `docs/specification.md` and registered in `.dev/2608/backlog.json`.
2. **Generational Versioning:** All schema version releases follow GVS (`2608.SUBVERSION.REVISION-TAG`).
3. **No Unstructured Tasks:** Never store tasks in ad-hoc Markdown files; always maintain `.dev/[GEN]/backlog.json`.
