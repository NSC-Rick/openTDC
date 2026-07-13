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

### Session ES-001: OEM TDC Baseline Documentation

**Date:** 2026-07-12  
**Time:** 08:24 - 08:29 (UTC-04:00)  
**Engineer:** Rick Daniell (Lead Systems Engineer)  
**Phase:** Engineering Discovery

#### Objective

Establish baseline photographic documentation of the OEM John Deere 316 Time Delay Controller prior to any disassembly, electrical testing, or reverse engineering activities.

#### Activities

- Photographed OEM TDC housing (external assembly)
- Photographed OEM TDC front PCB (component side)
- Photographed OEM TDC rear PCB (solder side)
- Created `hardware/OEM_TDC/` directory structure
- Imported photographs to `hardware/OEM_TDC/photos/`
- Created `hardware/OEM_TDC/OEM_TDC.md` hardware documentation
- Documented physical observations from visual inspection
- Identified known unknowns for future investigation

#### Observations

**Physical Observations (Visual Only):**
- Controller remains fully assembled
- External housing appears intact
- Through-hole component construction
- Relay visible on PCB
- Electrolytic capacitor present
- Multiple discrete components visible
- Connector solder joints visible
- No obvious signs of overheating, corrosion, or component damage

**Methodology Observations:**
- Photographic evidence captured before any analysis or interpretation
- Clear separation maintained between objective evidence and engineering conclusions
- Engineering confidence rating included in documentation
- Evidence Package concept successfully implemented

#### Data Collected

**Evidence Package ES-001:**
- `OEM Housing.jpeg` (659,498 bytes)
- `OEM TDC Front PCB.jpeg` (664,752 bytes)
- `OEM TDC Rear PCB.jpeg` (765,724 bytes)

**Documentation:**
- `hardware/OEM_TDC/OEM_TDC.md` - Hardware baseline documentation

#### Decisions Made

- **ED-008:** Baseline Hardware Documentation Prior to Reverse Engineering - See ENGINEERING_DECISIONS.md #008

Decision: All OEM hardware shall be thoroughly documented through non-destructive photographic evidence before any disassembly, modification, electrical testing, or reverse engineering activities.

#### Methodology Observations

- **MO-005:** Engineering Evidence Should Be Captured Before Engineering Interpretation - See METHODOLOGY_OBSERVATIONS.md #005

Observation: Capturing engineering evidence before analysis significantly improves quality and traceability. Evidence and interpretation should be clearly separated.

#### Open Questions

**Known Unknowns Identified:**
- Internal circuit topology
- Relay control logic
- Comparator usage
- Timing implementation
- Power supply architecture
- Input conditioning
- Output driver topology
- Presence of active timing circuitry
- Component values
- PCB revision level
- Functional truth table
- Connector pin assignments

#### Follow-Up Required

- [ ] Electrical characterization of connector pinout
- [ ] Power supply voltage identification
- [ ] Input signal characterization
- [ ] Output signal characterization
- [ ] Relay control logic analysis
- [ ] Component value measurement
- [ ] Circuit topology reverse engineering

#### Engineering Confidence

**Documentation Confidence:** ★★★★★

- Physical observations only
- No engineering assumptions made
- No circuit functionality inferred
- Baseline successfully established

#### Next Engineering Objective

Electrical characterization of OEM TDC connector pinout and power supply requirements.

#### EPP Reference

*To be created upon session completion*

---

### Session EPP-002: OEM Reference Documentation Collection

**Date:** 2026-07-12  
**Time:** 08:38 - 08:40 (UTC-04:00)  
**Engineer:** Rick Daniell (Lead Systems Engineer)  
**Phase:** Engineering Discovery

#### Objective

Capture and preserve all existing John Deere documentation that will inform the reverse engineering effort for the John Deere 316 Time Delay Controller.

#### Activities

- Created `research/OEM_Documentation/` directory structure
- Imported OEM reference documents from personal collection
- Created comprehensive documentation catalog in `research/OEM_Documentation/README.md`
- Cataloged each document with source, format, and metadata
- Identified document limitations and cross-references

#### Observations

**Documentation Collected:**
- 1 comprehensive service manual (21.7 MB PDF)
- 2 electrical schematics (TM1590 and PTO)
- 1 engine-specific service information document
- Total: 4 documents, ~22.2 MB

**Documentation Quality:**
- Service manual appears comprehensive
- TM1590 designation indicates official John Deere technical manual
- Some documents lack revision/date information
- All documents from personal collection (provenance documented)

**Engineering Value:**
- Service manual provides system integration context
- TM1590 schematics are primary electrical reference
- PTO schematic may contain TDC-related circuitry
- Onan P218G documentation provides engine context

#### Data Collected

**OEM Reference Documents:**
- `-johndeereonan316318420servicemanual-.pdf` (21,666,009 bytes)
- `318 Tm1590 schematics.pdf` (421,684 bytes)
- `PTO schematic for 318.JPG` (50,730 bytes)
- `Onan P218G ignition tests.jpg` (106,112 bytes)

**Documentation:**
- `research/OEM_Documentation/README.md` - Documentation catalog

#### Decisions Made

No new engineering decisions in this session.

#### Methodology Observations

**Documentation as Evidence:**
- OEM documentation represents authoritative design intent
- Document provenance recorded for traceability
- Limitations and unknowns explicitly identified
- Catalog structure supports future document additions

#### Open Questions

**Document Review Required:**
- What TDC-specific information is in the service manual?
- Does TM1590 contain TDC circuit details?
- What connector pinout information is available?
- Are there TDC specifications or operational parameters documented?

**Missing Documentation:**
- Connector pinout diagrams (may be in TM1590)
- Parts catalog excerpts
- TDC-specific service bulletins
- Revision-specific documentation

#### Follow-Up Required

- [ ] Review service manual for TDC sections
- [ ] Review TM1590 schematics for TDC circuit details
- [ ] Extract connector pinout information
- [ ] Identify TDC specifications and parameters
- [ ] Cross-reference documentation with hardware observations
- [ ] Document any discrepancies between OEM docs and hardware

#### Engineering Confidence

**Documentation Completeness:** ★★★★☆

- Good collection of primary reference materials
- Official John Deere service manual and schematics
- Some revision/date information missing
- May require additional documents as reverse engineering progresses

#### Next Engineering Objective

Review OEM documentation to extract TDC-specific information, connector pinouts, and operational specifications.

#### EPP Reference

EPP-002: OEM Reference Documentation

---

### Session EPP-001: Project Vision and Roadmap

**Date:** 2026-07-13  
**Time:** 05:27 - 05:31 (UTC-04:00)  
**Engineer:** Rick Daniell (Lead Systems Engineer)  
**Phase:** Engineering Discovery

#### Objective

Establish the long-term vision for the openTDC project, expanding from reverse engineering to developing a modern replacement controller platform.

#### Activities

- Defined project vision: modern, open-source replacement TDC
- Established three-phase project roadmap
- Created engineering decisions for replacement controller philosophy
- Documented engineering constraints for each phase
- Identified future enhancement candidates
- Created ROADMAP.md with complete phase details
- Updated PROJECT_CHARTER.md to reflect expanded vision
- Updated README.md with project deliverables

#### Observations

**Project Vision Expansion:**
- Project now encompasses complete replacement controller development
- Three distinct phases: Discovery, Classic, Enhanced
- OEM compatibility remains primary objective
- Modular platform architecture for future enhancements

**Engineering Philosophy:**
- Discovery must complete before design begins
- OEM behavior preserved before enhancements introduced
- Platform approach enables incremental enhancement
- Clear phase boundaries reduce risk

**Enhancement Candidates Identified:**
- Charging voltage monitoring
- Digital hour meter
- Diagnostic LEDs
- Service diagnostics mode
- Event logging and fault history
- Bluetooth/Wi-Fi connectivity (future evaluation)
- Mobile/web dashboard (future evaluation)
- Modular I/O expansion

#### Data Collected

**Documentation Created:**
- `ROADMAP.md` - Complete three-phase project roadmap
- Engineering Decisions: ED-009, ED-010, ED-011
- Methodology Observation: MO-006

**Documentation Updated:**
- `README.md` - Project vision and deliverables
- `PROJECT_CHARTER.md` - Version 2.0 with three-phase scope
- `ENGINEERING_DECISIONS.md` - Three new decisions, count: 8 → 11
- `METHODOLOGY_OBSERVATIONS.md` - MO-006 added, count: 5 → 6

#### Decisions Made

- **ED-009:** Replacement Controller Philosophy  
  Decision: OEM compatibility remains primary objective; preserve OEM behavior before enhancements

- **ED-010:** Reverse Engineering Before Design  
  Decision: No design work until Engineering Discovery establishes complete OEM understanding

- **ED-011:** Platform Architecture  
  Decision: Modular platform capable of future enhancements without core redesign

#### Methodology Observations

- **MO-006:** Separating Engineering Discovery from Innovation  
  Observation: Strict separation between discovery and innovation phases significantly reduces engineering risk and improves quality

#### Open Questions

**Phase 1 Completion:**
- What constitutes "complete understanding" of OEM operation?
- How will engineering team consensus be achieved?
- What format for Engineering Discovery report?

**Future Phases:**
- Which enhancements should be prioritized?
- What expansion architecture best supports modular enhancements?
- How to maintain OEM compatibility while adding features?

#### Follow-Up Required

- [ ] Continue Engineering Discovery activities
- [ ] Define Engineering Discovery completion criteria in detail
- [ ] Establish enhancement prioritization framework
- [ ] Plan Phase 1 → Phase 2 transition process

#### Engineering Confidence

**Project Vision Clarity:** ★★★★★

- Clear three-phase roadmap established
- Engineering philosophy well-defined
- Phase boundaries explicit
- Enhancement candidates identified
- Risk mitigation strategies documented

#### Next Engineering Objective

Continue Engineering Discovery Phase 1 activities:
- Battery installation and verification
- Charging system characterization
- Neutral switch characterization
- Safety interlock characterization
- TDC input/output mapping

**Engineering Discovery remains current phase. No design work authorized.**

#### EPP Reference

EPP-001: Project Vision and Roadmap

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
**Current Session:** EPP-001  
**Status:** Active
