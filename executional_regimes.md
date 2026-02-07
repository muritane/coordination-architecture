# Executional Regimes
## Exist · Persist · Scale
## Runtime Modes for Systems Under Bounded, Irreversible Execution

---

## Purpose

This document specifies **executional regimes**: discrete **runtime modes** that determine what kinds of reasoning are *admissible*, *dangerous*, or *inert* for a system operating under bounded, irreversible execution.

Executional regimes are not goals, aspirations, or maturity levels.  
They are **environmentally enforced states** that constrain what actions can safely govern execution.

This document complements *Executional Literacies* by defining the **outer control loop** that selects *which literacies are mandatory* at a given time.

---

## Core Claim

> **Reasoning is only execution-valid relative to the regime the system is actually in.**

Most catastrophic failures are not caused by bad designs, bad actors, or bad intentions, but by **regime mismatch**:
- scale reasoning applied in survival,
- optimization applied before stability,
- narrative coherence substituted for executional viability.

Execution does not negotiate regime.

---

## Definition: Executional Regime

An **executional regime** is a stable configuration of constraints, buffers, risks, and coupling that determines:

- what failure modes are terminal vs survivable,
- whether optionality is shrinking or growing,
- which forms of reasoning may safely guide action,
- which improvements are meaningful vs illusory.

Executional regimes are **state descriptions**, not value judgments.

---

## The Three Canonical Regimes

This framework defines three primary executional regimes:

1. **Exist** — survival under existential risk  
2. **Persist** — stability with buffer regeneration  
3. **Scale** — expansion under increasing coupling  

These are not linear “phases” by default.  
Systems can regress, oscillate, or die in any regime.

---

## Regime 1: Exist
### Survival Under Existential Risk

### Definition

A system is in **Exist** when:

- loss of a small number of invariants causes terminal failure,
- buffers are finite and actively depleting,
- rollback is partial, delayed, or unavailable,
- tail risks dominate expected value,
- humans or critical nodes are near exhaustion,
- the system may not survive another major error.

The objective in Exist is **continued existence**, not improvement.

---

### Structural Characteristics

- Optionality is **shrinking**
- Slack is **borrowed**, not earned
- Failure modes are **discontinuous**
- Optimization increases risk
- Design purity is irrelevant
- Speed of insight matters more than correctness

---

### What Counts as Success

- The system is still alive
- Some forward progress exists (non-zero liveness)
- Damage remains bounded
- Buffers are not catastrophically consumed
- Redesign remains possible

Nothing else matters yet.

---

### Mandatory Literacies (Non-Negotiable)

These must hold or the system dies before redesign:

- **Foundational Executional Literacy**
- **Forbearance Literacy**
- **Risk & Uncertainty Literacy**
- **Consequence Topology Literacy**
- **Liveness & Orchestration Literacy**

Failure of any one of these collapses Exist into terminal failure.

---

### Explicitly Dangerous Reasoning in Exist

The following are *actively harmful* in this regime:

- optimization-first reasoning,
- scale-readiness arguments,
- elegance or abstraction purity,
- consensus-seeking delays,
- metric maximization,
- long-horizon justification,
- “we can fix it later” narratives.

These consume optionality faster than they create it.

---

### Regime Error Signature

> “We tried to improve things, and then everything collapsed.”

This almost always indicates **scale or persist reasoning applied during Exist**.

---

## Regime 2: Persist
### Stability With Buffer Regeneration

### Definition

A system is in **Persist** when:

- core invariants are stable,
- failures are recoverable,
- buffers regenerate as fast as they are consumed,
- humans recover faster than they degrade,
- tail risks are bounded or contained,
- the system can survive ordinary errors.

Persist is where **maintenance and redesign** are possible.

---

### Structural Characteristics

- Optionality is **stable or slowly increasing**
- Slack can be deliberately created
- Failures are mostly continuous, not terminal
- Local optimization becomes meaningful
- Coordination costs begin to matter
- Drift becomes the primary threat

---

### What Counts as Success

- Buffers stop shrinking
- Incidents reveal more than they cost
- Redesign windows open and remain open
- The system does not require heroics to function
- Enforcement shifts from discretionary to structural

---

### Mandatory Literacies in Persist

Still required:
- Foundational
- Risk
- Consequence Topology
- Liveness

Now additionally load-bearing:
- **Constraint Literacy**
- **Horizon Literacy**
- **Metrics Literacy**
- **Access Control Literacy**

These determine whether stability holds or silently erodes.

---

### Common Failure in Persist

Persist fails when:

- drift is ignored,
- temporary fixes ossify,
- metrics replace system health,
- humans become hidden buffers again,
- forbearance is mistaken for invariance.

This produces **false stability**, followed by regression to Exist or collapse.

---

## Regime 3: Scale
### Expansion Under Increasing Coupling

### Definition

A system is in **Scale** when:

- it seeks increased throughput, scope, or reach,
- coupling and second-order effects dominate,
- adversarial pressure is expected,
- small local changes have global consequences,
- coordination overhead grows superlinearly.

Scale is not “more Persist.”  
It is a **topological phase change**.

---

### Structural Characteristics

- Optionality is abundant but fragile
- Errors propagate rapidly
- Metrics become weapons
- Interfaces become attack surfaces
- Representations fail faster
- Local reasoning is often wrong

---

### What Counts as Success

- Growth without topology collapse
- Externalities are bounded
- Incentives remain aligned with system health
- Failure modes degrade gracefully
- The system can absorb shocks proportional to its size

---

### Mandatory Literacies in Scale

All executional literacies become load-bearing, especially:

- **Coordination Literacy**
- **Meaning Literacy**
- **Representation Literacy**
- **Adversarial Dynamics Literacy**
- **Metrics Literacy** (high risk of proxy collapse)

Scale without these collapses into systemic failure.

---

### The Most Common Scale Error

> Attempting to scale a system that never truly reached Persist.

This produces:
- cascading failures,
- metric gaming,
- human burnout,
- reputational or legal collapse.

---

## Regime Transitions

### Exist → Persist

Occurs when:

- optionality burn ≤ optionality regeneration,
- buffers stop shrinking,
- tail risks are bounded,
- liveness is reliable under stress,
- humans recover faster than they degrade.

This is **not** achieved by desire, vision, or alignment.

---

### Persist → Scale

Occurs when:

- stability holds across drift,
- coordination mechanisms are enforced,
- representations are known to fail safely,
- adversarial pressure is anticipated,
- propagation is modeled and bounded.

Skipping this transition is fatal.

---

### Regression

Systems can regress:

- Persist → Exist (drift, shock, mismanagement)
- Scale → Exist (catastrophic propagation)

Regime regression is common and often denied until late.

---

## Regime Identification Principle

> **Identify the executional regime before admitting reasoning that governs action.**

If reasoning assumes:
- slack that does not exist,
- rollback that is unavailable,
- stability that is not enforced,
- coordination that is informal,

then it is **regime-invalid**, regardless of elegance or intent.

---

## Closing

Executional regimes are enforced by reality, not belief.

No amount of:
- desire,
- alignment,
- persuasion,
- optimism,
- or correctness-in-theory

can move a system out of Exist, stabilize Persist, or survive Scale.

Only reasoning that is **admissible in the current regime** preserves optionality long enough for redesign or growth.

Systems do not fail because they are bad.

They fail because **the wrong kind of reasoning was allowed to govern execution at the wrong time**.
