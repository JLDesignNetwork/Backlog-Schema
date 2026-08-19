---
{
  "metadata": {
    "author": "Jeff Langdon",
    "rulesetName": "JLDN Backlog Schema",
    "type": "ruleset",
    "platform": "github:public",
    "version": "2608.18.0-as",
    "backlog": ".dev/backlog.json",
    "changelog": "CHANGELOG.md"
  }
}
---
# JLDN Backlog Schema

[![GVS](https://img.shields.io/badge/GVS-2608.18.0--as-purple?style=flat-square)](https://github.com/JLDesignNetwork/Backlog-Schema)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)
[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-FFDD00?style=flat-square&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/jldesignnetwork)

Welcome to the **JLDN Backlog Schema** specification repository (JLDN Generational Versioning Schema: `2608.18.0-as`).

---

## Overview

The **JLDN Backlog Schema** is the standardized, document-bound and repository-bound task management protocol governing all JLDN software, technical specifications, publishing pipelines, and developer tooling.

* **Author:** Jeff Langdon (JL Design Network)
* **Schema Version:** `2608.18.0-as` (Public Alpha)
* **Active Generation:** `2608`

---

## 📚 Documentation & Quick Links

- 📄 **[Backlog Specification](docs/specification.md):** Complete technical protocol, validation regexes, and taxonomy rules.
- 🛠️ **[Usage Guide](docs/usage.md):** Mode 1 and Mode 2 implementation blueprints.
- 🗺️ **[Strategic Roadmap](.dev/ROADMAP.md):** Generational horizons and future tooling roadmap.
- 📝 **[Changelog](CHANGELOG.md):** Specification release history.

---

## Core Features

- **Unified Taxonomy Architecture:** Standardized `([DOMAIN]-[KIND]-[NN])` schema (e.g., `PROJ`, `DOCS`, `CORE`).
- **Dual Storage Modes:** Supports Mode 1 (Embedded Inline Frontmatter) and Mode 2 (Generational `.dev/` Hub Pattern).
- **Phase-Aware Lifecycle:** 11-state modular task matrix (`pending`, `in-progress:audit`, `completed`, `blocked`, `deprecated`).
- **Acyclic Relational Lineage:** Vertical ancestry (`child_of`) and horizontal association (`relates_to`, `prerequisite`).
- **Version Origin Tracking:** Conditionally mandatory `existed_since`, `blocked_since`, and `deprecated_since` tracking.
- **Architectural Protection:** Lock completed architectural milestones (`"protection": "protected"`).

---

## Funding & Support

If you find this specification or associated developer tooling helpful, consider supporting ongoing development:

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-FFDD00?style=flat-square&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/jldesignnetwork)

---

## License & Attribution

Licensed under the [MIT License](LICENSE). Designed and maintained by Jeff Langdon / JL Design Network. All rights reserved.
