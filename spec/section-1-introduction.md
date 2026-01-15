# Section 1 — Introduction

## 1.1 Background

As large language models (LLMs) have become increasingly capable, they are being applied to tasks involving extended interaction, complex reasoning, and collaborative problem-solving.

However, experience across research, engineering, and decision-support domains has revealed persistent failures in **long-horizon human–AI collaboration**, including:

- Progressive drift from the original task intent
- Ambiguity in authority between human operators and AI systems
- Continued generation under uncertainty or incomplete conditions
- Failures that are implicit, non-auditable, or only detectable after outcomes occur

These failures are frequently attributed to limitations in model capability or probabilistic uncertainty.  
This specification adopts a different position:

> **The dominant failure modes in long-horizon human–AI co-work are systemic, not model-centric.**

They arise from the absence of explicit phase control, authority boundaries, and failure semantics at the system level.

---

## 1.2 Problem Statement

Current AI application paradigms—such as conversational interfaces, retrieval-augmented generation, and agent-based workflows—are primarily optimized for **short-horizon, low-responsibility interactions**.

When applied to scenarios where responsibility cannot be externalized, these paradigms exhibit structural weaknesses:

- Tasks lack explicit phase boundaries
- Transitions occur implicitly through conversational flow
- Authority over continuation and termination is ambiguous
- Failure is treated as degraded output rather than a first-class state

As a result, systems tend to **continue generating** when they should instead suspend, refuse, or return control to human operators.

This specification addresses the absence of a formal framework for governing **human–AI co-work under responsibility constraints**.

---

## 1.3 Scope of This Specification

This specification defines a class of systems referred to as **Human–AI Co-Work Systems**.

It applies to scenarios characterized by one or more of the following properties:

- Long-horizon, multi-round interaction
- Non-reversible or high-impact outcomes
- The requirement for auditability and accountability
- Explicit human responsibility for final decisions

Examples include research assistance, high-stakes analysis, and extended decision-support processes.

This specification does **not** target:
- Consumer-facing or casual AI usage
- Low-responsibility, reversible interactions
- Model training, fine-tuning, or inference optimization
- Claims of model-level correctness or hallucination elimination

---

## 1.4 Design Philosophy

The design principles underlying this specification are as follows:

### Phase-First, Not Capability-First

System stability depends on explicit recognition of task phases and permissible actions within each phase, rather than on increased model intelligence.

### Failure-First, Not Success-Driven

Refusal, suspension, and uncertainty are valid and necessary system outcomes.  
A system that cannot stop safely is considered incomplete.

### Authority Separation, Not Orchestration Convenience

Human operators retain authority over:
- Phase transitions
- Execution authorization
- Termination and publication decisions

AI components operate strictly within delegated roles.

### Systems Over Tools

Long-horizon human–AI collaboration requires structural guarantees that cannot be provided through prompts, workflows, or tool chaining alone.

---

## 1.5 Non-Goals and Explicit Exclusions

This specification explicitly excludes:

- Autonomous final decision-making by AI systems
- Implicit or hidden phase transitions
- Undocumented memory mutation across interactions
- Guarantees of outcome correctness or completeness
- Replacement of existing AI application paradigms

The intent is to **define boundaries**, not to prescribe implementations.

---

## 1.6 Relationship to Experimental Evidence

The accompanying experimental evidence demonstrates that:

- Uncontrolled generative behavior can be suppressed under explicit runtime constraints
- Long-horizon stability correlates with phase and authority control
- Failure can be exposed as an explicit, inspectable system state

This specification provides the **conceptual and structural foundation** necessary to interpret that evidence, without constraining implementation choices.

---

## 1.7 Status of This Document

This section constitutes an **initial normative definition** of the problem domain addressed by Human–AI Co-Work systems.

Subsequent sections will define:
- Core concepts and terminology
- State machine semantics
- Authority and transition rules

This document is intended to evolve through structured revision and review.
