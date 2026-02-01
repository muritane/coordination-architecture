# Horizon-Bounded Validity and Redesign-Safe Abstractions

## Status and Intent

This document describes a **minimal set of invariants** required for representations,
models, or abstractions to remain **redesign-safe** under execution and time.

It does not propose complete models, optimal abstractions, or continuous adaptability.

It specifies only what must remain **present or recoverable** so that:
- invalidated assumptions can be detected,
- reinterpretation can terminate,
- and redesign remains *possible* rather than catastrophic.

The perspective is **architectural and descriptive**, not epistemic or normative.

---

## Core Claim

All executable abstractions are **horizon-bounded compressions**.

They become unsafe not when they are false,
but when they are treated as **horizon-independent** after their validity envelope expires.

Redesign failure occurs when abstractions eliminate the very variables
required to notice their own invalidation.

---

## Validity Is Not Truth

In this document, **validity** refers to:

> sufficiency of an abstraction to support execution  
> without violating invariants required for persistence  
> over a specified horizon.

An abstraction may be:
- true but invalid (correct but unusable),
- valid but incomplete,
- or valid only within a narrow regime.

Validity is **relative to execution, topology, and time**.

---

## Horizon-Bounded Abstractions

Every abstraction implicitly assumes:

- a time horizon,
- a regime of operation,
- and tolerated drift.

These assumptions are usually:
- implicit,
- unarticulated,
- and socially shared.

This is not an error.
It is a cost-saving compression.

Failure arises when the abstraction:
- omits its own horizon,
- and cannot represent conditions under which it expires.

---

## Example: Location Without Time

Statements like:
> “This is the same place.”

are never interpreted literally.

They implicitly include:
- a time index,
- acceptable transformation,
- bounded drift.

The time component is rarely stated because:
- it is almost always present implicitly,
- and usually does not bind execution.

When drift accumulates, the omission becomes operationally relevant.

This pattern generalizes across domains.

---

## Expired Abstractions

An abstraction is **expired** when:

1. It was once valid under execution,
2. Environmental or systemic drift has altered causal structure,
3. The abstraction cannot represent or signal that change,
4. Execution continues as if the abstraction were invariant.

Expiration is a **structural condition**, not a mistake or deception.

---

## Redesign-Safe Invariants (Minimal Set)

For redesign to remain possible, abstractions must preserve
(or allow recovery of) the following invariants.

These do **not** need to be foregrounded in routine operation.

They must only not be erased.

### 1. Time / Horizon

- Every claim is relative to a horizon.
- Horizon may be implicit, but must be recoverable.
- Claims without horizon are under-specified for execution.

---

### 2. Execution vs Interpretation

- Distinguish what executes from what explains.
- Interpretation must not masquerade as execution.
- Execution failures must be representable as such.

---

### 3. Irreversibility

- Actions eliminate options.
- Reversal is itself costly execution.
- Models must not assume lossless rollback by default.

---

### 4. Consequence Topology

- Effects propagate through structure, not intent.
- Latency, buffering, fan-out, and observability matter.
- Failure location must not be systematically obscured.

---

### 5. Bounded Resources

- Time, attention, coordination, and energy are finite.
- Infinite negotiation or inspection is not executable.
- Compression is mandatory, not optional.

---

### 6. Refusal or Interruption Possibility

- There must exist a representable point where execution could have stopped.
- If refusal is only narrative, agency claims are ill-typed.
- Redesign requires interruptibility somewhere.

---

### 7. Load Location

- Disturbance must land somewhere.
- If load location is invisible, it will default to implicit sinks.
- Responsibility claims without load tracing are unstable.

---

## Underspecification vs Error

Most failures arise not from incorrect models,
but from **underspecified ones** that silently rely on shared assumptions.

These assumptions remain invisible until:
- drift accumulates,
- horizons extend,
- or load increases.

Explicit articulation is usually triggered by failure, not foresight.

---

## Design Implication

The goal is not to keep all invariants explicit at all times.

The goal is to **never collapse them so completely**
that redesign requires crisis, heroics, or blame.

Redesign capability is a **coordination overhead** that cannot be eliminated,
only deferred or displaced.

---

## Closing

Abstractions do not fail because they are simplified.

They fail because simplification becomes **unrevisable**.

Validity under execution and time
requires only that a system can still ask:

> “Under what conditions would this stop working?”

If that question cannot be represented,
the abstraction has already expired —
whether anyone notices or not.
