# Executional Literacies — Code Domain Instantiation

## Scope and Jurisdiction

This document is a **domain instantiation** of *Executional Literacies* for the **software/code execution domain**.

It does **not** redefine the literacies.
It maps them explicitly onto:

* what **executes**,
* what **flows into execution**, and
* what is **structurally inert** at runtime.

The governing distinction throughout is:

> **Executable vs Non‑Executable Artifacts**

This is not about usefulness in general. It is about **load‑bearing participation in execution**.

---

## Core Executional Regime (Code)

A code execution environment satisfies the executional regime if:

* Code executes deterministically or probabilistically regardless of author intent
* State mutates irreversibly (memory, disk, network, external systems)
* Resources are finite (time, memory, IO, bandwidth)
* Failures may be partial, delayed, or silent
* Rollback is bounded, costly, or unavailable
* Execution halts before global optimality can be proven

Any reasoning that ignores these facts may be coherent but is **non‑isomorphic to runtime behavior**.

---

## Load‑Bearing Execution Loop (Code)

```
input → computation → side effects
```

* **Input**: data, signals, user actions, network messages
* **Computation**: executable instructions, control flow, algorithms
* **Side effects**: memory mutation, IO, persistence, external calls

Only artifacts that **participate in this loop** are execution‑relevant.

---

## Foundational Executional Literacy (Code)

### Definition

The ability to reason about software **as if runtime is real**, even when this invalidates:

* elegant abstractions
* explanatory narratives
* authorial intent
* design purity

### Preserved Distinctions

* compiles vs does not compile
* executes vs annotates
* state mutation vs description
* rollback illusion vs commit reality
* simulation vs production runtime

### Non‑Executable (Out of Scope)

* comments asserting importance
* comments asserting authority
* comments asserting intent
* README claims unreflected in code

These may influence humans, but **they do not run**.

---

## Constraint Literacy (Code)

### Executable Constraints

* time complexity (e.g. **O(n)** vs **O(n²)**)
* space complexity
* stack depth limits
* memory ceilings
* rate limits
* API contracts enforced at runtime

### Non‑Executable Substitutes

* "should be fast"
* "don’t use this in production"
* "this won’t be called often"

Runtime enforces constraints. Comments do not.

---

## Horizon Literacy (Code)

### Executable Horizons

* algorithmic scaling behavior
* memory growth over time
* log accumulation
* data drift
* dependency version decay

### Non‑Executable Horizons

* "future refactor"
* "temporary workaround" (without enforcement)
* "will fix later"

A claim without a time horizon is incomplete.

---

## Frame Literacy (Code)

### Execution‑Capable Frames

* performance analysis
* safety analysis
* correctness under input variance
* failure‑mode analysis

### Non‑Executing Frames

* stylistic purity
* moral ownership ("don’t touch my code")
* narrative justification

A correct argument in a non‑executing frame still fails at runtime.

---

## Meaning Literacy (Code)

### Shared Meaning (Executable)

* function signatures
* type systems
* interfaces
* schemas
* protocols
* tests that fail

### Internal Meaning (Non‑Executable)

* informal intent descriptions
* implicit conventions
* tribal knowledge

Meaning that cannot fail cannot coordinate.

---

## Coordination Literacy (Code)

### Executable Coordination Mechanisms

* version control rules
* CI/CD pipelines
* automated tests
* access permissions
* deployment gates

### Non‑Executable Coordination Claims

* "everyone knows"
* "please be careful"
* "this is obvious"

Coordination is imposed by shared state, not goodwill.

---

## Metrics Literacy (Code)

### Runtime‑Real Metrics

* latency
* throughput
* memory usage
* error rates
* saturation

### Non‑Executing Metrics

* aesthetic cleanliness
* perceived elegance
* author confidence

Metrics that collapse distinctions externalize cost.

---

## Risk and Uncertainty Literacy (Code)

### Execution‑Relevant Risk

* crashes
* data corruption
* security vulnerabilities
* cascading failures

### Non‑Executing Risk Talk

* "unlikely"
* "hasn’t happened yet"
* "probably safe"

Some failures invalidate the system, not just the result.

---

## Authority Literacy (Code)

### Executable Authority

* merge permissions
* deployment rights
* runtime credentials
* production access

### Non‑Executable Authority

* seniority claims
* authorship pride
* social intimidation

Authority that does not gate execution is commentary.

---

## Model Literacy (Code)

### Executable Models

* complexity models
* memory models
* concurrency models
* failure models

### Model Failure

All models compress.
All compression fails under drift.

Defending a model past its execution horizon causes latent failure.

---

## Summary Invariant (Code Domain)

> **Only what executes—or constrains execution—can govern system behavior.**

Everything else is annotation.

Annotations may be useful.
They are not load‑bearing.

Execution ignores commentary.
