# Executional Literacies — Code Domain Instantiation
## Structural Alphabets for Reasoning Under Bounded, Irreversible Software Execution

---

## Purpose

This document is a **domain instantiation** of *Executional Literacies* for the **software/code execution domain**.

It does not redefine the literacies.  
It maps them onto software reality by making explicit:

- what **executes**,
- what **constrains execution**,
- what **gates execution** (what reaches runtime),
- and what is **structurally inert at runtime**.

The governing partition throughout is:

> **Runtime-Load-Bearing vs Runtime-Inert**

“Runtime-inert” does not mean “useless.”  
It means **it does not directly participate in, constrain, or gate execution**.

---

## Scope and Jurisdiction

This instantiation applies when software exists in an **executional regime**:

- code runs regardless of author intent,
- state mutates (memory/disk/network/external systems),
- resources are finite (CPU, memory, IO, bandwidth, money),
- failures can be partial, delayed, silent, or cascading,
- rollback is bounded, costly, or unavailable,
- environments drift (dependencies, traffic, data, infra, attacker behavior),
- systems halt before global correctness/optimality is proven.

Reasoning that ignores these invariants may be coherent but is **non-isomorphic** to runtime behavior.

---

## Definitions (Stabilized for Code)

- **Runtime-load-bearing artifact**: participates in, constrains, or gates execution.
  - Examples: executable code, configuration that affects behavior, schemas, ACLs, deploy gates, tests that fail the pipeline.
- **Runtime-inert artifact**: does not directly affect runtime behavior.
  - Examples: comments, most prose documentation, intent statements without enforcement.
- **Executional validity (code)**: whether reasoning remains correct when compiled into:
  - actual runtime constraints,
  - real failure modes,
  - and real deployment/ops coupling.

---

## Quick Map (Code)
### Literacies and Their Software Failure Surfaces

- **Foundational**: guards against reasoning as if rollback/retries are free and production is a simulator.
- **Constraint**: guards against ignoring complexity/resource ceilings and runtime contracts.
- **Horizon**: guards against drift/accumulation (leaks, queues, logs, dependency decay).
- **Frame**: guards against “winning” style/architecture debates that don’t survive runtime.
- **Meaning**: guards against “shared understanding” without interfaces/schemas/tests.
- **Coordination**: guards against multi-author shared state failures (merge/deploy, coupling, externalities).
- **Metrics**: guards against proxy collapse (optimizing dashboards while users suffer).
- **Risk**: guards against tail failures (data corruption, security incidents, cascading outages).
- **Access Control**: guards against confusing status/seniority with actual gating (permissions, credentials, approvals).
- **Representation**: guards against misusing models (complexity, concurrency, capacity) past their regime.

---

## The Execution Loop (Code)

A minimal execution loop in software:

**input → computation → side effects**

- **Input**: requests, events, messages, user actions, files, clocks, network, entropy sources.
- **Computation**: control flow, algorithms, scheduling, concurrency, resource allocation.
- **Side effects**: memory mutation, IO, persistence, external calls, billing, queue publishes, cache invalidation.

Only artifacts that participate in or constrain this loop are runtime-load-bearing.

---

## Execution Surfaces

Software execution couples to multiple surfaces; “it runs” is not one thing.

### 1) Runtime Surface (Production)
- the process, container, VM, serverless runtime
- memory/CPU/IO scheduling
- network behavior, retries, timeouts

### 2) Persistence Surface
- databases, object stores, caches, filesystems
- schema/constraints/indexing
- migration and backfill behavior

### 3) Integration Surface
- upstream/downstream services
- API contracts, rate limits, auth, compatibility

### 4) Deployment Surface (Gating)
- CI/CD pipelines, build steps, tests
- feature flags, canaries, progressive delivery
- approval gates, environment promotion

### 5) Security Surface (Gating + Runtime)
- secrets, credentials, ACLs, IAM roles
- supply chain dependencies
- audit logs and incident response

Executional validity must survive **all** relevant surfaces.

---

## Foundational Executional Literacy (Code)

### Definition

The capacity to reason about software **as if production runtime is real**—even when this invalidates:

- elegant abstractions,
- design purity,
- authorial intent,
- local reasoning divorced from ops reality.

It prevents **non-executable reasoning** from governing changes that will run.

### Core Alphabet (Distinctions Preserved)

- **compiles/builds** vs **does not**
- **executes** vs **annotates**
- **side effects** vs **descriptions**
- **bounded rollback** vs **rollback illusion**
- **staging/simulation** vs **production**
- **local correctness** vs **system correctness under coupling**

### Failure Signature

Reasoning that assumes invisible rollback or free retries, such as:

- “We can revert if it breaks” (while data/schema side effects persist)
- “We’ll just retry” (while retries amplify load or duplicate effects)
- “It’s fine; tests passed” (while production differs in scale, latency, data shape)
- “It worked on my machine” (environment non-isomorphism)

### Diagnostic Question

> *Am I reasoning as if production is a simulator with infinite retries, perfect observability, and cheap rollback?*

---

## 1) Constraint Literacy (Code)

### Definition

The ability to distinguish **runtime constraints** (enforced) from preferences and intentions.

Constraints are invariants: runtime enforces them without negotiation.

### Runtime-Load-Bearing Constraints

- time/space complexity and scaling regimes
- memory ceilings, GC pressure, allocator behavior
- CPU saturation, IO wait, bandwidth ceilings
- concurrency limits, queue depth, thread pools
- rate limits and quota enforcement
- API contracts enforced at runtime (schemas, validation, auth)
- timeout budgets and retry policies

### Runtime-Inert Substitutes

- “should be fast”
- “don’t call this often”
- “won’t happen in production”
- “we’ll optimize later” (without gates/budgets)

### Failure Signature

- Designs that require the system not to reach real scale.
- “Optimization” that never touches the bottleneck.
- Breaking runtime contracts while preserving narrative correctness.

### Diagnostic Question

> *Am I treating an enforced constraint as if it were a negotiable preference?*

---

## 2) Horizon Literacy (Code)

### Definition

The ability to reason about **time-indexed validity** under accumulation and drift.

A claim without a horizon (“safe now” vs “safe at scale over time”) is incomplete.

### Executional Horizons (Load-Bearing)

- algorithmic scaling as input grows
- memory growth over time (leaks, caches, fragmentation)
- log/trace accumulation and storage costs
- queue/backpressure behavior under spikes
- dependency version drift and deprecation
- data shape drift (new fields, nulls, distributions)
- infra drift (autoscaling, instance types, kernel/runtime changes)

### Runtime-Inert Horizons

- “temporary workaround” (without expiry enforcement)
- “future refactor”
- “we’ll fix it next sprint”

### Failure Signature

- “Temporary” code ossifies; the horizon was never enforced.
- Slow leaks and creep failures that appear weeks later.
- A change is correct at t=0 and wrong at t=90 days.

### Diagnostic Question

> *What is the validity horizon of this change, and what will drift or accumulate past it?*

---

## 3) Frame Literacy (Code)

### Definition

A **frame** maps claims to actions.  
Frame literacy is the ability to choose frames that remain **execution-capable** at runtime.

### Execution-Capable Frames

- performance and capacity analysis
- failure-mode and effects analysis (FMEA)
- safety/correctness under input variance
- concurrency and memory-model reasoning
- observability and operability analysis

### Non-Executing Frames (Often Useful, Not Runtime-Decisive)

- style purity and aesthetic cleanliness
- “ownership” narratives (“don’t touch my code”)
- intent justifications disconnected from constraints

### Failure Signature

- Winning architecture debates while shipping regressions.
- Mistaking readability arguments for correctness/operability.
- Treating elegance as a substitute for failure analysis.

### Diagnostic Question

> *If I’m “right” inside this frame, does that still produce code that survives production execution?*

---

## 4) Meaning Literacy (Code)
### Shared Meaning-for-Coordination

### Definition

Meaning in software coordinates only when it is **externally addressable** and **failure-capable**.

In execution-coupled software, shared meaning exists when it is expressed as:

- interfaces and type contracts,
- schemas and protocol definitions,
- invariants enforced by code,
- tests that fail,
- tools that block or gate execution.

### Runtime-Load-Bearing Shared Meaning

- function signatures, types, effect annotations (where enforced)
- schemas (DB, JSON, protobuf), migrations
- API contracts, versioning rules
- tests, linters, static analysis that block merges/releases
- feature flag semantics and rollout rules

### Runtime-Inert Internal Meaning

- informal prose intent
- “tribal knowledge”
- conventions without enforcement
- comments asserting meaning without checks

### Failure Signature

- “Everyone knows how this works” until a new contributor breaks it.
- “It’s obvious” until the interface changes and consumers silently misinterpret.
- Production incidents caused by assumptions not encoded as contracts.

### Diagnostic Question

> *Where does this meaning live in an interface, schema, or test that can fail and stop unsafe execution?*

---

## 5) Coordination Literacy (Code)

### Definition

The ability to reason about **multi-author execution** under shared state and externalities.

Coordination is imposed by shared repositories, shared deploy pipelines, shared production, and shared on-call reality.

### Load-Bearing Coordination Mechanisms

- version control workflows (branch protection, required reviews)
- CI/CD pipelines, quality gates
- automated tests, integration tests, contract tests
- deployment strategies (canary, blue/green, progressive delivery)
- incident protocols, runbooks, SLO/SLA practices

### Runtime-Inert Coordination Claims

- “be careful”
- “don’t break prod”
- “everyone knows the rules”
- “please remember to…”

### Failure Signature

- Coordination relies on memory and good intentions.
- Merge conflicts and deploy collisions become production outages.
- Local wins produce global failures due to coupling.

### Diagnostic Question

> *What mechanism prevents the bad version from shipping when people are tired, rushed, or unaware?*

---

## 6) Metrics Literacy (Code)
### Measurement Under Load and Incentives

### Definition

Metrics literacy is the ability to distinguish:

- metrics as **instruments that allocate attention and incentives**,
- from metrics as **truth**.

Metrics are load-bearing when they are used to gate or steer action. Misalignment externalizes cost.

### Runtime-Real Metrics

- latency, tail latency (p95/p99), jitter
- throughput, saturation, queue depth
- memory usage, GC time, error rates
- availability, success rate, burn rate, SLO error budget
- cost metrics (per request, per tenant), resource efficiency

### Failure Signature

- Dashboard green while users suffer (wrong slices, wrong percentiles).
- Metric improves because behavior changed, not because system improved.
- Cost pushed outside the measured boundary (e.g., downstream pain).

### Diagnostic Question

> *Is this metric collapsing distinctions, incentivizing gaming, or externalizing cost to an unmeasured surface?*

---

## 7) Risk & Uncertainty Literacy (Code)

### Definition

The ability to reason under uncertainty where some failure modes are **ruinous**—they invalidate the evaluation frame rather than merely degrading performance.

### Execution-Relevant Tail Risks

- data corruption and irrecoverable writes
- security vulnerabilities and credential compromise
- cascading failures and retry storms
- partial outages with silent wrongness
- inconsistent states across services (split-brain, idempotency failure)

### Failure Signature

- “Unlikely” is treated as “acceptable” despite catastrophic impact.
- Rare concurrency bugs shipped without containment.
- Safety properties assumed without proving or gating them.

### Diagnostic Question

> *What are the tail failures here, and which ones are terminal (data loss, security breach, systemic outage)?*

---

## 8) Access Control Literacy (Code)
### Gating, Credentials, and Real Authority

### Definition

Access control literacy distinguishes:

- **permission** (what credentials allow),
- **legitimacy** (what process accepts without enforcement),
- **coordination discount** (trust/latency tax imposed on actions).

In software, “authority” is load-bearing only when it **gates** execution or access to shared state.

### Runtime-Load-Bearing Authority

- merge permissions, branch protection
- deploy rights and environment promotion
- runtime credentials (IAM roles, secrets, service accounts)
- database permissions and key management
- feature flag control and kill-switch access

### Runtime-Inert Authority

- seniority claims
- authorship pride
- social intimidation
- “this is my subsystem” without gating power

### Failure Signature

- A high-status person can’t actually stop unsafe deploys (no gate).
- A low-status account can exfiltrate secrets (bad IAM).
- “Approval” exists socially but not technically.

### Diagnostic Question

> *What actually gates the action (merge, deploy, credential use), and who bears consequences when it goes wrong?*

---

## 9) Forbearance Literacy (Code)

### Temporary Non-Enforcement at Runtime and in Process

### Definition

**Forbearance literacy (code)** is the ability to distinguish **runtime or process safety** from **temporary non-enforcement** caused by:

* low load,
* unused code paths,
* partial rollout,
* discretionary human intervention,
* or delayed detection.

Lack of failure is not evidence of correctness.

---

### Runtime Sources of Forbearance

* Code paths not yet exercised in production.
* Feature flags shielding behavior from real traffic.
* Low traffic masking performance or concurrency bugs.
* On-call engineers manually mitigating effects.
* Silent data corruption not yet queried.
* Security exposure not yet exploited.

These are **buffers**, not invariants.

---

### Core Alphabet (Code)

* **correct execution** vs **untriggered failure**
* **safety** vs **lack of observation**
* **invariant enforcement** vs **human patching**
* **tested under load** vs **not yet exercised**
* **rollback available** vs **damage not yet surfaced**

---

### Failure Signature

* “It’s been fine so far” used as correctness evidence.
* Shipping unsafe code because incidents haven’t occurred.
* Treating feature flags as safety mechanisms rather than delay mechanisms.
* Confusing manual intervention with system resilience.
* Catastrophic failure when traffic, scale, or adversarial input arrives.

---

### Diagnostic Question

> *Is this behavior safe, or merely unexercised or temporarily mitigated?*

---

### Interaction With Other Literacies (Code)

* **Foundational**: production is not a simulator; silence is not success.
* **Horizon**: forbearance expires as load, data, or attackers arrive.
* **Risk**: tail failures are masked until they are terminal.
* **Access Control**: human mitigation is not a gate.

---

## 10) Representation Literacy (Code)
### Compression, Scope, and Drift in Technical Models

### Definition

Software engineering relies on representations (models) that compress reality: complexity models, memory models, concurrency models, capacity plans, threat models.

Representation literacy is the ability to use these compressions within their regime—and to detect when drift breaks them.

### Load-Bearing Representations

- big-O and scaling models (with constants and practical ceilings)
- memory and allocation models
- concurrency and happens-before models
- reliability models (timeouts, retries, circuit breakers)
- threat models and trust boundaries
- capacity and queuing models

### Failure Signature

- Defending a model beyond its regime (e.g., big-O ignores IO or constant factors dominate).
- Applying single-node reasoning to distributed systems.
- Treating test environment performance as production truth.

### Diagnostic Question

> *What does this model compress away, and under what conditions will that hidden mass dominate execution?*

---

## Dependency Structure (Code)

These literacies are not independent.  
In high-coupling software environments, a typical cascade (not universal):

1. Foundational collapses (production treated as simulator)
2. Constraint collapses (runtime ceilings ignored)
3. Horizon collapses (drift/accumulation ignored)
4. Frame collapses (style debates replace runtime reasoning)
5. Meaning collapses (assumptions not encoded)
6. Coordination collapses (process relies on goodwill)
7. Metrics collapses (proxy dominates experience)
8. Risk collapses (tail failures dismissed)
9. Access control collapses (status replaces gating)
10. Forbearance collapses (silence mistaken for safety)
11. Representation collapses (models treated as sovereign)

---

## Derived Invariant (Code) — Not a Literacy

> **Only what executes, constrains execution, or gates execution can govern runtime behavior.**

Everything else is annotation.

Annotations can be valuable for humans, but they are not runtime-load-bearing unless they are coupled to enforcement (tests, gates, contracts, tooling).

---

## Assessment Principle (Code)

Executional literacies in software are assessed by:

- avoidance of structural failure modes (not just passing tests),
- stability of distinctions under incident pressure,
- refusal to ship reasoning that depends on rollback illusion,
- deliberate, bounded cost to preserve invariants (gates, idempotency, containment),
- resistance to narrative substitution (“should,” “unlikely,” “everyone knows”).

---

## Closing

Software does not care what the author meant.

Runtime executes:

- the code,
- the constraints,
- the gates,
- the drift,
- and the failure modes.

Executional literacies make systems **legible to themselves under execution** by forcing reasoning to remain isomorphic to runtime.

Only what survives production depletion persists.
