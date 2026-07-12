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
- Review OEM documentation for TDC-specific information
- Extract connector pinout from schematics
- Electrical characterization of OEM TDC connector pinout

---

## [Discovery.EPP-002.0] - 2026-07-12

### Added

**OEM Reference Documentation:**
- `research/OEM_Documentation/` directory structure
- `research/OEM_Documentation/README.md` - Comprehensive documentation catalog

**Service Manuals:**
- `-johndeereonan316318420servicemanual-.pdf` (21.7 MB) - John Deere Onan 316/318/420 service manual

**Electrical Schematics:**
- `318 Tm1590 schematics.pdf` (422 KB) - Official John Deere TM1590 technical manual schematics
- `PTO schematic for 318.JPG` (51 KB) - PTO electrical schematic

**TDC-Related Service Information:**
- `Onan P218G ignition tests.jpg` (106 KB) - Onan P218G engine ignition test procedures

**Engineering Sessions:**
- Session EPP-002: OEM Reference Documentation Collection

### Changed

- `ENGINEERING_NOTEBOOK.md` - Added Session EPP-002, updated current session

### Deprecated
- N/A

### Removed
- N/A

### Fixed
- N/A

### Security
- N/A

---

## [Discovery.ES-001.0] - 2026-07-12

### Added

**Hardware Documentation:**
- `hardware/OEM_TDC/` directory structure
- `hardware/OEM_TDC/photos/` directory for evidence storage
- `hardware/OEM_TDC/OEM_TDC.md` - OEM hardware baseline documentation

**Evidence Package ES-001:**
- `OEM Housing.jpeg` - External housing assembly photograph
- `OEM TDC Front PCB.jpeg` - Front side PCB photograph
- `OEM TDC Rear PCB.jpeg` - Rear side PCB photograph

**Engineering Decisions:**
- Decision 008: Baseline Hardware Documentation Prior to Reverse Engineering

**Engineering Sessions:**
- Session ES-001: OEM TDC Baseline Documentation

**Methodology Observations:**
- Observation 005: Engineering Evidence Should Be Captured Before Engineering Interpretation

### Changed

- `ENGINEERING_NOTEBOOK.md` - Added Session ES-001, updated current session
- `ENGINEERING_DECISIONS.md` - Added ED-008, updated decision count to 8
- `METHODOLOGY_OBSERVATIONS.md` - Added MO-005, updated observation count to 5

### Deprecated
- N/A

### Removed
- N/A

### Fixed
- N/A

### Security
- N/A

---

## [Discovery.EPP-000.0] - 2026-07-12

### Added

**NorthStar Engineering Workflow:**
- Formal engineering team structure with defined roles
- Lead Systems Engineer: Rick Daniell
- Engineering Research & Systems Partner: Grace
- Engineering Configuration Manager: Devin
- Standard engineering workflow from bench to repository
- Repository Health Assessment protocol

**Engineering Decisions:**
- Decision 005: Engineering Authority and AI Role Boundaries
- Decision 006: Git Commit and Push Approval Required
- Decision 007: Repository Health Assessment Advisory Status

**Engineering Sessions:**
- Session EPP-000: NorthStar Engineering Workflow Adoption

**Methodology Observations:**
- Observation 004: NorthStar Engineering Workflow Scalability

### Changed

- `README.md` - Added Engineering Team section and NorthStar Engineering Workflow
- `ENGINEERING_NOTEBOOK.md` - Added Session EPP-000, updated current session
- `ENGINEERING_DECISIONS.md` - Added ED-005, ED-006, ED-007, updated decision count to 7
- `METHODOLOGY_OBSERVATIONS.md` - Added Observation 004, updated observation count to 4

### Deprecated
- N/A

### Removed
- N/A

### Fixed
- N/A

### Security
- N/A

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
| Discovery.EPP-000.0 | 2026-07-12 | Engineering Discovery | NorthStar Engineering Workflow adoption |
| Discovery.ES-001.0 | 2026-07-12 | Engineering Discovery | OEM TDC baseline documentation |
| Discovery.EPP-002.0 | 2026-07-12 | Engineering Discovery | OEM reference documentation collection |

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
**Current Version:** Discovery.EPP-002.0  
**Status:** Active
