# Project Charter: openTDC

**Document Version:** 2.0  
**Date Established:** July 12, 2026  
**Last Amended:** July 13, 2026 (EPP-001)  
**Status:** Active

---

## Project Identity

**Project Name:** openTDC  
**Full Title:** Open Engineering Repository for the John Deere 316 Time Delay Controller  
**Classification:** Engineering Knowledge Repository  
**Current Phase:** Engineering Discovery

---

## Project Objective

To develop a modern, open-source replacement for the John Deere 316 Time Delay Controller (TDC) that preserves OEM functionality while introducing carefully engineered enhancements.

The project will deliver:
1. Complete understanding of OEM controller operation through reverse engineering
2. 100% OEM-compatible replacement controller (OpenTDC Classic)
3. Enhanced replacement with diagnostics and monitoring (OpenTDC Enhanced)
4. Comprehensive engineering documentation and knowledge base

This project serves as a model for engineering-first development of replacement controllers for legacy agricultural equipment.

---

## Scope

### Phase 1: Engineering Discovery (Current)

**In Scope:**
- Reverse engineering of the original TDC hardware
- Input/output characterization
- Functional truth table development
- Timing behavior analysis
- Bench testing and validation of OEM behavior
- Documentation of circuit design and operation
- Engineering decision documentation
- Evidence package collection
- Knowledge preservation

**Out of Scope:**
- Hardware architecture design
- Firmware development
- PCB design or layout
- Enhancement implementation
- Component selection for replacement
- Any design work based on incomplete understanding

### Phase 2: OpenTDC Classic (Future)

**Scope:**
- 100% OEM-compatible replacement controller design
- Modern component selection
- PCB design and layout
- Firmware implementing OEM behavior
- Validation and testing
- Complete engineering documentation
- Drop-in replacement capability

### Phase 3: OpenTDC Enhanced (Future)

**Scope:**
- Modular enhancement architecture
- Diagnostics and monitoring features
- Service and troubleshooting capabilities
- Data logging and connectivity
- Configuration tools
- Enhanced documentation
- Backward compatibility with Phase 2

**See ROADMAP.md for complete phase details and enhancement candidates.**

---

## Project Governance

### Decision Authority

Engineering decisions are made based on:
1. Measured evidence
2. Engineering analysis
3. Documented rationale
4. Peer review (when applicable)

### Phase Transitions

Transitions between project phases require:
- Completion of phase objectives (see ROADMAP.md for criteria)
- Documentation of findings
- Engineering team consensus on readiness
- Formal decision record
- Updated project charter

**Phase 1 → Phase 2 requires:**
- All inputs/outputs fully characterized
- Complete functional truth table
- Timing behavior understood
- Engineering Discovery report complete

**Phase 2 → Phase 3 requires:**
- 100% OEM compatibility validated
- Successful tractor installation
- Extended operational validation
- Engineering team consensus on baseline stability

### Repository Maintenance

- All engineering work must be documented
- Changes must be traceable
- Decisions must include rationale
- Evidence must be preserved

---

## Success Criteria

### Phase 1: Engineering Discovery

- [ ] All inputs fully characterized (voltage levels, timing, behavior)
- [ ] All outputs fully characterized (voltage levels, timing, behavior)
- [ ] Complete functional truth table validated
- [ ] Timing behavior understood and documented
- [ ] All operating modes documented
- [ ] Engineering evidence packages complete
- [ ] Engineering Discovery report complete
- [ ] Engineering team consensus on complete understanding

### Phase 2: OpenTDC Classic

- [ ] Hardware architecture designed and documented
- [ ] PCB design complete (schematics, layout, gerbers)
- [ ] Firmware implementing OEM behavior complete
- [ ] Prototype built and tested
- [ ] 100% OEM compatibility validated
- [ ] Successful tractor installation
- [ ] Extended operational validation complete
- [ ] Complete engineering documentation

### Phase 3: OpenTDC Enhanced

- [ ] Modular enhancement architecture implemented
- [ ] Diagnostic and monitoring features functional
- [ ] Service and troubleshooting capabilities validated
- [ ] Configuration tools developed
- [ ] Enhanced documentation complete
- [ ] OEM baseline compatibility maintained
- [ ] Successful field deployment

**See ROADMAP.md for detailed success criteria and phase transition requirements.**

---

## Stakeholders

### Primary Engineer(s)

*To be documented*

### Contributors

*To be documented as project evolves*

### Reviewers

*To be documented if peer review is established*

---

## Project Constraints

### Technical Constraints

- Must preserve OEM behavior documentation before any modifications
- All measurements must be reproducible
- All conclusions must be evidence-based

### Resource Constraints

- Limited to available test equipment
- Dependent on availability of original hardware samples

### Methodological Constraints

- Engineering rigor over speed
- Documentation completeness over rapid iteration
- Evidence-based conclusions over assumptions

---

## Risk Management

### Technical Risks

- **Hardware damage during reverse engineering**  
  *Mitigation:* Non-destructive testing prioritized; document before disassembly

- **Incomplete firmware extraction**  
  *Mitigation:* Multiple extraction methods; verification procedures

- **Measurement errors or misinterpretation**  
  *Mitigation:* Calibrated equipment; repeated measurements; peer review

### Project Risks

- **Scope creep into implementation before understanding is complete**  
  *Mitigation:* Strict phase discipline; Decision 010 prohibits design during discovery; charter enforcement

- **Loss of engineering knowledge due to poor documentation**  
  *Mitigation:* Rigorous documentation standards; session-based workflow; evidence packages

- **Premature design work biasing reverse engineering**  
  *Mitigation:* Explicit phase boundaries; Decision 010; evidence-first methodology

- **Incomplete OEM understanding leading to design errors**  
  *Mitigation:* Clear Phase 1 completion criteria; engineering team consensus required

- **Feature creep in enhancement phase**  
  *Mitigation:* Enhancement prioritization; modular architecture; phase boundaries

---

## Project Timeline

### Phase 1: Engineering Discovery

**Status:** In Progress  
**Start Date:** July 12, 2026  
**Target Completion:** TBD based on completion criteria  
**Objective:** Complete understanding of OEM controller operation

### Phase 2: OpenTDC Classic

**Status:** Not Started  
**Prerequisites:** Phase 1 complete  
**Target Start:** TBD  
**Objective:** 100% OEM-compatible replacement controller

### Phase 3: OpenTDC Enhanced

**Status:** Not Started  
**Prerequisites:** Phase 2 complete and validated  
**Target Start:** TBD  
**Objective:** Enhanced replacement with diagnostics and monitoring

**See ROADMAP.md for detailed phase information and timelines.**

---

## Repository Philosophy

This repository is maintained as an **Engineering Configuration Repository**, not a software repository.

All artifacts—code, schematics, test data, photographs—are treated as engineering documentation subject to configuration management.

---

## Amendments

This charter may be amended through formal decision records documented in `ENGINEERING_DECISIONS.md`.

All amendments must include:
- Rationale for change
- Impact analysis
- Approval record

---

## Approval

*Initial charter established by project founder.*

**Charter Version:** 1.0  
**Effective Date:** July 12, 2026

### Amendment Record

**Amendment 1 (Version 2.0):**  
**Date:** July 13, 2026  
**Session:** EPP-001  
**Changes:** Expanded project vision to include replacement controller development; added three-phase roadmap; updated scope, success criteria, and timeline  
**Rationale:** Project vision expanded from reverse engineering to complete replacement controller platform  
**Related Decisions:** ED-009, ED-010, ED-011  
**Approved By:** Rick Daniell (Lead Systems Engineer)

**Next Review:** Upon phase transition or significant project milestone
