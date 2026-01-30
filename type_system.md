# Load-Bearing Stack as a Type System
## A Structural Typing Discipline for Bounded Execution Under Drift

> **Purpose:** provide a *type system* that makes claims about action, evaluation, agency, responsibility, optimization, and governance **well-formed (or ill-formed)** for **bounded executors** in **irreversible, drifting** environments.  
> This is a **static checker** for discourse about execution.

This document is **not** a theory of:
- human cognition, consciousness, intent, or preference formation
- morality, legitimacy, justice, fairness
- what goals *should* be
- any specific optimization method

It is a typing discipline that:
- **rejects ill-typed claims** (category errors)
- **forces explicit horizons, resources, and causal assumptions**
- **marks “under-typed” claims** when current observations are insufficient

---

## 0. Core stance: all claims are conditional on an epistemic context

Every judgment is relative to an **epistemic context** and a **provisional causal model**.

- **Epistemic context** `E` = what is currently observed/known, measurement quality, and what is *not* observed.
- **Topology model** `T̂` = the *current best* model of consequence propagation (latency, fan-out, buffers, observability, irreversibility gradients, dissipation/recovery).
- **Horizon set** `H` = one or more time horizons under which viability is assessed.
- **Resource budget** `R` = bounded time/energy/attention/bandwidth/material capacity.

**Key rule:** if a claim does not specify (or imply) `(E, T̂, H, R)`, it is usually **under-typed** (not rejectable as false, but not executable as a statement about bounded execution).

---

## 1. Objects (terms) and types

### 1.1 Terms (what we talk about)

- `x ∈ State` : world/system state
- `a ∈ Act` : an action (state-changing)
- `π ∈ Policy` : action selection rule
- `C ∈ Closure` : a compression/termination of interpretation (discarded distinctions)
- `M ∈ Metric` : executable evaluation interface inside a closure
- `b ∈ Boundary` : a pre-execution decision boundary
- `refuse(b)` / `accept(b)` : boundary options
- `F ∈ FailureMode` : failure semantics (how it fails, where load lands)

### 1.2 Primitive types (structural, not moral)

- `Exec` : an execution event (irreversible state change)
- `Interp` : interpretation / narrative / justification (does not execute by itself)
- `Topo` : consequence topology (propagation structure)
- `Horiz` : horizon specification
- `Res` : bounded resources (time/energy/attention/etc.)
- `Viable` : continued execution remains possible over specified horizons
- `ClosureOK` : closure is currently sufficient (relative to E, T̂, H, R)
- `MetricOK` : metric is valid within its envelope and fails explicitly when violated
- `Decidable` : boundary where acceptance and refusal are executable paths
- `AgencyOK` : agency attribution is coherent (at a specific boundary)
- `RespOK` : responsibility/load attribution is coherent (within a closure + metrics + decidability)

### 1.3 Claim types (what sort of statement is this?)

We type *claims* as one of:

- `⟦…⟧ : ExecClaim`  
  “X executes / caused Y” (about state changes)
- `⟦…⟧ : InterpClaim`  
  “X intended / meant / justified …” (about interpretation)
- `⟦…⟧ : EvalClaim`  
  “X is good/bad by criterion …” (judgment signal)
- `⟦…⟧ : OptClaim`  
  “Optimizing objective O improves …” (requires viability + metric validity)
- `⟦…⟧ : AgencyClaim`  
  “Actor A chose freely at boundary b …” (requires decidability + refusal symmetry)
- `⟦…⟧ : RespClaim`  
  “Actor A is responsible for outcome Y …” (requires settled closure + bounded metrics + decidable entry + controllables)

### 1.4 Judgment outcomes (three-valued)

For bounded execution we need a third category besides true/false:

- `Well-Typed` : claim is structurally coherent under current `(E, T̂, H, R)`
- `Ill-Typed` : claim violates structural constraints (category error)
- `Under-Typed` : not enough information in `E` / `T̂` / `H` to type-check (epistemic insufficiency)

---

## 2. Contexts (what the type checker requires)

A typing context bundles what must be explicit:

`Γ = (E, T̂, H, R, C?, M?, B?, K)`

Where:
- `E` current observations and measurement quality
- `T̂` current causal/topology hypothesis (explicitly provisional)
- `H` horizons in scope (often multiple)
- `R` resource bounds and margin estimate
- `C?` optional: the closure currently governing execution
- `M?` optional: metric(s) currently used for coordination
- `B?` optional: boundary definition(s)
- `K` known failure semantics (what happens on refusal, overload, saturation, drift)

---

## 3. Structural axioms (invariants)

These are not optional assumptions; they are constraints for bounded executors.

**A1 Irreversibility:** `Exec` destroys information and eliminates alternatives.  
**A2 Boundedness:** `Res` is finite; full sensing/modeling is impossible.  
**A3 Drift:** `T̂` is regime-dependent and can break; invariants are horizon-bound.  
**A4 Unavoidable compression:** any executable representation is lossy.  
**A5 Viability precedes optimization:** “improvement” is undefined if continued execution is not secured.

**Ill-typed trigger:** any framework that presumes reversibility, infinite resources, stationary environments, or lossless abstraction.

---

## 4. Typing rules (the checker)

Below, “`Γ ⊢ claim : Type`” reads: “under context `Γ`, this claim type-checks as `Type`”.

### 4.1 Execution vs interpretation (non-collapse rule)

**Rule EX/IN:**  
If a statement does not refer to state change in `T̂`, it cannot be typed as execution.

- If `claim` references *only* intent/meaning/justification without binding to state transitions:  
  `Γ ⊬ claim : ExecClaim` (Ill-Typed as execution)  
  `Γ ⊢ claim : InterpClaim` (at best)

**Consequence:** “We decided / we value / we intend” is execution-inert unless it binds closures/metrics/boundaries.

---

### 4.2 Viability gate (optimization is not typeable without it)

**Rule V-GATE:**  
`Γ ⊢ OptClaim` only if `Γ ⊢ Viable` over the declared horizons.

Formally (schematic):

- If `Γ ⊢ Viable(H)` and `Γ ⊢ MetricOK(M, C, H)` then `Γ ⊢ OptClaim`
- Else:
  - If viability is violated: `Ill-Typed` (optimization talk is undefined)
  - If viability unknown: `Under-Typed`

---

### 4.3 Closure typing (compression for repetition)

Closure is a mapping that discards degrees of freedom:

`C : State → State_C` (lossy)

**Rule C-OK:**  
`Γ ⊢ ClosureOK(C)` only if:
1) closure extent is bounded by `R` (executable representation)  
2) closure is sufficient for viability across declared `H` *under current `T̂`*  
3) there exists a redesign/exception path with bounded failure semantics (some interruptible region)

If (2) fails due to drift evidence, closure becomes **type-unstable**: it may have been well-typed historically, but is now `Ill-Typed` for the updated `E`.

---

### 4.4 Settlement typing (closure hardening)

Settlement is closure that persists through repetition and depletion.

**Rule SETTLE:**  
`Γ ⊢ Settled(C)` only if:
- closure survives repeated execution under depletion,
- alternatives are eliminated by failure not preference,
- viability holds locally without hidden subsidy **or** the subsidy is explicit in `E` and included in `R`.

If subsidy/buffering exists but is unmodeled: claims of stability are `Under-Typed` (epistemically incomplete).

---

### 4.5 Metric typing (executable interface with explicit failure)

A metric is a finite interface inside a closure:

`M : State_C → ℝ^k` (or comparable finite outputs)

**Rule M-OK:**  
`Γ ⊢ MetricOK(M, C, H)` only if:
1) **Envelope:** validity conditions `Env(M)` are specified (what must be true for substitutability)  
2) **Sufficiency:** metric encodes the minimal DOFs needed for viability in `C` over `H`  
3) **Boundedness:** metric is computable within `R`  
4) **Determinacy:** metric yields determinate outcomes under the closure  
5) **Explicit failure:** outside `Env(M)`, metric *fails loudly* (alarms, saturation, refusal, handoff to redesign)

**If (5) fails**: you get silent saturation → proxy capture.  
In this type system, silent metrics are **ill-typed** as coordination interfaces for optimization.

---

### 4.6 Decidability typing (where choice is coherent)

A boundary is decidable only if refusal is executable.

**Rule D-OK:**  
`Γ ⊢ Decidable(b)` only if:
1) `accept(b)` and `refuse(b)` are both real execution paths in `T̂`  
2) consequences are bounded relative to `H` (containment exists)  
3) failure semantics are characterized in `K` (not omniscient—just actionable)  
4) interruptibility exists with sufficient margin in `R`

If refusal exists “on paper” but triggers catastrophic non-viability under `T̂`, then:
- `Γ ⊬ Decidable(b)` (Ill-Typed)

---

### 4.7 Agency typing (agency exists only at decidable boundaries)

Agency attribution requires a boundary witness.

**Rule AGENCY:**  
`Γ ⊢ AgencyOK(actor, b)` only if:
- `Γ ⊢ Decidable(b)` and
- **refusal symmetry** holds *at that boundary*, under the declared horizon(s)

**Refusal symmetry (structural):**  
If actor X can refuse without catastrophic loss but actor Y cannot (under `T̂`, `H`), then attributing agency to Y for accepting is **ill-typed** *for that boundary*.

Inside execution (post-boundary), only `Discretion` is typeable, not `Agency`.

---

### 4.8 Responsibility typing (load attribution, not moral blame)

Responsibility is typeable only after closure + metric binding + decidable entry.

**Rule RESP:**  
`Γ ⊢ RespOK(actor, outcome)` only if:
1) `Γ ⊢ Settled(C)` (or at least `ClosureOK(C)` with explicit coupling)  
2) `Γ ⊢ MetricOK(M, C, H)` (bounded, valid, explicit failure)  
3) entry into the relevant execution path was decidable: `Γ ⊢ Decidable(b_entry)`  
4) the outcome depends on variables controllable by actor within the closure (not merely affected by them)  
5) load routing is characterized in `T̂` (where cost lands: latency/fan-out/buffers/observability)

If (3) fails, “they are responsible” is generally **ill-typed** as structural responsibility for that boundary (though you can still talk about load location).

---

## 5. The “type checker” workflow (how to use this)

Given a claim `q`, do:

### Step 1 — Classify the claim (what type is it trying to be?)
- Exec / Interp / Eval / Opt / Agency / Responsibility

### Step 2 — Require witnesses (attach the missing structure)
Ask (or specify yourself):
- What horizons `H`?
- What resource bounds `R` and margin estimate?
- What topology model `T̂` (even if provisional)?
- What closure `C` is assumed?
- What metric `M` is binding execution?
- What boundary `b` is the decision point?

If you can’t supply these from current `E`, the claim is usually **Under-Typed**.

### Step 3 — Run the relevant rules
- Opt → V-GATE + M-OK
- Agency → D-OK + refusal symmetry
- Responsibility → settlement + metric validity + decidable entry + controllables

### Step 4 — Output one of:
- **Well-Typed** (coherent under current context)
- **Ill-Typed** (structural violation)
- **Under-Typed** (insufficient observation/model to type-check)

---

## 6. Runtime semantics (what happens when the world changes)

Because drift exists, types are not permanent.

### 6.1 Type instability under drift
When `E` updates or `T̂` changes, previously well-typed claims can become ill-typed.

- Example: metric `M` remains determinate but drift introduces a previously discarded variable `z` that now drives outcomes.
  - `MetricOK(M, C, H)` may fail its envelope or sufficiency checks.
  - If `M` doesn’t fail explicitly → proxy capture (a runtime type error that doesn’t throw).

### 6.2 Redesign as retyping
Redesign is “reopening distinctions”:
- expand or alter closure `C`
- adjust horizons `H`
- replace metrics `M`
- move boundaries `b` to restore decidability
- change topology (buffers, observability, interruptibility)

Redesign authority cannot be fully expressed through the settled metrics that encode the closure being revised. In type terms: **you cannot use a type to fully specify its own retyping rules** without an outer meta-context.

---

## 7. Common ill-typed patterns (diagnostics)

### 7.1 Agency laundering
Claim: “They chose it”  
But refusal was non-executable under `T̂` and `H`.  
→ `Ill-Typed AgencyClaim` (boundary witness fails)

### 7.2 Optimization without viability
Claim: “We should optimize metric M to improve system”  
But viability is failing or undefined on the relevant horizon.  
→ `Ill-Typed OptClaim` (fails V-GATE)

### 7.3 Silent metric saturation
Metric never fails explicitly; drift manifests as gaming.  
→ `Ill-Typed Metric` for coordination under bounded execution

### 7.4 Horizon mismatch
Short-horizon metric binds execution while long-horizon viability fails.  
→ `Under-Typed` until horizons are declared; often becomes `Ill-Typed` once declared

### 7.5 Stability by hidden subsidy
Settlement claimed but buffering/subsidy is unmodeled in `E`/`R`.  
→ `Under-Typed` (epistemic incompleteness); may become `Ill-Typed` if subsidy removal breaks viability

---

## 8. Minimal worked typings (schematic)

### Vignette A — “We can keep adapting freely”
- Requires margin `R` and containment topology `T̂` that keeps failures local.
- If margin is not specified or is near zero, the claim is **Under-Typed**.
- If failures are non-local and costly (fan-out, high irreversibility), then “free adaptation” is **Ill-Typed** unless closure/coordination artifacts are introduced.

### Vignette B — Metric as interface under drift
- Closure tracks `{x,y}`, discards `z`.
- Drift makes `z` causal for outcomes.
- If `M(x,y)` does not have an explicit envelope/alarm for this regime change → `Ill-Typed Metric` (silent saturation).
- The well-typed move is retyping: reopen closure to include `z` or change horizon/topology.

### Vignette C — Agency claim with refusal asymmetry
- Boundary offers “accept P or refuse.”
- Refusal triggers catastrophic loss for B but not for A.
- `Decidable(b)` fails for B.  
→ “B chose P” is **Ill-Typed** as `AgencyClaim` at that boundary.

---

## 9. Where “values” live (descriptive, not normative)

In this type system, “values” become execution-relevant only when they:
- constrain closure selection (`C`)
- constrain metric envelopes (`Env(M)`)
- allocate redesign authority (who can retype the system)
- preserve refusal executability (decidability)

Otherwise values remain `InterpClaim`—not false, but execution-inert.

---

## 10. Compressed summary (type-level)

- Execution is irreversible; resources are bounded; drift breaks invariants.
- Compression is mandatory; closure enables repetition; settlement hardens closure.
- Metrics coordinate inside closures but must have explicit envelopes and failure.
- Optimization is only typeable after viability and metric validity are established.
- Agency is only typeable at decidable boundaries with executable refusal.
- Responsibility is only typeable after closure + metrics + decidable entry + controllables.
- Every claim is conditional on current observations `E` and a provisional topology model `T̂`.

Only what **executes**—and survives depletion—persists.
