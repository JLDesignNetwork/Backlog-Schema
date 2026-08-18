# JLDN Backlog Schema Strategic Roadmap

> **Specification:** JLDN Backlog Schema  
> **Generation Epoch:** `2608` (August 2026)  
> **Author:** Jeff Langdon (JL Design Network)  
> **Status:** Active Standard  

---

## Strategic Vision

The **JLDN Backlog Schema** is the universal, standardized, document-bound and repository-bound task management protocol governing all JLDN software, rulesets, publishing pipelines, and developer tooling.

```
                    BACKLOG SCHEMA GENERATIONAL TIMELINE
  ┌────────────────────────┐       ┌────────────────────────┐       ┌────────────────────────┐
  │ Generation 2608        │       │ Generation 2609        │       │ Future Generations     │
  │ Core Backlog Protocol  │ ───>  │ Automated CI Tooling   │ ───>  │ IDE Language Server    │
  │ Mode 1 & Mode 2 Hubs   │       │ CLI Schema Validator   │       │ Real-Time Sync Daemon  │
  └────────────────────────┘       └────────────────────────┘       └────────────────────────┘
```

---

## Generational Backlogs & Horizons

### Generation 2608 (Active Baseline)
- [x] **Formal 11-State Modular Task Matrix:** Initial, review, audit, refactor, and terminal states.
- [x] **Relational Lineage:** Strict DAG vertical ancestry (`child_of`), horizontal associations (`relates_to`, `prerequisite`).
- [x] **Version Origin & Protection:** Mandatory `existed_since`, `blocked_since`, `deprecated_since`, and `"protection": "protected"` governance flags.
- [x] **Generational Hub Architecture:** Mode 2 `.dev/[GEN]/backlog.json` companion datasets.
- [x] **Target Metadata Keys:** Cross-repository and cross-version pointer taxonomy (`target_*`).
- [ ] **Orange Team Legacy Modernization:** Full alignment with JLDN Gold Standard baseline scaffolding and GitHub governance.

### Generation 2609+ (Future Horizons)
- [ ] **Automated CI Validation Tooling:** High-speed schema validator script (`validate_backlog.py` / `pnpm dlx @jldn/backlog-validate`).
- [ ] **Interactive Visualizer:** Terminal UI and web dashboard component for rendering DAG dependency graphs.
