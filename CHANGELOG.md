# Changelog - JLDN Backlog Schema Specification

All notable changes to the **JLDN Backlog Schema Specification** will be documented in this file.

The format is based on [Keep a Changelog 1.1.0](https://keepachangelog.com/en/1.1.0/),
and this project adheres to the [JLDN Generational Versioning Schema (GVS)](https://github.com/JLDesignNetwork/Generational-Versioning-Schema).

## [2608.19.1-bs] - 2026-08-19

### Changed
- **Lifecycle Transition**: Promoted the Backlog Schema standard to Beta Supported (`-bs`).

## [2608.19.0-as] - 2026-08-19

### Changed
- **Taxonomy Restructuring**: Eliminated terminology collision by explicitly separating `Type`, `Domain`, `Kind`, `Scope`, `Action`, and `Category`. Replaced `[TYPE]` with `[KIND]` in the Backlog ID string format (`[DOMAIN]-[KIND]-[NN]`).
- **Domain Declarations**: Restructured the Domain namespace to strictly require `PROJ` and `DOCS` as universal baseline domains across all projects, while unlocking 3-5 character custom domains for developer architecture.
- **Project Archetypes**: Renamed documentation project type from `docs` to `wiki` and experimental type from `sandbox` to `prototype` to resolve keyword collisions with Git commit verbs and workspace directories.
- **Tracking Modes**: Enforced explicit file paths for `backlog` and `changelog` frontmatter keys, removing the ambiguous `linked` string example.

## [2608.18.0-as] - 2026-08-18

### Changed
- **Branding & Repository Standardization**: Renamed specification and repository to **JLDN Backlog Schema** (`Backlog-Schema`), aligning specification naming with the `.dev/[GEN]/backlog.json` Generational Hub architecture.
- **Taxonomy Normalization**: Codified canonical `[DOMAIN]-[TYPE]-[NN]` prefix taxonomy across all schema models.

### Added
- **In-Repo Documentation Wiki (`docs/`)**: Initialized internal wiki hub containing `docs/index.md`, `docs/specification.md`, and `docs/usage.md`.
- **Generational Development Hub (`.dev/`)**: Established root `.dev/` generational hub containing `ROADMAP.md`, `backlog.json`, `2608/backlog.json`, and `2608/ideas.json`.
- **GitHub Governance Suite**: Scaffolded `.github/FUNDING.yml`, `.github/SECURITY.md`, `.github/CONTRIBUTING.md`, `.github/CODE_OF_CONDUCT.md`, `.github/PULL_REQUEST_TEMPLATE.md`, `.github/copilot-instructions.md`, structured `.github/ISSUE_TEMPLATE/` forms, and automated CI workflows (`ci.yml`, `codeql.yml`).

## [2608.17.0-as] - 2026-08-04

### Added
- **Target Metadata Keys (`target_*`)**: Codified optional target pointers (`target_version`, `target_file`, `target_component`, `target_repository`) to eliminate reference ambiguity in cross-version task datasets.

## [2608.16.0-as] - 2026-08-04

### Added
- **Standard Dataset Filenames**: Standardized default companion file naming to `backlog.json` within major version folders.
- **Non-Redundant Version Naming**: Standardized document naming inside version folders.

## [2608.15.0-as] - 2026-08-04

### Added
- **Storage Modes Architecture**: Codified Mode 1 (Embedded Inline Frontmatter) and Mode 2 (Companion Dataset Storage Pattern).
- **Metadata File Pointers**: Codified `"todo_file"` and `"changelog_file"` within document frontmatter headers.

## [2608.14.0-as] - 2026-08-03

### Added
- **Version Origin Keys**: Codified `existed_since`, `blocked_since`, and `deprecated_since`.
- **Protection Key**: Codified `"protection": "protected"` governance key for completed tasks.

## [2608.1.0-s] - 2026-08-03

### Added
- **Initial Baseline Specification**: Codified 11-state modular task matrix, priority levels, and document-bound isolation.
