# AI Agent & Copilot Development Guidelines

> [!IMPORTANT]
> **Authoritative Rules:** Universal JLDN rules apply. Workspace-specific guidelines are codified in:
> - **Local Rules:** `.agents/AGENTS.md`
> - **Generational Hub:** `.dev/`

## Key Invariants
1. **Schema Specifications:** All changes to task states, metadata fields, and regexes must update `docs/specification.md`.
2. **Generational Backlog:** Keep `.dev/[GEN]/backlog.json` synchronized on every task resolution.
3. **No Unstructured Tasks:** Never introduce standalone `TODO.md` or `BUGS.md` files.
