# Executional Literacies
## An abstract spec for distinction-preservation under irreversible constraint

> **Purpose**  
> Define the minimal **distinctions** a reasoner must preserve for reasoning to remain **runtime-load-bearing** under bounded execution, drift, and irreversibility.

These literacies are not virtues, traits, or morality.
They are **structural competencies**: if the distinctions collapse, reasoning becomes non-executable (or produces systematically wrong commitments).

This document is the **abstract spec**.  
Concrete instantiations (e.g., code, security, orgs) specialize these literacies into domain gates and artifacts.

---

## Jurisdiction and scope

This framework applies when claims are intended to:

- guide action that commits resources,
- coordinate across agents and time,
- persist under disturbance,
- survive depletion across a horizon.

It does **not** claim that non-executable discourse is illegitimate.
It claims only:

> non-executable discourse is not **load-bearing** until it binds to execution surfaces.

---

## Core concept: runtime-load-bearing reasoning

A piece of reasoning is **runtime-load-bearing** iff, when executed through a constrained system over a binding horizon, it:

- preserves relevant invariants (or correctly predicts their violation),
- correctly accounts for irreversibility and recovery channels,
- does not rely on hidden buffers, hidden permissions, or interpretive substitution,
- remains stable across the system’s consequence topology.

---

## Two-layer model (anchor)

Most confusion comes from collapsing these layers:

### Cognitive layer (reasoner discipline)
The reasoner preserves distinctions so they do not hallucinate:
- rollback where none exists,
- permission where none is enforced,
- harmlessness where buffers are masking cost,
- local success where topology exports failure.

### Control layer (system enforcement)
The system must encode those distinctions into:
- gates and invariants,
- defaults and omission semantics,
- refusal paths,
- audit surfaces,
- bounded failure semantics.

This document specifies the **cognitive layer**.
It assumes the control layer exists only where explicitly named.

---

## Executional validity (minimal operationalization)

“Executional validity” is not a metric.
It is a minimal set of checks that make a claim *eligible* to guide execution.

A claim is executionally valid (for system S, horizon H) only if it can answer:

1) **Commit inventory**  
   What irreversible commits does this claim imply?

2) **Recovery channels**  
   What bounded recovery exists for each commit (and who owns it)?

3) **Probe vs commit**  
   What can be staged/canary’d, and what abort condition halts rollout?

4) **Surface audit**  
   On which execution surfaces must this claim remain true?

5) **Horizon binding**  
   Over what horizon does “works” mean “does not violate invariants”?

Failure to answer does not make the claim false.
It makes the claim **non-load-bearing**.

---

# The literacies (abstract spec)

Each literacy is defined by:
- **Distinction preserved**
- **Failure mode when collapsed**
- **Diagnostic question**
- **Minimal evidence**

---

## 0) Foundational Literacy
### Distinction preserved
**Execution is irreversible** and consumes bounded resources.

### Failure mode
Rollback hallucination:
- treating commitments as reversible by reinterpretation,
- treating cost as optional,
- ignoring debt accumulation.

### Diagnostic question
“What, exactly, becomes harder or impossible after we do this?”

### Minimal evidence
A named irreversible commit + a bounded recovery channel (or an admission that none exists).

---

## 1) Constraint Literacy
### Distinction preserved
Invariants are **enforced** by the system, not negotiated by intent.

### Failure mode
Constraint denial:
- reasoning as if invariants are preferences,
- hoping the system will “understand,”
- betting on exception without owning its buffer.

### Diagnostic question
“What invariant will stop this, and where does it enforce?”

### Minimal evidence
A concrete enforcement surface (gate, default, capacity limit) and what it does on violation.

---

## 2) Horizon Literacy
### Distinction preserved
“Works” is horizon-bound; short-run stability is not long-run viability.

### Failure mode
Temporal overgeneralization:
- proving liveness over a short slice and claiming persistence,
- ignoring accumulation, saturation, and drift.

### Diagnostic question
“For how long must this remain true, and what dominates at that horizon?”

### Minimal evidence
A declared horizon + at least one long-horizon dominant effect (drift, saturation, irreversibility gradient).

---

## 3) Topology Literacy
### Distinction preserved
Consequences propagate through topology; “where it lands” is not where it started.

### Failure mode
Locality illusion:
- assuming local fixes remain local,
- ignoring fan-out, coupling, and displaced load.

### Diagnostic question
“Where does the disturbance go, and who absorbs it?”

### Minimal evidence
A path sketch: interfaces touched, buffers crossed, and the first downstream owner.

---

## 4) Surface Literacy
### Distinction preserved
A claim must remain true on the **execution surfaces** where it runs.

### Failure mode
Abstract correctness with runtime failure:
- reasoning valid “in principle,”
- failing at the boundary (defaults, omitted parameters, environment mismatch).

### Diagnostic question
“Where does this actually execute, and what does ‘true’ mean there?”

### Minimal evidence
Enumerated surfaces (even coarse) + at least one default/omission semantic.

---

## 5) Default Literacy (Omission Semantics)
### Distinction preserved
Non-action executes system defaults; silence is an action where defaults exist.

### Failure mode
Responsibility laundering via omission:
- “we didn’t do anything,”
- “it just happened,”
- letting the default execute while claiming neutrality.

### Diagnostic question
“What happens if we do nothing?”

### Minimal evidence
A named default transition and its downstream commit.

---

## 6) Buffer Literacy
### Distinction preserved
Buffers defer legibility; they do not remove cost.

### Failure mode
Buffer-as-safety illusion:
- interpreting absence of failure as sufficiency,
- ignoring saturation and unowned buffers.

### Diagnostic question
“What buffer is currently absorbing this, and what consumes it?”

### Minimal evidence
Buffer inventory: capacity, owner, depletion signal.

---

## 7) Forbearance Literacy
### Distinction preserved
Forbearance is **buffered violation** (discretionary non-enforcement), not safety.

### Failure mode
Tolerance misread as permission:
- assuming “allowed” implies “safe,”
- scaling on borrowed slack.

### Diagnostic question
“What is being violated that is merely not enforced yet?”

### Minimal evidence
A named violated constraint + the buffer that is masking it + the depletion trigger.

#### Canonical buffer-depletion model (tiny formalism)
Forbearance = violation × buffer

Buffers can be:
- attention,
- detection latency,
- surplus capacity,
- goodwill,
- audit gaps,
- low load,
- asymmetry.

Checklist:
- What buffer masks the violation?
- What consumes it?
- What replenishes it?
- Earliest depletion signal?

---

## 8) Access Control Literacy
### Distinction preserved
Runtime gating beats social story.

### Failure mode
Permission confusion:
- legitimacy treated as permission,
- credentials treated as entitlement,
- approval treated as enforcement.

### Diagnostic question
“What gate stops this if we’re wrong?”

### Minimal evidence
A concrete enforced gate or refusal path.

#### Triad (disambiguation)
- **Permission** = enforced gate (credentials, policy, control)
- **Legitimacy** = cheap cooperation (social acceptance)
- **Coordination discount** = friction function (trust/latency tax)

These often correlate. They are not equivalent.

---

## 9) Meaning Literacy (Coordination Meaning)
### Distinction preserved
Meaning that coordinates must be able to **fail**.

### Failure mode
Unfalsifiable coordination:
- slogans that cannot be violated,
- “values” with no executable commitments,
- ambiguity used to avoid accountability.

### Diagnostic question
“How can this meaning fail, and who pays when it does?”

### Minimal evidence (the triad)
- **Commitment:** what is bound?
- **Detection:** what counts as failure and how is it observed?
- **Attribution:** who is structurally attributable / bears cost?

> Meaning that cannot fail cannot coordinate.

---

## 10) Metric Literacy
### Distinction preserved
Metrics encode compressed degrees of freedom; they saturate and misalign.

### Failure mode
Proxy collapse:
- optimizing the map,
- exporting cost to uncaptured surfaces,
- mistaking metric movement for viability.

### Diagnostic question
“What does this metric erase, and who absorbs the erased load?”

### Minimal evidence
A saturation condition + a known externality surface.

---

## 11) Attribution Literacy (Agency vs Discretion)
### Distinction preserved
Agency exists at decidable boundaries; discretion is in-execution adjustment.

### Failure mode
Moralization of structure:
- blaming constrained actors for non-decidable outcomes,
- treating downstream coping as upstream choice.

### Diagnostic question
“Where was refusal executable?”

### Minimal evidence
A boundary where accept/refuse were both executable and bounded over the horizon.

---

## 12) Closure Literacy
### Distinction preserved
Closure discards distinctions to remain executable; redesign reopens them.

### Failure mode
Closure denial or closure absolutism:
- refusing to close → coordination collapse,
- refusing to reopen → brittleness under drift.

### Diagnostic question
“What distinctions are we discarding to run, and who can reopen them?”

### Minimal evidence
Named discarded distinctions + a redesign interface (who/where/when reopening is allowed).

---

## 13) Regime Literacy
### Distinction preserved
Different regimes admit different reasoning.

### Failure mode
Wrong-regime reasoning:
- importing optimization talk into existence crises,
- importing legitimacy talk into enforcement surfaces,
- importing scale assumptions into fragile interiors.

### Diagnostic question
“What regime are we in (exist/persist/scale), and what literacies are mandatory here?”

### Minimal evidence
A regime classification + one binding indicator (buffer burn, coupling pressure, coordination overhead, adversarial pressure).

---

## 14) Redesign Literacy
### Distinction preserved
When invariants break under drift, redesign is mandatory—not negotiable.

### Failure mode
Stuck-in-optimization:
- treating structural mismatch as execution error,
- adding correction overhead instead of reopening the closure.

### Diagnostic question
“What would have to be true for this to work without heroics?”

### Minimal evidence
A redesign admission: “the current closure is insufficient,” plus an executable path to reopen it.

---

# Common collapse pathways (not universal)

The literacies often collapse in recognizable patterns, especially in high-coupling environments.

### A) Buffer-first collapse
Buffers mask violations → forbearance scaling → sudden saturation → moralization of the crash.

### B) Metric-first collapse
Proxy becomes target → externalities accumulate off-ledger → correction overhead rises → viability breaks.

### C) Access-control collapse (security / governance)
Legitimacy substituted for gates → adversarial contact → enforcement asserts → “surprise” failure.

These are common pathways, not laws. Order varies by domain and topology.

---

# Minimal kernel (for adoption)

If someone will only learn a small set, the kernel is:

1) Foundational (irreversibility)  
2) Constraint (enforcement)  
3) Horizon (dominant effects)  
4) Topology (where load lands)  
5) Forbearance (buffered violation)

Everything else specializes or composes these.

---

# Closing

Executional literacies are not about being “right.”
They are about remaining **coherent under constraint**.

A reasoner who preserves these distinctions:
- avoids rollback hallucination,
- stops mistaking permission for gating,
- detects buffer masking,
- binds claims to horizons,
- and can tell when redesign is mandatory.

Without them, reasoning becomes narratively persuasive but executionally inert.

Only what survives execution remains load-bearing.
