# openTDC

**Open Engineering Repository for the John Deere 316 Time Delay Controller**

---

## Repository Purpose

This is an **engineering knowledge repository**, not a software development project.

The openTDC repository exists to document, preserve, and organize the complete engineering process involved in understanding, reverse engineering, validating, and modernizing the John Deere 316 Time Delay Controller (TDC).

Software, hardware, PCB design, and firmware are considered **engineering artifacts**—not the primary objective. This repository prioritizes engineering knowledge, methodology, and decision-making over code.

---

## Engineering Philosophy

This project is guided by the following principles:

- **Understand before redesign** — Reverse engineering precedes forward engineering.
- **Measure before concluding** — Data and evidence drive decisions.
- **Evidence outweighs opinion** — Engineering conclusions must be reproducible and traceable.
- **Preserve OEM behavior before introducing enhancements** — The original design is respected and documented.
- **Engineering decisions must be traceable** — All decisions are recorded with context and rationale.
- **AI supports engineering but does not replace engineering judgment** — Tools assist; engineers decide.

---

## Current Project Phase

**Engineering Discovery**

This phase focuses on:
- Understanding the original TDC design
- Reverse engineering hardware and firmware
- Documenting OEM behavior through bench testing
- Establishing baseline measurements and observations
- Building a foundation of engineering knowledge

**No firmware development, PCB redesign, or hardware redesign is currently authorized.**

---

## Repository Structure

```
openTDC/
├── README.md                          # This file
├── PROJECT_CHARTER.md                 # Project scope, objectives, and governance
├── ENGINEERING_PRINCIPLES.md          # Detailed engineering philosophy and standards
├── ENGINEERING_NOTEBOOK.md            # Chronological engineering session log
├── ENGINEERING_DECISIONS.md           # Decision records with rationale
├── CHANGELOG.md                       # Repository and project change history
├── METHODOLOGY_OBSERVATIONS.md        # Lessons learned and process improvements
│
├── docs/                              # Supporting documentation
├── bench/                             # Bench test procedures and results
├── photos/                            # Engineering photographs and visual documentation
├── hardware/                          # Hardware artifacts and documentation
├── firmware/                          # Firmware artifacts and reverse engineering notes
├── schematics/                        # Circuit diagrams and PCB layouts
├── research/                          # Background research and reference materials
└── releases/                          # Formal engineering release packages
```

---

## Workflow Model

This repository operates on an **Engineering Session** model:

1. **Engineering sessions** are discrete periods of focused engineering work
2. Each session concludes with an **Engineering Project Prompt (EPP)**
3. EPPs serve as authoritative engineering handoffs for repository synchronization
4. All work is traceable through session logs and decision records

---

## Repository Classification

**This is an Engineering Configuration Repository**, not a software repository.

It is maintained with the same rigor as engineering documentation in regulated industries:
- Version controlled
- Peer reviewable
- Traceable to source decisions
- Maintained for long-term reference

---

## Getting Started

1. Review `PROJECT_CHARTER.md` for project scope and objectives
2. Read `ENGINEERING_PRINCIPLES.md` for detailed standards and practices
3. Consult `ENGINEERING_NOTEBOOK.md` for session history
4. Reference `ENGINEERING_DECISIONS.md` for context on past decisions

---

## Contributing

All contributions must align with the engineering philosophy and current project phase.

Before contributing:
- Understand the current phase constraints
- Review existing engineering decisions
- Document your work in the engineering notebook
- Provide evidence and rationale for all conclusions

---

## License

*To be determined based on project governance decisions.*

---

## Contact

*Project maintainer and contact information to be added.*

---

**Repository Established:** July 12, 2026  
**Current Phase:** Engineering Discovery  
**Repository Type:** Engineering Configuration Repository
