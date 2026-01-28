# Decidability, Degrees of Freedom, and Agency in Load-Bearing Systems

## A Structural Account of Boundary Consent, Constraint Collapse, and Binding Participation

---

## Status

This document presents a **structural and architectural account of agency** in load-bearing systems.

Agency is treated as a **topological property of boundary decisions under constraint**, not as:
- a psychological trait,
- an expression of preference,
- a moral quality,
- a claim about intent or virtue,
- or a narrative of resistance.

The account is **descriptive, mechanical, and non-normative**.  
It specifies when agency exists, when it does not, and when claims of responsibility assignment are structurally valid.

---

## Scope and Level of Abstraction

This document operates at the level of **system topology and execution boundaries**, not lived experience.

It applies to any domain that:
- coordinates independent agents,
- allocates shared resources,
- substitutes operators or evaluators,
- propagates failure across boundaries,
- or commits irreversible action under load.

Examples include hardware interfaces, protocols, markets, institutions, evaluation systems, and regulatory regimes.

---

## Core Definition of Agency

**Agency** is defined as:

> the capacity to make a **binding yes/no decision** at a declared boundary of a **load-bearing substrate**, with explicit knowledge of which constraints, interfaces, invariants, and failure semantics will apply upon entry.

Agency is not freedom from constraint.  
Agency is **decidability over which constraints one binds oneself to**.

---

## What This Document Is Not

This document does **not**:

- claim all participation is voluntary,
- deny coercion or asymmetry,
- justify existing power structures,
- equate consent with fairness,
- moralize compliance or refusal,
- assert that exit is always possible,
- or claim systems are just.

It makes one claim only:

> **Binding participation requires a real, declared boundary decision.**

---

## The Structural Claim

In load-bearing systems:

> **Agency exists at boundaries, not inside execution.**

Once an agent crosses a boundary and enters execution:

- interpretation terminates,
- invariants apply,
- routing rules hold,
- buffers are owned,
- failure semantics are fixed,
- renegotiation is invalid.

Inside execution, behavior is not agency.  
It is **execution under declared constraints**.

---

## Decidability as the Minimal Form of Agency

Agency reduces to **decidability**:

- the ability to say **yes**,
- the ability to say **no**,
- with **known, bounded consequences** for each.

Anything less is not agency.  
Anything more is exploration or negotiation.

A boundary decision is **not decidable** if:

- refusal carries unbounded or undefined cost,
- constraints are implicit or revealed only after entry,
- interfaces are underspecified,
- failure semantics are retroactive,
- or obligations expand post hoc.

Decidability is a *minimal* definition of agency in load-bearing contexts.  
It is not an exhaustive account of human action.

---

## Participation as Topological Binding

To participate in a load-bearing substrate is to bind oneself to:

- declared interfaces,
- enforced invariants,
- specified inputs and outputs,
- explicit buffer ownership,
- authority and escalation paths,
- known failure and refusal semantics.

This binding is **structural**, not interpersonal.

Participation is a contract with the **topology**, not with individual actors.

---

## Degrees of Freedom (DOFs) as the Operator of Agency

Decidability is meaningless unless the system declares **which degrees of freedom collapse at entry**.

A system can only claim agency-valid consent if it explicitly classifies task-relevant DOFs at the boundary.

### DOF Classes at Entry

For any load-bearing task, degrees of freedom fall into the following classes:

#### Essential DOFs
- Fixed at entry.
- Required for correctness and substitutability.
- Enforced during execution.
- Reinterpretation is invalid.

These DOFs define what participation *means*.

---

#### Optional DOFs
- Delegated at entry within declared bounds.
- Variation is permitted, but only within scope.
- Control is explicitly assigned.

Optional DOFs are agency-preserving **only if declared**.

---

#### Latent DOFs
- Explicitly preserved for future regimes.
- Not binding in the current execution context.
- Activated only via version change.

Latent DOFs preserve adaptability across time.

---

#### Irrelevant DOFs
- Declared non-contributory.
- Collapsed explicitly.
- Cannot be used to dispute outcomes.

---

#### Unknown DOFs
- Not yet characterized.
- Excluded from responsibility assignment.
- Must remain outside load-bearing execution.

Unknown DOFs cannot ground consent or blame.

---

## Agency-Grade Boundary Declaration

A boundary supports agency **iff** it declares:

1. Which DOFs are Essential and fixed at entry.
2. Which DOFs are Optional and delegated.
3. Which DOFs are Latent and versioned.
4. Which DOFs are Irrelevant and collapsed.
5. Which DOFs are Unknown and excluded.

If this partition is absent or misleading, **agency is not present**, regardless of narrative choice.

---

## Hardware as the Canonical Example

A hardware component illustrates this mechanically:

- A RAM module selects a standard (e.g. DDR generation).
- By doing so, it accepts:
  - voltage levels,
  - timing constraints,
  - signaling protocols,
  - error behavior,
  - compatibility limits.

The act of insertion is the act of agency.

After insertion:
- Essential DOFs are fixed,
- renegotiation is impossible,
- refusal manifests as non-function.

This is not punishment.  
It is **topological incompatibility**.

---

## Markets and Institutions as Load-Bearing Substrates

Markets, standards bodies, and institutions function the same way when hygienic.

Participation binds an actor to:

- specification requirements,
- compliance thresholds,
- liability assignment,
- buffer ownership (time, capital, inventory),
- evaluation and refusal mechanisms.

When DOFs are explicit:
- entry is meaningful,
- responsibility is legible,
- failure is localized.

When DOFs are implicit:
- agency is retroactively asserted,
- responsibility is moralized,
- buffers are silently captured.

---

## False Agency Patterns (Structural Failures)

### 1. Post-Hoc Reinterpretation

> “I agreed, but not to *this* consequence.”

Structurally:
- an Essential DOF fixed at entry is being reclassified after execution,
- interpretation is being reopened after topology hardened.

This is valid only in exploratory regimes.

In load-bearing execution, this is a **denial of topology**, not an exercise of agency.

---

### 2. Coerced Entry Disguised as Choice

> “You are free to refuse, but refusal carries unlimited penalty.”

Here:
- refusal semantics are unbounded,
- Essential DOFs are undeclared,
- the system is already load-bearing while pretending to be exploratory.

This is not agency.  
It is forced participation with moral cover.

---

## Responsibility Without Moralization

Under this model:

- responsibility is not blame,
- responsibility is **load location**.

Responsibility is assignable **only** for outcomes dependent on DOFs that were:

1. Declared Essential or Optional at entry, and
2. Within the agent’s assigned control scope.

If harm arises from:
- Unknown DOFs,
- misclassified DOFs,
- latent DOFs that later collapse,
- or misrepresented constraints,

then responsibility was misrouted.

No moral language is required to establish this.

---

## Constraint Discovery and the End of Negotiation

Constraint discovery explains **when** invariants become unavoidable under load.

Agency explains **who is legitimately bound once they do**.

Constraint discovery without decidability produces coercion.  
Decidability without constraint discovery produces illusion.

Negotiation belongs **before** entry.  
Execution belongs **after**.

---

## Exit, Versioning, and Temporal Agency

Agency across time requires not only entry, but **bounded exit or versioning**.

Healthy systems declare:

- compatibility horizons,
- end-of-life timelines,
- migration paths,
- which DOFs may change and when.

Versioning is the mechanism by which:

- Essential DOFs are allowed to reclassify,
- consent is refreshed rather than fossilized,
- specialization is bounded in time.

Without versioning:
- latent DOFs collapse silently,
- consent becomes permanent,
- participation becomes entrapment.

---

## Summary (Compressed)

- Agency is boundary decidability.
- Decidability requires explicit DOF classification.
- Participation binds to topology, not intent.
- Inside execution, reinterpretation is invalid.
- Responsibility follows declared DOF control.
- Coercion is undeclared load-bearing entry.
- Versioning preserves agency across time.
- Moral language often substitutes for missing boundaries.

---

## Closing Note

Agency is not freedom from constraint.

It is the freedom to choose **which constraints to bind oneself to**,  
under **declared degrees of freedom**,  
with **honest refusal semantics**,  
before execution begins.

Load-bearing systems do not eliminate agency.  
They require it to be **explicit, bounded, and mechanically real**.
