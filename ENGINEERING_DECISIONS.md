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
**Current Decisions:** 4  
**Status:** Active
