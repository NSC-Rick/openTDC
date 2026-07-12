# Changelog

**Project:** openTDC  
**Purpose:** Record of repository and project changes  
**Format:** Based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)

---

## Changelog Guidelines

This changelog documents notable changes to the openTDC repository and project.

### Change Categories

- **Added:** New features, files, or capabilities
- **Changed:** Changes to existing functionality or documentation
- **Deprecated:** Features or approaches marked for future removal
- **Removed:** Deleted features, files, or capabilities
- **Fixed:** Bug fixes or corrections
- **Security:** Security-related changes

### Version Numbering

This project uses **phase-based versioning** rather than semantic versioning:
- Format: `Phase.Session.Revision`
- Example: `Discovery.001.0` = Engineering Discovery phase, Session 1, no revisions

---

## [Unreleased]

### Planned
- Test equipment inventory documentation
- Hardware sample documentation
- First TDC characterization session

---

## [Discovery.001.0] - 2026-07-12

### Added

**Repository Structure:**
- Created top-level folder structure:
  - `docs/` - Supporting documentation
  - `bench/` - Bench test procedures and results
  - `photos/` - Engineering photographs and visual documentation
  - `hardware/` - Hardware artifacts and documentation
  - `firmware/` - Firmware artifacts and reverse engineering notes
  - `schematics/` - Circuit diagrams and PCB layouts
  - `research/` - Background research and reference materials
  - `releases/` - Formal engineering release packages

**Documentation:**
- `README.md` - Repository overview and engineering philosophy
- `PROJECT_CHARTER.md` - Project scope, objectives, and governance
- `ENGINEERING_PRINCIPLES.md` - Detailed engineering philosophy and standards
- `ENGINEERING_NOTEBOOK.md` - Chronological engineering session log
- `ENGINEERING_DECISIONS.md` - Decision records with rationale
- `CHANGELOG.md` - This file
- `METHODOLOGY_OBSERVATIONS.md` - Lessons learned and process improvements

**Engineering Decisions:**
- Decision 001: Repository Classification as Engineering Configuration Repository
- Decision 002: Project Phase Structure
- Decision 003: Session-Based Workflow with EPP Handoffs
- Decision 004: AI Role and Oversight

**Engineering Sessions:**
- Session 001: Repository Initialization

### Changed
- N/A (Initial release)

### Deprecated
- N/A (Initial release)

### Removed
- N/A (Initial release)

### Fixed
- N/A (Initial release)

### Security
- N/A (Initial release)

---

## Version History Summary

| Version | Date | Phase | Description |
|---------|------|-------|-------------|
| Discovery.001.0 | 2026-07-12 | Engineering Discovery | Repository initialization and foundation |

---

## Changelog Maintenance

- Update this file with each significant repository change
- Group changes by session or logical unit of work
- Date entries when they are released/completed
- Move items from [Unreleased] to versioned sections when sessions complete
- Reference related engineering decisions and session IDs
- Use clear, descriptive language

---

**Changelog Established:** July 12, 2026  
**Current Version:** Discovery.001.0  
**Status:** Active
