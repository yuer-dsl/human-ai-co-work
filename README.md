# human-ai-co-work
Specifications and experimental evidence for long-horizon human–AI co-work systems, focusing on phase control, authority boundaries, and failure-first design.

This repository documents an emerging class of systems designed for **long-horizon human–AI co-work**, where responsibility cannot be delegated, failure must be observable, and generation must remain interruptible.

It contains:
- Experimental evidence demonstrating the feasibility of controlled long-horizon AI collaboration
- A formal specification defining the problem space and system boundaries
- Design principles for phase-aware, authority-bounded, failure-first human–AI systems

This repository is **not** a reference implementation and does **not** provide executable code.

---

## Background

As large language models become increasingly capable, their limitations in **long-horizon, high-responsibility scenarios** have become more visible:

- Multi-round interactions drift from the original task intent
- Authority boundaries between humans and AI become ambiguous
- Systems continue generating output under uncertainty instead of stopping
- Failures are implicit, non-auditable, and hard to attribute

These issues are not primarily model-capability problems.  
They are **system-design problems**.

---

## What This Repository Is About

This project focuses on a specific problem domain:

> **Human–AI co-work systems where responsibility cannot be externalized.**

Examples include (but are not limited to):
- Research assistance and scientific reasoning
- High-stakes decision support
- Long-horizon analytical collaboration
- Systems requiring auditability and explicit failure handling

In such scenarios, correctness alone is insufficient.  
Systems must be able to:
- Detect phase or role misalignment
- Interrupt or suspend generation when conditions are not met
- Preserve human authority over transitions and outcomes
- Expose failure as a first-class, inspectable state

---

## What This Repository Is *Not*

To avoid ambiguity, this repository explicitly does **not** aim to:

- Replace existing AI application paradigms (RAG, agents, prompt engineering)
- Optimize consumer-facing or low-responsibility AI experiences
- Provide a general-purpose AI safety framework
- Claim the existence of “hallucination-free” models

Existing approaches remain effective and appropriate in **low-responsibility, reversible-use scenarios**.

This work applies only where **responsibility cannot be offloaded to probabilistic generation**.

---

## Structure of the Repository

/
├── README.md # This document
├── evidence/ # Experimental evidence and observable behaviors
│ └── README.md
├── spec/ # Formal specifications
│ └── section-1-introduction.md


### `/evidence`
Contains **experimental evidence** demonstrating that, under explicit runtime control and phase constraints, uncontrolled generative behavior can be suppressed in observable conditions.

This evidence focuses on **system behavior**, not implementation details.

### `/spec`
Contains formal specifications defining:
- The problem domain
- System scope and non-goals
- Core design philosophy

Specifications are written in a **normative, implementation-agnostic** style.

---

## Design Philosophy

This work is guided by several foundational principles:

- **Phase-first, not capability-first**  
  System stability depends on explicit phase control, not stronger models.

- **Failure-first, not success-driven**  
  Refusal, suspension, and uncertainty are valid system outcomes.

- **Authority separation, not convenience orchestration**  
  Humans retain transition and termination authority.

- **Systems over tools**  
  Long-horizon collaboration requires structural guarantees, not prompt-level tuning.

---

## Status

This repository represents an **early-stage public disclosure** of:
- A validated problem domain
- Experimental evidence of feasibility
- A formalized system boundary

Detailed mechanisms, implementations, and extensions are intentionally out of scope at this stage.

---

## License

No license is granted at this time.

This repository is published for the purposes of:
- Technical discussion
- Problem-domain definition
- Standards-oriented exploration

---

## Contact

For research discussion or collaboration inquiries:

**Author:** yuer  
**Project context:** EDCA OS (Expression-Driven Cognitive Architecture)



