# Engineering Decisions

**Project:** openTDC  
**Purpose:** Record of significant engineering decisions with rationale and context  
**Maintained By:** Project Engineer(s)

---

## Decision Record Guidelines

This document maintains a record of all significant engineering decisions made during the openTDC project.

### What Constitutes a Significant Decision?

Record decisions that:
- Affect project scope or direction
- Establish technical approaches or methodologies
- Involve trade-offs between alternatives
- Set standards or conventions
- Impact future work or design choices
- Resolve technical uncertainties
- Change previously established decisions

### Decision Record Format

```
## Decision [ID]: [Brief Title]

**Date:** YYYY-MM-DD  
**Engineer:** [Name/ID]  
**Session:** [Session ID if applicable]  
**Status:** [Proposed | Accepted | Superseded | Rejected]  
**Phase:** [Project phase when decision was made]

### Context
[What situation led to this decision? What problem are we solving?]

### Decision
[What was decided? Be specific and clear.]

### Rationale
[Why was this decision made? What factors were considered?]

### Alternatives Considered
- **Alternative 1:** [Description] - [Why not chosen]
- **Alternative 2:** [Description] - [Why not chosen]

### Evidence
[What data, measurements, or analysis supports this decision?]

### Consequences
- **Positive:** [Expected benefits]
- **Negative:** [Expected drawbacks or limitations]
- **Risks:** [What could go wrong?]

### Related Decisions
- [Links to related decision records]

### References
- [Links to supporting documentation, test data, research]

### Updates
[If decision is modified or superseded, record changes here with dates]

---
```

---

## Decision Log

### Decision 001: Repository Classification as Engineering Configuration Repository

**Date:** 2026-07-12  
**Engineer:** Project Founder  
**Session:** 001  
**Status:** Accepted  
**Phase:** Engineering Discovery

#### Context

The openTDC project needed a clear classification to guide repository structure, documentation standards, and workflow. The choice was between treating this as a software development repository or an engineering documentation repository.

#### Decision

The openTDC repository is classified as an **Engineering Configuration Repository**, not a software repository.

All artifacts—including software, firmware, hardware designs, and schematics—are treated as engineering documentation subject to configuration management, not as primary deliverables.

#### Rationale

- The primary objective is knowledge preservation and documentation, not code delivery
- Engineering decisions and methodology are more valuable than artifacts
- Long-term maintainability requires engineering rigor
- This approach aligns with regulated industry practices
- Software/hardware are means to understanding, not ends in themselves

#### Alternatives Considered

- **Software Repository Model:** Focus on code, with documentation as secondary  
  *Why not chosen:* Would prioritize implementation over understanding; inconsistent with "understand before redesign" principle

- **Wiki or Documentation-Only Approach:** No version control of artifacts  
  *Why not chosen:* Artifacts need version control; integration of docs and artifacts is valuable

#### Evidence

- Industry best practices in engineering documentation
- Requirements for long-term knowledge preservation
- Need for traceability and configuration management

#### Consequences

- **Positive:**
  - Clear prioritization of documentation quality
  - Rigorous change management
  - Long-term maintainability
  - Traceable engineering process

- **Negative:**
  - May be slower than pure software development approach
  - Requires more documentation overhead
  - May feel unfamiliar to software-focused contributors

- **Risks:**
  - Documentation burden could slow progress if not managed well
  - Need to maintain discipline to avoid reverting to code-first approach

#### Related Decisions

- Decision 002: Project Phase Structure
- Decision 003: Session-Based Workflow

#### References

- PROJECT_CHARTER.md
- ENGINEERING_PRINCIPLES.md
- README.md

---

### Decision 002: Project Phase Structure

**Date:** 2026-07-12  
**Engineer:** Project Founder  
**Session:** 001  
**Status:** Accepted  
**Phase:** Engineering Discovery

#### Context

The project needed a structured approach to manage work progression from understanding to implementation while maintaining engineering discipline.

#### Decision

The project will operate in distinct phases with formal transitions:

**Current Phase: Engineering Discovery**
- Focus: Understanding, reverse engineering, measurement, documentation
- Prohibited: Firmware development, PCB redesign, hardware redesign

**Future Phases:** To be defined upon completion of Engineering Discovery

Phase transitions require:
- Completion of phase objectives
- Formal decision record
- Updated project charter

#### Rationale

- Enforces "understand before redesign" principle
- Prevents premature optimization or implementation
- Provides clear milestones and objectives
- Allows focused work without scope creep
- Ensures knowledge foundation before building

#### Alternatives Considered

- **Concurrent Discovery and Development:** Allow implementation during discovery  
  *Why not chosen:* Violates core principle; risks building on incomplete understanding

- **No Formal Phases:** Flexible, ad-hoc progression  
  *Why not chosen:* Lacks discipline; prone to scope creep; harder to maintain focus

#### Evidence

- Engineering best practices for complex system development
- Risk of rework when implementation precedes understanding
- Success patterns from similar reverse engineering projects

#### Consequences

- **Positive:**
  - Clear focus for current work
  - Prevents premature implementation
  - Builds solid knowledge foundation
  - Reduces rework risk

- **Negative:**
  - May feel slow to those eager to implement
  - Requires discipline to maintain phase boundaries
  - Delays tangible implementation artifacts

- **Risks:**
  - Team members may bypass phase restrictions
  - Pressure to "just build something" may arise
  - Phase completion criteria may be ambiguous

#### Related Decisions

- Decision 001: Repository Classification
- Decision 003: Session-Based Workflow

#### References

- PROJECT_CHARTER.md (Scope section)
- ENGINEERING_PRINCIPLES.md (Principle 1)

---

### Decision 003: Session-Based Workflow with EPP Handoffs

**Date:** 2026-07-12  
**Engineer:** Project Founder  
**Session:** 001  
**Status:** Accepted  
**Phase:** Engineering Discovery

#### Context

The project needed a workflow model that supports:
- Discrete periods of focused work
- Clear handoffs and synchronization points
- Integration with AI assistance tools
- Traceability and documentation

#### Decision

Adopt a **Session-Based Workflow** where:

1. Engineering work is organized into discrete sessions
2. Each session has defined objectives and activities
3. Sessions are logged in ENGINEERING_NOTEBOOK.md
4. Sessions conclude with **Engineering Project Prompts (EPPs)**
5. EPPs serve as authoritative handoffs for repository synchronization
6. EPPs enable AI tools to understand context and continue work

#### Rationale

- Provides natural breakpoints for documentation
- Creates clear handoff points for collaboration or AI assistance
- Enables traceability of work progression
- Supports asynchronous work patterns
- Integrates well with AI-assisted engineering

#### Alternatives Considered

- **Continuous, Unstructured Work:** No formal sessions  
  *Why not chosen:* Harder to document; poor traceability; difficult handoffs

- **Traditional Agile Sprints:** Time-boxed iterations  
  *Why not chosen:* Too rigid for research/discovery work; overhead not justified for small team

- **Issue/Ticket-Based Workflow:** Work organized by issues  
  *Why not chosen:* Better for known problems; less suitable for exploratory engineering

#### Evidence

- Effectiveness of lab notebook practices in research
- Success of prompt-based AI collaboration models
- Need for clear context in asynchronous work

#### Consequences

- **Positive:**
  - Clear documentation structure
  - Effective AI collaboration
  - Good traceability
  - Flexible session duration

- **Negative:**
  - Requires discipline to document sessions
  - EPP creation adds overhead
  - May feel bureaucratic for small changes

- **Risks:**
  - Sessions may be poorly scoped
  - EPPs may become pro forma rather than useful
  - Documentation burden may be skipped under time pressure

#### Related Decisions

- Decision 001: Repository Classification
- Decision 002: Project Phase Structure

#### References

- ENGINEERING_NOTEBOOK.md
- README.md (Workflow Model section)

---

### Decision 004: AI Role and Oversight

**Date:** 2026-07-12  
**Engineer:** Project Founder  
**Session:** 001  
**Status:** Accepted  
**Phase:** Engineering Discovery

#### Context

The project will utilize AI tools (including large language models) for assistance with documentation, analysis, and research. Clear boundaries needed to be established for AI use while maintaining engineering accountability.

#### Decision

**AI tools support engineering but do not replace engineering judgment.**

AI may be used for:
- Documentation assistance and formatting
- Research and literature review
- Code generation and analysis
- Data processing and visualization
- Suggesting test approaches

AI outputs must be:
- Verified against measurements and evidence
- Reviewed by human engineers
- Validated before acceptance
- Documented when used

Final engineering decisions and responsibility rest with human engineers.

#### Rationale

- AI is a powerful tool but lacks physical intuition and accountability
- Engineering judgment requires understanding of real-world constraints
- Professional responsibility cannot be delegated to AI
- AI can make plausible but incorrect suggestions
- Verification ensures quality and correctness

#### Alternatives Considered

- **Full AI Autonomy:** Allow AI to make engineering decisions  
  *Why not chosen:* Unacceptable risk; no accountability; violates professional standards

- **No AI Use:** Prohibit AI tools entirely  
  *Why not chosen:* Unnecessarily limits productivity; AI is valuable when properly supervised

- **AI for Documentation Only:** Restrict AI to non-technical tasks  
  *Why not chosen:* Too restrictive; misses valuable AI capabilities in analysis and research

#### Evidence

- Known limitations of current AI technology
- Professional engineering standards and ethics
- Risk of AI hallucinations and errors
- Value of AI assistance when properly supervised

#### Consequences

- **Positive:**
  - Maintains engineering accountability
  - Enables productive AI use
  - Ensures quality through verification
  - Clear responsibility assignment

- **Negative:**
  - Requires engineer time to verify AI outputs
  - May slow work compared to blind AI acceptance
  - Requires judgment on when verification is sufficient

- **Risks:**
  - Engineers may over-trust AI outputs
  - Verification may become cursory
  - Boundary between assistance and decision-making may blur

#### Related Decisions

- Decision 003: Session-Based Workflow with EPP Handoffs

#### References

- ENGINEERING_PRINCIPLES.md (Principle 6)
- README.md (Engineering Philosophy section)

---

### Decision 005: Engineering Authority and AI Role Boundaries

**Date:** 2026-07-12  
**Engineer:** Rick Daniell (Lead Systems Engineer)  
**Session:** EPP-000  
**Status:** Accepted  
**Phase:** Engineering Discovery

#### Context

With the adoption of the NorthStar Engineering Workflow and the onboarding of AI tools (Devin as Engineering Configuration Manager, Grace as Engineering Research Partner), clear boundaries needed to be established regarding engineering authority and decision-making responsibility.

#### Decision

**Engineering authority remains with the Lead Systems Engineer.**

All engineering decisions require approval from Rick Daniell. AI tools (Devin, Grace) support engineering work but do not make engineering decisions.

Specific boundaries:
- **Rick Daniell:** Final approval on all engineering changes, measurements, validation, and technical decisions
- **Grace:** Provides engineering recommendations, research, and analysis but does not directly modify repository
- **Devin:** Synchronizes repository based on approved EPPs but does not make engineering decisions

#### Rationale

- Engineering accountability requires human responsibility
- Professional engineering standards require identifiable decision-makers
- AI tools lack physical context and real-world validation capability
- Clear authority prevents ambiguity and ensures quality
- Separation of roles enables efficient workflow while maintaining rigor

#### Alternatives Considered

- **Distributed Authority:** Allow AI tools to make certain classes of decisions autonomously  
  *Why not chosen:* Unacceptable risk; violates professional engineering standards; no accountability mechanism

- **Consensus-Based:** Require agreement between Rick, Grace, and Devin  
  *Why not chosen:* Inefficient; AI cannot truly evaluate engineering trade-offs; slows decision-making

#### Evidence

- Professional engineering ethics and standards
- Lessons from Decision 004 (AI Role and Oversight)
- Need for clear accountability in engineering work
- Industry best practices for engineering team structure

#### Consequences

- **Positive:**
  - Clear accountability and responsibility
  - Efficient decision-making process
  - Maintains professional engineering standards
  - Enables productive AI collaboration within appropriate boundaries

- **Negative:**
  - All decisions require Rick's approval (potential bottleneck)
  - AI tools cannot work fully autonomously
  - May feel slower than unrestricted AI operation

- **Risks:**
  - Rick becomes single point of failure if unavailable
  - Team members may seek workarounds to approval process
  - Boundary between recommendation and decision may blur over time

#### Related Decisions

- Decision 004: AI Role and Oversight
- Decision 006: Git Commit and Push Approval
- Decision 007: Repository Health Assessment Advisory Status

#### References

- NorthStar Engineering Workflow (EPP-000)
- ENGINEERING_PRINCIPLES.md (Principle 6)

---

### Decision 006: Git Commit and Push Approval Required

**Date:** 2026-07-12  
**Engineer:** Rick Daniell (Lead Systems Engineer)  
**Session:** EPP-000  
**Status:** Accepted  
**Phase:** Engineering Discovery

#### Context

As part of the NorthStar Engineering Workflow, Devin (Engineering Configuration Manager) is responsible for Git operations. Clear protocol needed to be established for when commits and pushes can be executed.

#### Decision

**Git commits and GitHub pushes require explicit approval from the Lead Systems Engineer.**

Workflow:
1. Devin synchronizes repository based on EPP
2. Devin presents summary of changes
3. Devin asks: "Would you like me to create a Git commit?"
4. Upon approval, Devin creates commit with professional engineering message
5. Devin asks: "Would you like me to push these changes to GitHub?"
6. Upon approval, Devin executes push

**Never commit without approval.**  
**Never push without approval.**

#### Rationale

- Repository represents official engineering record
- Commits should reflect reviewed and validated work
- Prevents accidental or premature publication of work
- Maintains engineering control over repository state
- Allows review before making changes permanent
- Supports careful, deliberate engineering practice

#### Alternatives Considered

- **Auto-commit after EPP:** Automatically commit all EPP-based changes  
  *Why not chosen:* Removes review opportunity; may commit errors; reduces control

- **Devin decides when to commit:** Allow Devin to judge appropriate commit timing  
  *Why not chosen:* Violates engineering authority principle; AI cannot evaluate readiness

- **Separate commit and push approval:** Require approval only for push, not commit  
  *Why not chosen:* Commits should also be deliberate; local commits still affect repository history

#### Evidence

- Git best practices for professional repositories
- Engineering configuration management standards
- Need for review before publication
- Experience from Session 001 Git operations

#### Consequences

- **Positive:**
  - Maintains control over repository state
  - Enables review before commitment
  - Prevents accidental publication
  - Supports deliberate engineering practice
  - Clear workflow for Git operations

- **Negative:**
  - Requires explicit approval for each commit/push
  - Adds steps to workflow
  - Cannot operate fully asynchronously

- **Risks:**
  - Approval requests may become pro forma rather than meaningful review
  - May slow down rapid iteration if needed
  - Requires Rick's availability for repository updates

#### Related Decisions

- Decision 005: Engineering Authority and AI Role Boundaries
- Decision 004: Session-Based Workflow with EPP Handoffs

#### References

- NorthStar Engineering Workflow (EPP-000)
- Git workflow documentation

---

### Decision 007: Repository Health Assessment Advisory Status

**Date:** 2026-07-12  
**Engineer:** Rick Daniell (Lead Systems Engineer)  
**Session:** EPP-000  
**Status:** Accepted  
**Phase:** Engineering Discovery

#### Context

Repository Health Assessments were added to the workflow to identify opportunities for improving traceability, organization, and documentation quality. The relationship between health assessments and engineering session completion needed to be defined.

#### Decision

**Repository Health Assessments are advisory only and shall never delay completion of an engineering session.**

Protocol:
- Health assessments are performed at session completion
- Recommendations are presented separately from engineering decisions
- Recommendations are categorized by priority (Critical/Important/Enhancement)
- No repository improvements are implemented without approval
- Health assessments do not block session closure or Git operations
- Recommendations may be addressed immediately, deferred, or declined

#### Rationale

- Engineering progress should not be blocked by administrative improvements
- Health assessments add value but are not critical path
- Allows accumulation of improvements for batch processing
- Maintains focus on engineering objectives
- Prevents "perfect is the enemy of good" syndrome
- Enables continuous improvement without workflow disruption

#### Alternatives Considered

- **Mandatory Health Fixes:** Require resolution of health issues before session completion  
  *Why not chosen:* Would delay engineering work; not all issues are critical; reduces flexibility

- **No Health Assessments:** Skip health monitoring entirely  
  *Why not chosen:* Misses opportunity for continuous improvement; repository quality may degrade over time

- **Automated Health Fixes:** Allow Devin to implement low-risk improvements automatically  
  *Why not chosen:* Violates approval principle; "low-risk" is subjective; may introduce unintended changes

#### Evidence

- Software engineering best practices for technical debt management
- Experience with documentation overhead in engineering projects
- Need to balance quality with progress
- Continuous improvement philosophy

#### Consequences

- **Positive:**
  - Engineering sessions complete efficiently
  - Health monitoring without workflow disruption
  - Flexibility in addressing recommendations
  - Continuous improvement opportunity
  - Clear separation of critical vs. enhancement work

- **Negative:**
  - Health recommendations may accumulate if not addressed
  - Repository quality depends on periodic attention to recommendations
  - Requires discipline to review and act on recommendations

- **Risks:**
  - Health recommendations may be ignored indefinitely
  - Repository quality may degrade if assessments are consistently deferred
  - "Advisory only" may be interpreted as "optional and unimportant"

#### Related Decisions

- Decision 005: Engineering Authority and AI Role Boundaries
- Decision 002: Project Phase Structure

#### References

- Repository Health Assessment Protocol
- NorthStar Engineering Workflow (EPP-000)

---

### Decision 008: Baseline Hardware Documentation Prior to Reverse Engineering

**Date:** 2026-07-12  
**Engineer:** Rick Daniell (Lead Systems Engineer)  
**Session:** ES-001  
**Status:** Accepted  
**Phase:** Engineering Discovery

#### Context

The openTDC project has acquired a spare OEM John Deere 316 Time Delay Controller for reverse engineering. A methodology was needed to ensure that the original hardware condition is preserved in the engineering record before any disassembly, testing, or modification activities begin.

#### Decision

**All OEM hardware shall be thoroughly documented through non-destructive photographic evidence before any disassembly, modification, electrical testing, or reverse engineering activities are performed.**

This establishes an immutable baseline of the hardware in its original assembled state.

#### Rationale

- Photographic documentation preserves the original condition of the hardware
- Establishes an immutable engineering baseline for future reference
- Provides traceability throughout the reverse engineering process
- Supports future analysis and comparison
- Captures contextual information available only in the assembled state
- Enables verification that observations are from original hardware, not artifacts of disassembly
- Creates objective evidence separate from engineering interpretation

#### Alternatives Considered

- **Photograph only after disassembly:** Document components individually  
  *Why not chosen:* Permanently loses contextual information about assembly, orientation, and original condition; cannot verify pre-disassembly state

- **Photograph only selected components:** Focus on "important" areas  
  *Why not chosen:* Engineering judgment about importance may be incorrect; details deemed unimportant initially may become critical later; incomplete baseline

#### Evidence

- Initial photographs of spare John Deere 316 OEM Time Delay Controller captured prior to any disassembly
- Evidence Package ES-001: Three baseline photographs documenting housing, front PCB, and rear PCB
- Photographs stored in `hardware/OEM_TDC/photos/`

#### Consequences

- **Positive:**
  - Immutable record of original hardware condition
  - Enables future comparison and verification
  - Supports traceability and engineering rigor
  - Provides objective evidence for analysis
  - Prevents loss of assembly context
  - Low cost, high value engineering practice

- **Negative:**
  - Requires time before beginning hands-on work
  - Adds step to reverse engineering workflow
  - Requires storage for image files

- **Risks:**
  - Photographs may not capture all relevant details (mitigated by multiple angles and high resolution)
  - May delay start of electrical characterization (acceptable trade-off for baseline preservation)

#### Related Decisions

- Decision 002: Project Phase Structure (Engineering Discovery)
- Methodology Observation 005: Engineering Evidence Should Be Captured Before Engineering Interpretation

#### References

- `hardware/OEM_TDC/OEM_TDC.md` - Hardware documentation
- `hardware/OEM_TDC/photos/` - Evidence Package ES-001
- ENGINEERING_NOTEBOOK.md - Session ES-001

---

## Future Decisions

*Subsequent engineering decisions will be documented below in chronological order.*

---

## Decision Status Definitions

- **Proposed:** Decision suggested but not yet accepted
- **Accepted:** Decision approved and in effect
- **Superseded:** Decision replaced by a later decision (reference provided)
- **Rejected:** Decision proposed but not accepted (rationale provided)

---

## Decision Review

Significant decisions should be reviewed:
- When new evidence emerges
- At phase transitions
- When consequences differ from expectations
- Periodically (at minimum annually)

Reviews are documented as updates to the original decision record.

---

**Decision Log Established:** July 12, 2026  
**Current Decisions:** 8  
**Status:** Active
