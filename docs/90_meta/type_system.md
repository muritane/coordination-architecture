# The Load-Bearing Stack as a Type System  
## A Structural Typing Discipline for Bounded Execution Under Drift

---

## Status and Intent

This document defines the **Load-Bearing Stack** as a **type system** for reasoning about action, evaluation, agency, responsibility, optimization, and governance in **bounded, irreversible, drifting systems**.

It functions as a **static checker** for discourse about execution.

It does not determine what is true, good, optimal, or legitimate.
It determines whether a claim is **well-formed** with respect to executional constraint.

The system:

- rejects **ill-typed claims** (category errors),
- marks **under-typed claims** where executional witnesses are missing,
- forces explicit horizons, resources, and causal assumptions,
- preserves reinterpretation without allowing it to masquerade as execution.

---

## Core Stance

All claims are **conditional on an epistemic context**.

No statement about action, responsibility, or optimization is meaningful
without specifying the constraints under which it is supposed to hold.

Every claim is typed relative to:

- what is observed,
- how consequences propagate,
- which horizons matter,
- and which resources are finite.

---

## Epistemic Context (Typing Environment)

A typing environment bundles the minimum structure required to type-check executional claims.

Let:

- **E** — current observations and measurement quality (including blind spots),
- **T̂** — a provisional topology model of consequence propagation  
  (latency, fan-out, buffers, observability, irreversibility gradients),
- **H** — one or more horizons over which viability is evaluated,
- **R** — bounded resources and remaining margin.

**Typing rule (global):**  
If a claim does not specify or imply `(E, T̂, H, R)`, it is usually **under-typed**.

Under-typed does not mean false.  
It means **non-executable as a statement about bounded systems**.

---

## Terms and Objects

The type system reasons over the following objects:

- **State** — world or system configurations.
- **Act** — actions that induce state transitions.
- **Policy** — rules for action selection.
- **Closure** — lossy compression that terminates interpretation.
- **Metric** — executable evaluative interface inside a closure.
- **Boundary** — a pre-execution decision point.
- **FailureMode** — how breakdown occurs and where load lands.

These are structural terms, not moral ones.

---

## Primitive Types

Primitive types describe **executional roles**, not human qualities.

- **Exec** — irreversible execution.
- **Interp** — interpretation, narrative, justification.
- **Topo** — consequence topology.
- **Horiz** — horizon specification.
- **Res** — bounded resources.
- **Viable** — continued execution remains possible.
- **ClosureOK** — closure sufficient under current context.
- **MetricOK** — metric valid and explicitly failing.
- **Decidable** — refusal and acceptance are both executable.
- **AgencyOK** — agency attribution is coherent.
- **RespOK** — responsibility attribution is coherent.

---

## Claim Kinds (What Is Being Asserted)

Claims are typed by *what they are trying to be*:

- **Execution claims** — “X caused Y.”
- **Interpretive claims** — “X intended / meant / justified.”
- **Evaluation claims** — “X is good/bad by criterion C.”
- **Optimization claims** — “Optimizing O improves the system.”
- **Agency claims** — “Actor A chose freely.”
- **Responsibility claims** — “Actor A is responsible for outcome Y.”

Typing errors arise primarily from **claim-kind confusion**.

---

## Judgment Outcomes (Three-Valued)

Every claim type-checks as one of:

- **Well-Typed** — structurally coherent under `(E, T̂, H, R)`,
- **Ill-Typed** — violates executional constraints (category error),
- **Under-Typed** — insufficient structure to evaluate.

This third category is essential: most discourse fails by **missing witnesses**, not by being wrong.

---

## Structural Axioms (Non-Negotiable)

These are invariants for bounded executors:

1. **Irreversibility** — execution destroys information and eliminates alternatives.
2. **Boundedness** — resources are finite; full sensing is impossible.
3. **Drift** — causal structure changes; invariants are horizon-bound.
4. **Unavoidable compression** — executable representations are lossy.
5. **Viability precedes optimization** — improvement is undefined without survival.

Any framework that assumes reversibility, infinite resources, or lossless abstraction is **ill-typed by construction**.

---

## Typing Rules (Selected)

### Execution vs Interpretation

A claim that references only intent, meaning, or justification cannot be typed as execution.

Interpretation does not execute.

Statements like “we decided” or “we value” are **execution-inert** unless they bind closures, metrics, or boundaries.

---

### Viability Gate for Optimization

Optimization claims are typeable **only if viability is established** over the declared horizons.

If survival is failing or undefined, optimization talk is ill-typed.

Optimization without a viability witness is not wrong — it is **undefined**.

---

### Closure Typing

A closure is acceptable only if:

- it is executable within resource bounds,
- it preserves viability across horizons under current topology,
- it has a bounded redesign or escape path.

Closures that once worked may become ill-typed under drift.

---

### Metric Typing

A metric is valid only if it:

- encodes the minimal necessary degrees of freedom,
- is computable under resource bounds,
- yields determinate outcomes,
- and **fails explicitly** outside its envelope.

Metrics that never fail loudly are **ill-typed as coordination interfaces**.
They silently accumulate error.

---

### Decidability

A boundary is decidable only if refusal is an executable path with bounded consequences.

If refusal exists only narratively, agency claims at that boundary are ill-typed.

---

### Agency Attribution

Agency is typeable only at **decidable boundaries** with refusal symmetry.

If one party can refuse without catastrophe and another cannot, attributing agency symmetrically is ill-typed.

Post-execution, only discretion exists — not agency.

---

### Responsibility Attribution

Responsibility is typeable only when:

- a closure is settled or explicitly binding,
- metrics are valid and failure-bearing,
- entry into execution was decidable,
- outcomes depend on controllable variables,
- and load routing is legible in the topology.

Responsibility follows **load-bearing paths**, not narrative involvement.

---

## Drift and Retyping

Types are not permanent.

As observations update or topology shifts:

- previously well-typed claims may become ill-typed,
- metrics may silently saturate,
- closures may lose sufficiency.

Redesign is **retyping**:
reopening distinctions, adjusting horizons, changing metrics, or relocating boundaries.

No type can fully specify its own retyping rules from inside itself.

---

## Common Ill-Typed Patterns

- **Agency laundering** — attributing choice where refusal was non-executable.
- **Optimization without viability** — improving metrics while survival erodes.
- **Silent metric saturation** — metrics that never fail, only drift.
- **Horizon mismatch** — short-horizon evaluation destroying long-horizon viability.
- **Hidden subsidy stability** — apparent robustness dependent on unmodeled buffers.

These are structural errors, not moral ones.

---

## Where Values Appear (Descriptively)

Values become execution-relevant only when they:

- constrain closure selection,
- define metric envelopes,
- allocate redesign authority,
- preserve refusal executability.

Otherwise, values remain interpretive claims — real, but execution-inert.

---

## Closing Compression

The Load-Bearing Stack is a type system for execution.

It does not tell you what to want.
It tells you when what you are saying **could possibly be true** for a bounded executor.

Only claims that survive:

- irreversibility,
- bounded resources,
- drift,
- explicit closure,
- executable metrics,
- decidable boundaries,

are well-typed as statements about action.

Everything else remains interpretation —
not invalid,
but unbound.
