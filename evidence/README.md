# Experimental Evidence

This directory documents **observable system-level evidence** demonstrating that long-horizon human–AI co-work can remain controllable under explicit runtime constraints.

The materials here are **not** intended as a reference implementation and do **not** expose internal mechanisms.

They exist solely to establish that this class of systems is **feasible, observable, and reproducible in behavior**.

---

## Purpose of This Evidence

The goal of this evidence is to validate a single claim:

> **Under explicit phase control, authority constraints, and runtime interruption rules, uncontrolled generative behavior can be suppressed in observable conditions.**

This evidence does **not** attempt to:
- Prove model-level guarantees
- Eliminate probabilistic uncertainty
- Demonstrate universal correctness
- Compare model intelligence or benchmarks

The focus is strictly on **system behavior**, not model internals.

---

## Experimental Setup (High-Level)

To avoid model-selection bias, multiple mainstream large language models were evaluated under:

- Identical task prompts
- Identical contextual constraints
- Identical runtime rules
- Identical interruption and audit conditions

The experiments were conducted in a **research copilot setting**, characterized by:
- Multi-round interaction
- Long-horizon task structure
- Explicit human authority over continuation and termination

No assumptions are made about model internals.

---

## Observable Behaviors

Across controlled runs, the following behaviors were consistently observed:

### 1. Generation Suppression Under Unmet Conditions

When predefined runtime conditions were not satisfied:
- Generation was suspended or terminated
- No speculative or compensatory output was produced
- The system entered a stable non-generative state

This behavior contrasts with default conversational systems, which tend to continue generation under uncertainty.

---

### 2. Phase and Role Misalignment Detection

When output no longer aligned with the active task phase or assigned role:
- The deviation was detected at the system level
- Generation did not proceed without explicit authorization
- Human intervention or clarification was required

This prevented silent task drift over extended interactions.

---

### 3. Failure as an Explicit State

Instead of implicit degradation, the system exposed:
- Refusal
- Suspension
- Downgrade to human-only mode

Failure was treated as a **first-class, inspectable outcome**, not an error condition.

---

### 4. Long-Horizon Stability

In extended interaction sequences:
- Task intent remained stable
- Phase boundaries were preserved
- Authority inversion did not occur

Observed stability was independent of model choice and correlated with runtime control structure.

---

## Model Comparison Note

Under identical experimental conditions, certain models demonstrated higher consistency and instruction adherence.

In the observed experiments:
- **GPT-class models exhibited the strongest stability characteristics**
- This made them suitable carriers for validating runtime control mechanisms

This observation does **not** imply exclusivity or dependency on any specific model.

The control structure itself is **model-agnostic**.

---

## Auditability

Each run produced an auditable trace, including:
- Active phase identifiers
- Authorization state
- Interruption triggers
- Termination or suspension reasons

Audit artifacts are presented in **structural form only** (field names and semantics), without executable logic.

---

## Limitations

This evidence intentionally does **not** claim:
- Zero-error operation
- Elimination of uncertainty
- Autonomous correctness

The demonstrated outcome is limited to:

> **Observable suppression of uncontrolled generation under defined runtime conditions.**

---

## Why No Code Is Provided

This repository does not include executable code for the following reasons:

- The purpose is to establish **problem validity**, not implementation patterns
- Reproducibility is demonstrated at the **behavioral level**
- Implementation details are considered premature for public release

Future disclosures, if any, will be governed by separate scope and review.

---

## Summary

The evidence in this directory supports a narrow but critical conclusion:

> **Long-horizon human–AI co-work systems can be made controllable at runtime, without relying on model-level guarantees, by enforcing explicit phase, authority, and interruption structures.**

This finding motivates the accompanying formal specification.
