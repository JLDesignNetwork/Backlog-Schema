# JLDN Todo Schema Specification (v2608.16.0-as)

Welcome to the **JLDN Todo Schema Specification** (Generational Versioning Schema: `2608.16.0-as`).

## Overview

This repository contains the master specification and task tracking dataset for the **JLDN Todo Schema**.

* **Author:** Jeff Langdon (JL Design Network)
* **Specification Version:** `2608.16.0-as` (Public Alpha)

### Generation 2608 Workspace Layout
- 📄 **[Specification Document](./2608/todo.md):** `2608/todo.md`
- 📊 **[TODO Dataset](./2608/todo.json):** `2608/todo.json` (JLDN Todo Schema v2608.16.0-as Mode 2)
- 📝 **[Changelog](./2608/CHANGELOG.md):** `2608/CHANGELOG.md`

## Core Features

- **Dual Storage Architecture:** Supports Mode 1 (Embedded Inline Frontmatter) and Mode 2 (Companion Dataset Pattern).
- **Phase-Aware Lifecycle:** 11-state modular task matrix (`pending`, `in-progress:audit`, `completed`, `blocked`, `deprecated`).
- **Relational Lineage:** Vertical ancestry (`child_of`) and horizontal association (`relates_to`, `prerequisite`).
- **Version Origin Tracking:** Conditionally mandatory `existed_since`, `blocked_since`, and `deprecated_since` tracking.
- **Architectural Protection:** Lock completed architectural milestones (`"protection": "protected"`).

## License & Attribution

Designed and maintained by Jeff Langdon / JL Design Network. All rights reserved.
