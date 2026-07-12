# Engineering Notebook

**Project:** openTDC  
**Purpose:** Chronological log of engineering sessions and activities  
**Maintained By:** Project Engineer(s)

---

## Notebook Guidelines

This engineering notebook serves as a chronological record of all engineering work performed on the openTDC project.

### Entry Requirements

Each engineering session entry must include:
- **Date and time** of session
- **Session ID** (for reference and traceability)
- **Objective** of the session
- **Activities** performed
- **Observations** made
- **Data collected** (or references to data files)
- **Decisions made** (with reference to ENGINEERING_DECISIONS.md if significant)
- **Open questions** or follow-up items
- **Engineering Project Prompt (EPP)** if session concludes with repository synchronization

### Entry Format

```
## Session [ID]: [Brief Title]

**Date:** YYYY-MM-DD  
**Time:** HH:MM - HH:MM (timezone)  
**Engineer:** [Name/ID]  
**Phase:** [Current project phase]

### Objective
[What was the goal of this session?]

### Activities
- [Activity 1]
- [Activity 2]
- ...

### Observations
[What was observed, measured, or discovered?]

### Data Collected
- [Reference to data files, photos, measurements]
- [Location in repository]

### Decisions Made
- [Decision 1] - See ENGINEERING_DECISIONS.md #[ID]
- [Decision 2]

### Open Questions
- [Question 1]
- [Question 2]

### Follow-Up Required
- [ ] [Action item 1]
- [ ] [Action item 2]

### EPP Reference
[If applicable: Reference to Engineering Project Prompt used for repository sync]

---
```

---

## Session Log

### Session 001: Repository Initialization

**Date:** 2026-07-12  
**Time:** 07:27 - [In Progress] (UTC-04:00)  
**Engineer:** Project Founder  
**Phase:** Engineering Discovery

#### Objective

Establish the openTDC engineering repository with proper structure, documentation, and engineering-first philosophy.

#### Activities

- Created repository folder structure
- Established top-level documentation framework
- Defined project charter and engineering principles
- Initialized engineering notebook
- Set up engineering decision tracking
- Created methodology observation framework
- Established changelog

#### Observations

- Repository initialized as Engineering Configuration Repository
- Engineering-first philosophy established as foundation
- Session-based workflow model adopted
- EPP (Engineering Project Prompt) handoff model defined

#### Data Collected

- Initial repository structure
- Foundational documentation (README, PROJECT_CHARTER, ENGINEERING_PRINCIPLES)

#### Decisions Made

- Repository classified as Engineering Configuration Repository (not software repository)
- Current phase set to: Engineering Discovery
- No firmware, PCB, or hardware development authorized in current phase
- Session-based workflow with EPP handoffs adopted

#### Open Questions

- What specific test equipment is available for bench testing?
- What is the condition and availability of original TDC hardware samples?
- Will peer review process be established?

#### Follow-Up Required

- [ ] Define test equipment inventory
- [ ] Document available hardware samples
- [ ] Establish first engineering session objectives for TDC characterization

#### EPP Reference

Devin Prompt 001 - Repository Foundation

---

### Session EPP-000: NorthStar Engineering Workflow Adoption

**Date:** 2026-07-12  
**Time:** 08:01 - 08:09 (UTC-04:00)  
**Engineer:** Rick Daniell (Lead Systems Engineer)  
**Phase:** Engineering Discovery

#### Objective

Adopt the NorthStar Engineering Workflow and establish the engineering team structure to support long-term openTDC project operations.

#### Activities

- Defined NorthStar Engineering Workflow
- Established engineering team roles and responsibilities
- Onboarded Devin as Engineering Configuration Manager
- Onboarded Grace as Engineering Research & Systems Partner
- Defined standard engineering session workflow
- Established Repository Health Assessment protocol
- Documented Engineering Project Prompt (EPP) format and usage
- Formalized Git commit and push approval process

#### Observations

- Clear separation of roles (Engineering, Research, Configuration Management) enables efficient workflow
- EPP-based handoffs provide complete context for repository synchronization
- Repository Health Assessments enable continuous improvement without blocking progress
- Explicit approval for Git operations maintains engineering control
- Engineering authority remains clearly with Lead Systems Engineer

#### Data Collected

- NorthStar Engineering Workflow documentation
- Team role definitions
- Engineering decision records (ED-005, ED-006, ED-007)

#### Decisions Made

- **ED-005:** Engineering authority remains with Lead Systems Engineer; AI tools support but do not make decisions - See ENGINEERING_DECISIONS.md #005
- **ED-006:** Git commits and pushes require explicit approval - See ENGINEERING_DECISIONS.md #006
- **ED-007:** Repository Health Assessments are advisory only - See ENGINEERING_DECISIONS.md #007

#### Open Questions

- None (workflow establishment session)

#### Follow-Up Required

- [x] Document NorthStar Engineering Workflow in repository
- [x] Update README with team structure
- [x] Establish Repository Health Assessment protocol
- [ ] Begin Engineering Session ES-001: TDC characterization

#### Next Engineering Objective

**Engineering Session ES-001**

Objective: Characterize the OEM John Deere 316 Time Delay Controller input logic and document existing system behavior through evidence-based testing.

Initial focus:
- Battery verification
- Charging system verification
- Neutral switch characterization
- Safety interlock validation
- Initial TDC signal mapping

#### EPP Reference

EPP-000: NorthStar Engineering Workflow Adoption & Repository Operational

---

## Future Sessions

*Subsequent engineering sessions will be documented below in chronological order.*

---

## Notebook Maintenance

- Entries are made in chronological order
- Each session receives a unique sequential ID
- No entries are deleted; corrections are made with new dated entries
- Cross-references to other documents use explicit links
- Raw data and photos are stored in appropriate repository folders and referenced here

---

**Notebook Established:** July 12, 2026  
**Current Session:** EPP-000  
**Status:** Active
