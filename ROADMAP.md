# openTDC Project Roadmap

**Project:** openTDC  
**Purpose:** Long-term project vision and phased development plan  
**Established:** July 13, 2026

---

## Project Vision

The openTDC project will develop a modern, open-source replacement for the John Deere 316 Time Delay Controller that preserves OEM functionality while introducing carefully engineered enhancements.

The replacement controller will:
- Maintain 100% electrical compatibility with the original tractor
- Preserve OEM operating behavior as the baseline
- Significantly improve diagnostics, serviceability, and maintainability
- Support modular expansion for future enhancements
- Provide complete engineering documentation

---

## Engineering Philosophy

### Core Principles

1. **OEM Compatibility First**  
   Replacement controller must preserve original tractor operation

2. **Evidence-Based Engineering**  
   All design decisions supported by documented evidence

3. **Complete Understanding Before Design**  
   No design work until Engineering Discovery is complete

4. **Modular Platform Architecture**  
   Core control separated from enhancements, expansion over replacement

5. **Engineering Discipline**  
   Separate discovery from innovation, maintain phase boundaries

---

## Project Phases

### Phase 1: Engineering Discovery

**Status:** In Progress  
**Started:** July 12, 2026  
**Objective:** Completely understand OEM controller operation

#### Scope

- Reverse engineer OEM controller
- Characterize all inputs (voltage levels, timing, behavior)
- Characterize all outputs (voltage levels, timing, behavior)
- Build complete functional truth table
- Understand timing behavior and delays
- Validate OEM operation through testing
- Document all findings with evidence

#### Deliverables

- Complete OEM hardware documentation
- Input/output characterization data
- Functional truth table
- Timing diagrams
- Test results and validation data
- Engineering evidence packages
- Reverse engineering report

#### Completion Criteria

- All inputs fully characterized
- All outputs fully characterized
- Complete truth table validated
- Timing behavior understood
- No unknown operating modes
- All evidence documented
- Engineering team confident in complete understanding

#### Engineering Constraints

- No design work permitted
- No firmware development
- No PCB design
- No enhancement implementation
- No assumptions - only documented evidence
- Unknown is an acceptable state

---

### Phase 2: OpenTDC Classic

**Status:** Not Started  
**Prerequisites:** Phase 1 complete  
**Objective:** 100% OEM-compatible replacement controller

#### Scope

- Design hardware architecture based on OEM understanding
- Select modern components (microcontroller, relays, etc.)
- Design PCB layout
- Develop firmware implementing OEM behavior
- Create test procedures
- Validate 100% OEM compatibility
- Document complete design

#### Deliverables

- Hardware architecture documentation
- Component selection rationale
- PCB design files (schematics, layout, gerbers)
- Firmware source code
- Test procedures and results
- Assembly instructions
- User documentation
- Complete engineering package

#### Key Features

- **100% OEM Compatible:** Drop-in replacement, identical operation
- **Modern Components:** Improved reliability and availability
- **Fully Documented:** Complete schematics, firmware, assembly docs
- **Improved Reliability:** Modern components, better construction
- **Maintainable:** Open-source, documented, reproducible

#### Success Criteria

- Passes all OEM functional tests
- Identical timing behavior
- Identical input/output characteristics
- Successful installation in test tractor
- Extended operational validation
- No behavioral differences from OEM

---

### Phase 3: OpenTDC Enhanced

**Status:** Not Started  
**Prerequisites:** Phase 2 complete and validated  
**Objective:** Enhanced replacement with diagnostics and monitoring

#### Scope

- Design modular enhancement architecture
- Implement enhancement features
- Maintain OEM compatibility baseline
- Develop enhanced firmware
- Create configuration/diagnostic interfaces
- Validate enhanced operation
- Document enhancements

#### Enhancement Categories

##### Monitoring & Diagnostics

- **Charging System Voltage Monitoring**  
  Monitor battery and charging voltage, detect charging system issues

- **Digital Hour Meter**  
  Track engine operating hours

- **Power-On Self-Test**  
  Verify controller operation at startup

- **Diagnostic Status LEDs**  
  Visual indication of controller status and faults

- **Fault Indication**  
  Detect and indicate system faults

##### Service & Troubleshooting

- **Service Diagnostics Mode**  
  Special mode for troubleshooting and testing

- **Bench Test Mode**  
  Operate controller on bench without tractor

- **Test Points**  
  Accessible test points for troubleshooting

- **Service Connector**  
  Dedicated connector for service tools

##### Data & Connectivity

- **Event Logging**  
  Record operational events and faults

- **Fault History**  
  Maintain history of detected faults

- **Bluetooth or Wi-Fi Connectivity** *(Future Evaluation)*  
  Wireless connectivity for diagnostics

- **Mobile/Web Dashboard** *(Future Evaluation)*  
  Remote monitoring and diagnostics

##### Configuration & Expansion

- **Configurable Timing Parameters** *(Future Evaluation)*  
  User-adjustable timing if safe and beneficial

- **Firmware Update Capability**  
  Field-updateable firmware

- **Modular I/O Expansion**  
  Expansion capability for future features

#### Deliverables

- Enhanced hardware design
- Enhanced firmware
- Configuration tools
- Diagnostic software
- Mobile/web interface (if implemented)
- Enhanced documentation
- User guides

#### Key Features

- **OEM Baseline Preserved:** All enhancements optional, OEM mode always available
- **Modular Design:** Features can be enabled/disabled
- **Backward Compatible:** Works in tractors without enhancements
- **Diagnostic Capability:** Significantly improved troubleshooting
- **Data Logging:** Historical data for analysis
- **Future-Proof:** Expansion capability for unforeseen needs

#### Success Criteria

- OEM compatibility maintained
- Enhancements function as designed
- No interference with baseline operation
- User-friendly configuration
- Reliable diagnostic capability
- Successful field deployment

---

## Enhancement Prioritization

Enhancements will be prioritized based on:

1. **Engineering Value:** Benefit to troubleshooting and maintenance
2. **User Value:** Benefit to tractor owners
3. **Implementation Complexity:** Development effort required
4. **Risk:** Potential impact on baseline operation
5. **Cost:** Component and manufacturing cost impact

High-priority enhancements:
- Charging voltage monitoring
- Diagnostic LEDs
- Service diagnostics mode
- Digital hour meter

Medium-priority enhancements:
- Event logging
- Fault history
- Bench test mode
- Test points

Future-evaluation enhancements:
- Wireless connectivity
- Mobile/web dashboard
- Configurable timing
- I/O expansion

---

## Engineering Constraints

The following constraints apply to all phases:

### Phase 1 (Engineering Discovery)

- No design work
- No firmware development
- No PCB design
- No enhancement implementation
- Evidence-based conclusions only
- Unknown is acceptable

### Phase 2 (OpenTDC Classic)

- 100% OEM compatibility required
- No enhancements in Phase 2
- Complete validation before Phase 3
- No assumptions from Phase 1

### Phase 3 (OpenTDC Enhanced)

- OEM baseline must be preserved
- Enhancements must be optional
- No breaking changes to Phase 2
- Modular architecture required

---

## Risk Management

### Engineering Risks

- **Incomplete OEM Understanding:** Mitigated by thorough Phase 1, clear completion criteria
- **Design Assumptions:** Mitigated by evidence-based approach, no design until Phase 1 complete
- **Compatibility Issues:** Mitigated by OEM-first philosophy, extensive validation
- **Feature Creep:** Mitigated by phase boundaries, explicit enhancement prioritization
- **Over-Engineering:** Mitigated by modular approach, focus on core platform

### Project Risks

- **Scope Expansion:** Mitigated by clear phase definitions, engineering discipline
- **Premature Design:** Mitigated by Decision 010, phase boundaries
- **Loss of Focus:** Mitigated by current phase emphasis, roadmap visibility

---

## Current Status

**Current Phase:** Phase 1 - Engineering Discovery  
**Current Session:** EPP-001  
**Phase Progress:** Early stage - baseline documentation established

### Completed Activities

- Repository structure established
- NorthStar Engineering Workflow adopted
- OEM hardware baseline documented (Evidence Package ES-001)
- OEM reference documentation collected
- Project vision and roadmap established

### Next Activities

- Battery installation and verification
- Charging system characterization
- Neutral switch characterization
- Safety interlock characterization
- TDC input/output mapping
- Continued OEM hardware documentation

---

## Phase Transition Criteria

### Engineering Discovery → OpenTDC Classic

Required:
- [ ] All inputs fully characterized
- [ ] All outputs fully characterized
- [ ] Complete functional truth table
- [ ] Timing behavior understood
- [ ] All operating modes documented
- [ ] Engineering team consensus on complete understanding
- [ ] Engineering Discovery report complete

### OpenTDC Classic → OpenTDC Enhanced

Required:
- [ ] Phase 2 design complete
- [ ] Prototype built and tested
- [ ] 100% OEM compatibility validated
- [ ] Successful tractor installation
- [ ] Extended operational validation (minimum duration TBD)
- [ ] Engineering team consensus on baseline stability

---

## Long-Term Vision

The openTDC project aims to create:

1. **Complete Engineering Documentation**  
   Fully documented OEM controller operation and replacement design

2. **Open-Source Platform**  
   Community-accessible design, firmware, and documentation

3. **Modular Enhancement Ecosystem**  
   Platform supporting diverse enhancements and configurations

4. **Engineering Knowledge Base**  
   Comprehensive understanding of TDC operation and design

5. **Reproducible Design**  
   Anyone can build, modify, or enhance the controller

---

## Related Engineering Decisions

- **ED-009:** Replacement Controller Philosophy (OEM compatibility first)
- **ED-010:** Reverse Engineering Before Design (no design until discovery complete)
- **ED-011:** Platform Architecture (modular, expandable design)
- **ED-002:** Project Phase Structure (Engineering Discovery phase)

---

## Related Methodology Observations

- **MO-006:** Separating Engineering Discovery from Innovation (reduces risk, improves quality)
- **MO-005:** Engineering Evidence Should Be Captured Before Interpretation
- **MO-004:** NorthStar Engineering Workflow Scalability

---

**Roadmap Established:** July 13, 2026  
**Last Updated:** July 13, 2026  
**Status:** Active
