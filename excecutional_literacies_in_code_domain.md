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
  - Examples: executable code, configuration that affects behavior, schemas, ACLs/IAM, deploy gates, tests that fail the pipeline, feature-flag semantics.
- **Runtime-inert artifact**: does not directly affect runtime behavior.
  - Examples: comments, most prose documentation, intent statements without enforcement, style guidelines without gates.
- **Executional validity (code)**: whether reasoning remains correct when compiled into:
  - actual runtime constraints,
  - real failure modes,
  - real deployment/ops coupling,
  - and adversarial pressure where applicable.

---

## Quick Map (Code)
### Literacies and Their Software Failure Surfaces

- **Foundational**: guards against reasoning as if rollback/retries are free and production is a simulator.
- **Constraint**: guards against ignoring complexity/resource ceilings and runtime contracts.
- **Horizon**: guards against drift/accumulation (leaks, queues, logs, dependency decay).
- **Frame**: guards against “winning” design debates that don’t survive runtime.
- **Meaning**: guards against “shared understanding” without interfaces/schemas/tests that can fail.
- **Coordination**: guards against multi-author shared state failures (merge/deploy coupling, externalities).
- **Metrics**: guards against proxy collapse (optimizing dashboards while users suffer).
- **Risk**: guards against tail failures (data corruption, security incidents, cascading outages).
- **Access Control**: guards against confusing status/seniority with actual gating (permissions, credentials, approvals).
- **Forbearance**: guards against mistaking unexercised paths / low load / delayed detection for safety.
- **Consequence Topology**: guards against propagation blindness across degrading execution nodes (including humans).
- **Liveness & Orchestration**: guards against deadlock/livelock/starvation and over-constrained execution spaces under contention and jitter.
- **Adversarial Dynamics**: guards against hostile optimization through interfaces and trust boundaries.
- **Representation**: guards against misusing models (complexity, concurrency, capacity, threat) past their regime.

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
- the process/container/VM/serverless runtime
- memory/CPU/IO scheduling and contention
- network behavior, retries, timeouts, partial failures

### 2) Persistence Surface
- databases, object stores, caches, filesystems
- schema/constraints/indexing
- migrations, backfills, irreversible writes

### 3) Integration Surface
- upstream/downstream services
- API contracts, rate limits, auth, compatibility
- dependency behavior and failure propagation

### 4) Deployment Surface (Gating)
- CI/CD pipelines, build steps, tests
- feature flags, canaries, progressive delivery
- approvals, environment promotion, change management

### 5) Security Surface (Gating + Runtime)
- secrets, credentials, ACLs, IAM roles
- supply chain dependencies
- audit logs, detection, incident response paths

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

- **builds/compiles** vs **does not**
- **executes** vs **annotates**
- **side effects** vs **descriptions**
- **bounded rollback** vs **rollback illusion**
- **staging/simulation** vs **production**
- **local correctness** vs **system correctness under coupling**

### Failure Signature

Reasoning that assumes invisible rollback or free retries, such as:

- “We can revert if it breaks” (while data/schema side effects persist)
- “We’ll just retry” (while retries amplify load or duplicate effects)
- “Tests passed” treated as sufficient proof (while production differs in scale/data/latency)
- “Worked on my machine” (environment non-isomorphism)

### Diagnostic Question

> *Am I reasoning as if production is a simulator with infinite retries, perfect observability, and cheap rollback?*

---

## 1) Constraint Literacy (Code)

### Definition

The ability to distinguish **runtime constraints** (enforced) from preferences and intentions.

Constraints are invariants: runtime enforces them without negotiation.

### Runtime-Load-Bearing Constraints

- time/space complexity and scaling regimes (with real constants)
- memory ceilings, GC pressure, allocator behavior
- CPU saturation, IO wait, bandwidth ceilings
- concurrency limits, queue depth, thread pools
- rate limits and quota enforcement
- API contracts enforced at runtime (schemas, validation, auth)
- timeout budgets and retry policies
- persistence constraints (schema, uniqueness, foreign keys, write amplification)

### Runtime-Inert Substitutes

- “should be fast”
- “don’t call this often”
- “won’t happen in production”
- “we’ll optimize later” (without budgets/gates)

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
- security drift (new exploits, changing threat actor behavior)

### Runtime-Inert Horizons

- “temporary workaround” (without expiry enforcement)
- “future refactor”
- “we’ll fix it next sprint” (without gates)

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
- threat-modeling and trust-boundary analysis (where applicable)

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
- Incidents caused by assumptions not encoded as contracts.

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
- ownership *with enforcement* (on-call rotation, escalation paths, paging policies)

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

- latency (including p95/p99), jitter
- throughput, saturation, queue depth
- memory usage, GC time, error rates
- availability, success rate, burn rate, SLO error budget
- cost metrics (per request, per tenant), resource efficiency
- correctness proxies (data validation failure rates, reconciliation diffs)

### Failure Signature

- Dashboard green while users suffer (wrong slices, wrong percentiles).
- Metric improves because behavior changed, not because system improved.
- Cost pushed outside the measured boundary (downstream pain, user toil).

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
- supply-chain compromise and dependency substitution
- privilege escalation through mis-scoped IAM/ACLs

### Failure Signature

- “Unlikely” treated as “acceptable” despite catastrophic impact.
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
- production data access (PII gates, break-glass processes)

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
### Temporary Non-Enforcement and Unexercised Paths

### Definition

**Forbearance literacy (code)** is the ability to distinguish **runtime or process safety** from **temporary non-enforcement** caused by:

- low load,
- unexercised code paths,
- partial rollout,
- discretionary human intervention,
- delayed detection,
- or adversaries not yet acting.

Lack of failure is not evidence of correctness.

### Runtime Sources of Forbearance

- Code paths not yet exercised in production.
- Feature flags shielding behavior from real traffic.
- Low traffic masking performance or concurrency bugs.
- On-call engineers manually mitigating effects.
- Silent data corruption not yet queried.
- Security exposure not yet exploited.

These are **buffers**, not invariants.

### Core Alphabet (Code)

- **correct execution** vs **untriggered failure**
- **safety** vs **lack of observation**
- **invariant enforcement** vs **human patching**
- **tested under load** vs **not yet exercised**
- **rollback available** vs **damage not yet surfaced**

### Failure Signature

- “It’s been fine so far” used as correctness evidence.
- Shipping unsafe code because incidents haven’t occurred.
- Treating feature flags as safety mechanisms rather than delay mechanisms.
- Confusing manual intervention with system resilience.
- Catastrophic failure when traffic, scale, or adversarial input arrives.

### Diagnostic Question

> *Is this behavior safe, or merely unexercised or temporarily mitigated?*

---

## 10) Consequence Topology Literacy (Code)
### Propagation, Degradation, and Off-Ledger Nodes

### Definition

**Consequence topology literacy (code)** is the ability to model software execution as **propagating consequences** across a directed topology: services, queues, databases, humans, vendors, and institutions.

Nodes have **operational regimes** and **degradation curves**.  
Humans are execution nodes too: on-call, incident response, and manual mitigation are capacities that degrade under sustained load.

### Core Alphabet

- **local side effect** vs **downstream consequence**
- **service boundary** vs **blast radius boundary**
- **buffer** vs **capacity**
- **single-point failure** vs **common-mode failure**
- **nominal regime** vs **off-nominal regime**
- **load** vs **degradation**
- **recovery time** vs **failure time**

### Failure Signature

- Pushing failure onto downstream systems or humans until they collapse.
- Confusing “we can page someone” with resilience.
- Repeated off-nominal operation degrades correctness (incident fatigue, slower response, riskier changes).
- Treating downstream cost as irrelevant because it’s off-dashboard.

### Diagnostic Question

> *Where does this change send consequences, and which nodes (including humans) degrade first under sustained load or off-nominal operation?*

---

## 11) Liveness & Orchestration Literacy (Code)
### Progress Under Contention, Jitter, and Partial Failure

### Definition

**Liveness & orchestration literacy (code)** is the ability to reason about **progress** under constraints: the system must not merely preserve invariants, it must reliably **make forward progress** under contention, jitter, and partial failure.

In software, feasibility is not enough: changes must be **schedulable**, tolerant to variance, and robust to coordination costs.  
Over-constrained designs collapse the executable region to near-zero.

### Core Alphabet

- **feasible** vs **schedulable**
- **safety** vs **liveness** (invariants vs progress)
- **deadlock** vs **livelock** vs **starvation**
- **synchronization** vs **parallelism**
- **throughput** vs **latency** vs **jitter**
- **hard realtime** vs **soft realtime** (tolerance bands)
- **backpressure** vs **overrun**
- **idempotency** vs **duplicate effects** (progress under retries)

### Failure Signature

- Throughput collapses due to contention (lock convoys, thundering herds).
- Systems require unrealistic timing precision (brittle protocols).
- Retry policies create self-amplifying load (liveness death spirals).
- Queues grow without bound; consumers starve; producers stall.

### Diagnostic Question

> *Under contention and variance, do we still guarantee progress—and is the feasible operating region large enough with tolerance?*

---

## 12) Adversarial Dynamics Literacy (Code)
### Hostile Optimization Through Interfaces and Supply Chains

### Definition

**Adversarial dynamics literacy (code)** is the ability to reason about software in environments containing **intentional harm**: attackers optimize against your constraints, metrics, interfaces, and trust boundaries.

As protocols become more symmetric (APIs, cryptography, identity systems), **stakes remain asymmetric**: your private keys must be protected because others’ keys are not practically breachable; your service must resist abuse because an abuser needs only one cheap exploit path.

### Core Alphabet

- **bug** vs **vulnerability**
- **accidental misuse** vs **adversarial abuse**
- **interface boundary** vs **trust boundary**
- **feature surface** vs **attack surface**
- **capability** vs **authorization**
- **deterrence** vs **prevention** vs **detection/response**
- **symmetric protocol** vs **asymmetric cost/power**

### Failure Signature

- “No one would do that” used as a security argument.
- Auth is treated as a UX detail; trust boundaries are implicit.
- Supply chain and dependencies are assumed benign by default.
- Rate limits, quotas, and abuse controls missing or non-enforced.
- Incident response is social, not coupled to controls.

### Diagnostic Question

> *If an attacker wanted the cheapest path to extract value or cause harm, what interface or dependency gives it to them?*

---

## 13) Representation Literacy (Code)
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

- Defending a model beyond its regime (big-O ignores IO; constants dominate).
- Applying single-node reasoning to distributed systems.
- Treating test environment performance as production truth.
- Treating a threat model as static while attackers and surfaces drift.

### Diagnostic Question

> *What does this model compress away, and under what conditions will that hidden mass dominate execution?*

---

## Dependency Structure (Code)

These literacies are not independent.  
In high-coupling software environments, a typical cascade (not universal):

1. Foundational collapses (production treated as simulator)
2. Constraint collapses (runtime ceilings ignored)
3. Horizon collapses (drift/accumulation ignored)
4. Frame collapses (aesthetics replace runtime reasoning)
5. Meaning collapses (assumptions not encoded as contracts)
6. Coordination collapses (process relies on goodwill)
7. Metrics collapses (proxy dominates experience)
8. Risk collapses (tail failures dismissed)
9. Access control collapses (status replaces gating)
10. Forbearance collapses (silence mistaken for safety)
11. Consequence topology collapses (propagation/degradation ignored)
12. Liveness & orchestration collapses (deadlock/over-constraint)
13. Adversarial dynamics collapses (hostile optimization ignored)
14. Representation collapses (models treated as sovereign)

---

## Derived Invariants (Code) — Not Literacies

### Invariant A
> **Only what executes, constrains execution, or gates execution can govern runtime behavior.**

Everything else is annotation.

Annotations can be valuable for humans, but they are not runtime-load-bearing unless they are coupled to enforcement (tests, gates, contracts, tooling).

### Invariant B (Model Error Prior)
> **Assume the model is wrong in some way you did not enumerate.**

Execution-safe reasoning therefore prefers:

- **bounded probes** (canaries, staged rollout) over irreversible commits,
- **containment** (blast-radius limits, circuit breakers) over pure optimization,
- **instrumentation for surprise** (unknown failure classes, anomaly detection),
- **kill-switches and escape hatches** where tail impact is discontinuous.

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
- the adversaries,
- and the failure modes.

Executional literacies make systems **legible to themselves under execution** by forcing reasoning to remain isomorphic to runtime.

Only what survives production depletion persists.
