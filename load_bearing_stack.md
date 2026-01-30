# Load‑Bearing Stack
## A Constraint‑Mapping Account of Bounded Execution

> **Purpose:** specify the **structural preconditions** under which talk of action, evaluation, agency, responsibility, optimization, and governance becomes *well‑formed* for bounded executors operating in drifting environments.

This document is a **minimal execution architecture** for systems where:
- execution is **irreversible**,
- resources (including **energy**) are **bounded**,
- environments are **non‑stationary** (drift),
- and repeated action must remain **viable** over time.

It is **not** a theory of:
- human psychology or cognition,
- intelligence, intent, or consciousness,
- morality, legitimacy, justice, or fairness,
- preference formation, value prescription, or optimization procedures.

It does **not** prescribe goals or mechanisms. It performs **constraint mapping**:
- identifies **necessary structural conditions** for coherent execution,
- marks **impossibility boundaries** (where common claims become undefined),
- preserves **critical separations** that collapse under pressure.

---

## How to read this document
- Treat “layers” as **coexisting regimes** and **interfaces**, not a maturity ladder.
- Use it as a **validator**: if a claim violates a constraint or collapses a separation, the claim is structurally ill‑posed regardless of rhetoric.

---

## Glossary (operational definitions)

- **Executor:** any system that selects actions affecting state under bounded resources and irreversibility.
- **Execution:** state‑changing action with consequences that propagate through coupled state.
- **Irreversibility:** acting eliminates alternatives and destroys information; reversal requires additional execution and cost.
- **Drift:** regime change over time; invariants are conditional, horizon‑bound, and can break.
- **Compression:** discarding distinctions to remain executable under bounds; always lossy.
- **Margin:** slack in time/energy/attention/bandwidth that allows deviation, buffering, or redesign without collapse.
- **Closure:** deliberate termination of interpretation over selected distinctions so repeated execution remains viable.
- **Settlement (settled closure):** closure that persists through repetition and depletion and becomes enforced by failure, not preference.
- **Metric:** a finite executable interface that encodes the degrees of freedom kept within a closure regime.
- **Topology (consequence topology):** the structure by which execution consequences propagate: latency, fan‑out, buffers, observability, irreversibility gradients, dissipation/recovery.
- **Horizon:** timescale over which viability is evaluated (often multiple, partially incompatible horizons).
- **Decidable boundary:** a pre‑execution region where both **acceptance** and **refusal** are real executable paths (interruptible with known failure semantics under sufficient margin).
- **Discretion:** in‑execution adjustment within a closure; not agency attribution.
- **Agency (structural):** attribution that is coherent only at decidable boundaries.
- **Responsibility (structural):** **load attribution** within topology (where coordination pressure and failure cost are located), not moral blame.

---

## Primitive constraints (architectural invariants for bounded executors)

These are not moral claims and not optional design choices. They are the invariants of the **bounded execution problem**.

1. **Execution is irreversible.**  
   Acting commits resources, destroys information, and eliminates alternatives. Undoing requires further execution and additional loss.

2. **Resources are bounded.**  
   No executor can sense/model/store/act on everything. Bounds include time, bandwidth, attention, material capacity, and **energy**.

3. **Environments drift.**  
   Apparent invariants are regime‑dependent, provisional, and horizon‑specific. Stability is always conditional.

4. **Compression is unavoidable.**  
   Feasibility is purchased by blindness. All viable execution discards distinctions; there is no lossless abstraction under bounded execution.

5. **Viability precedes optimization.**  
   A system must remain capable of continued execution and redesign before any notion of “improvement” or “optimality” is coherent.

**Structural incoherence test:** if a framework requires lossless abstraction, infinite resources, reversibility, or stationary environments, it is not describing bounded execution.

---

## Critical separations (do not collapse)

Persistent failure modes arise when these distinctions are conflated:

- **execution** vs **interpretation** (what happens vs what is said about what happens)  
- **existence** vs **persistence** vs **scale** (emerge vs keep going vs become reusable building block)  
- **exploration** vs **exploitation** vs **redesign** (generating options vs repeating cheaply vs reopening distinctions)  
- **regulation** vs **control** (cheap background closure vs costly adaptive intervention)  
- **discretion** vs **agency** (in‑execution adjustment vs boundary‑level choice)  
- **evaluation** vs **optimization** (judgment signals vs executable objective pursuit)

These regimes can be simultaneously active in different subsystems. The point of the stack is to preserve articulation across them under constraint.

---

# The Stack as Constraint Map

## Regime 0 — Existence (coherent execution pattern)

A system **exists** (in this account) when a coherent execution pattern emerges and persists long enough to propagate consequences beyond immediate interaction.

Existence requires:
- coupling to lower‑layer dynamics,
- internal constraints that channel execution,
- non‑immediate decoherence under disturbance.

Existence does **not** require:
- stability/persistence,
- intention/awareness,
- optimization,
- recognition by observers.

Evidence of existence is **causal propagation**, not description or endorsement.

---

## Regime 1 — Coordination pressure (coupled execution under cost)

Coordination is not chosen; it emerges whenever:
- multiple independent processes execute,
- execution affects shared/coupled state,
- information is partial/asymmetric,
- resources are bounded,
- actions are irreversible,
- failure carries non‑trivial cost.

Under these conditions, independent execution becomes unsafe.

**Coordination pressure** is the minimum additional structure required to maintain viability under coupled execution.

### Displacement, subsidy, masking
Coordination pressure may be:
- **buffered** (slack/storage/latency delays failure),
- **subsidized** (external systems absorb cost),
- **displaced** (cost exported elsewhere),
- **masked** (metrics/narratives defer recognition).

Apparent absence of coordination pressure is often evidence of **displacement**, not resolution.

---

## Regime 2 — Optionality preservation (exploration under margin)

Where coordination pressure has not yet bound locally **and margin remains sufficient**:
- interpretation remains open,
- deviation is cheap,
- failures are local and mostly reversible,
- information is preserved rather than destroyed.

This regime is **not** assumed to be optimization, preference discovery, or objective function evaluation.

Evaluation here is typically:
- heuristic and context‑rich,
- non‑comparable across domains,
- not directly executable.

Optionality preservation is **conditional**: it disappears when margin collapses—even without formal closure. It can reappear locally wherever margin is restored (sandboxes, exception paths, redesign boundaries).

---

## Regime 3 — Consequence topology and horizons (how action propagates)

Execution propagates through a **consequence topology** characterized by:
- path length (latency),
- fan‑out (distribution breadth),
- buffers/storage,
- observability/attenuation,
- irreversibility gradients,
- **energy dissipation and recovery**.

Interpretation can lag; intent does not propagate. Only execution persists.

### Horizons
A **horizon** specifies the timescale over which viability is evaluated.

Topology + horizon determine:
- where disturbance appears,
- where it accumulates or dissipates,
- where it becomes invisible.

Systems usually operate across **multiple partially incompatible horizons**. Choosing which horizon binds execution is itself a **closure decision** (explicit or implicit).

---

## Regime 4 — Execution closure (deliberate compression for repetition)

As coordination pressure increases, horizons extend, or margin shrinks, maintaining interpretation over all distinctions becomes unsafe.

**Execution closure** is the deliberate termination of interpretation over selected distinctions so that repeated execution remains viable.

Closure is:
- domain‑specific,
- role‑specific,
- horizon‑specific,
- margin‑dependent.

Closure eliminates distinctions not because they are false, but because they are no longer executable under constraint.

### Closure surface area (useful refinement)
Closures differ along three axes:
- **extent:** how many degrees of freedom are collapsed,
- **coupling:** how many other subsystems depend on the closure,
- **reversibility cost:** difficulty/cost of reopening the distinctions (redesign).

Large‑extent, high‑coupling, high‑cost closures are the primary sources of brittleness and downstream coercion‑like dynamics (structurally, not morally).

---

## Regime 4.1 — Settlement (when closure hardens)

When closure:
- survives repeated execution,
- remains sufficient across relevant horizons,
- persists under depletion (energy/attention),
- eliminates alternatives through **failure** rather than choice,

it becomes **settled**.

At settlement:
- distinctions cease to appear as choices,
- constraints feel descriptive rather than imposed,
- disagreement occurs *within* the representation, not about it.

Settlement sustained mainly by buffering/subsidy/energy injection is **not** genuine local sufficiency; it is a dependence disguised as stability.

---

## Regime 5 — Metrics as executable interfaces (binding evaluation to closure)

Once closure occurs, evaluation must coordinate execution.

**Metrics** are executable interfaces that encode compressed distinctions.

A metric is real‑for‑execution only if it:
- captures minimally sufficient degrees of freedom for viability in the closure regime,
- is finite and resource‑bounded,
- is operationally substitutable within that regime,
- yields determinate outcomes,
- **fails explicitly** when saturated or misapplied.

Metrics do not encode truth; they encode what must be held fixed for viability over a horizon.

Articulated “values” that do not bind compression remain narratively visible but execution‑inert.

---

## Regime 6 — Decidability boundaries and agency (where choice is coherent)

Agency is coherent only at **decidable boundaries**, prior to execution.

A boundary is decidable when it has:
- explicit execution paths,
- bounded consequences (relative to the horizon),
- known failure semantics,
- interruptibility,
- sufficient margin to make **refusal executable**.

A decision is decidable only if **acceptance and refusal are both real execution paths**.

### Symmetry requirement (structural, not moral)
In a coupled topology, agency attribution requires symmetry of refusal *at the boundary in question*. If one party can refuse without catastrophic loss while the other cannot, attributing agency to the constrained party for the coupled outcome is structurally invalid **for that boundary**.

Inside execution, actors exercise **discretion** (adjustment under closure), not agency.

---

## Regime 7 — Responsibility as load attribution (where cost lands)

Responsibility here is not moral blame. It is **load location** within topology.

Responsibility can be coherently assigned only when:
- coordination pressure exists,
- execution closure has occurred,
- metrics are bounded and executable,
- entry was decidable,
- outcomes depend on controlled variables within the closure.

Absent these conditions, responsibility claims are structurally undefined or purely rhetorical.

---

## Dynamic operation — Regulation vs control

Viable systems separate:
- **Regulation:** settled, low‑cost background execution over closed distinctions.
- **Control:** costly, adaptive intervention near redesign boundaries.

Regulation absorbs the known. Control confronts the unknown.

Coordination artifacts (metrics, protocols, authority structures) do not eliminate coordination pressure; they route, concentrate, defer, or price it—often inducing secondary closures elsewhere.

---

## Threshold independence (exist / persist / scale)

Three thresholds are independent:
- **Exist:** coherent execution pattern emerges.
- **Persist:** efficient maintenance under disturbance and depletion.
- **Scale:** recognition as a reusable building block at higher layers.

A system may cross any subset without the others.

---

## Complementarity (gap‑filling under bounds)

**Complementarity** is structural coupling that supplies missing degrees of freedom under constraint.

It is not automatically cooperation, alignment, or mutual benefit. It is **gap‑filling** that produces a new composite consequence topology.

Complementarity can enable conditional existence, partial persistence, or limited scale, while also masking fragility via dependency.

---

## Compression, drift, redesign (the recurring cycle)

Because environments drift, all compression is provisional.

Systems cycle through regimes:
1. **Optionality preservation** (margin permits exploration),
2. **Compression/closure** (discard distinctions to remain executable),
3. **Exploitation** (cheap repeated execution under closure),
4. **Redesign** (reintroduce discarded distinctions when invariants break).

Redesign authority cannot be fully expressed through settled metrics, because metrics encode the closure being revised.

Redesign authority tends to reside at boundaries:
- exception paths,
- external couplings,
- interfaces,
- interruptible regions where failure is containable.

Failure to redesign when error patterns violate assumed invariants is a primary collapse mode.

---

## Where values appear (descriptive, not normative)

Values appear through compression decisions:
- which distinctions were discarded,
- when they were discarded,
- where redesign authority resides,
- what survived depletion and repetition.

Values are not injected; they are the residue of irreversible abstraction that survived execution.

This does not deny deliberation; it specifies where deliberation ceases to bind execution unless it binds compression.

---

# Diagnostic use: constraint‑mapping templates (domain‑neutral)

Use these to test whether a claim is *structurally well‑formed*.

## Template A — Is the claim about execution or interpretation?
1. What **actually executes** (state changes)?
2. What is merely **described** (narrative, intent, justification)?
3. Where does description fail to bind execution?

## Template B — Where is coordination pressure?
1. What state is **shared/coupled**?
2. What failures are **non‑trivial** (costly, non‑local, irreversible)?
3. Is pressure resolved, or **buffered/subsidized/displaced/masked**?

## Template C — What closures exist (and what did they discard)?
1. Which distinctions are treated as *non‑choices*?
2. What is the closure’s **extent/coupling/reversibility cost**?
3. Where is the redesign boundary (exception path / interruptibility)?

## Template D — Do metrics bind, and do they fail explicitly?
1. What degrees of freedom do metrics keep?
2. Where do they saturate or become misapplied?
3. Do they **fail loudly**, or do they silently induce proxy capture?

## Template E — Is “agency” being attributed coherently?
1. Identify the **boundary** where choice is claimed.
2. Are acceptance and refusal both **executable paths**?
3. Are consequences bounded and failure semantics known?
4. Is refusal symmetry present for the coupled actors **at that boundary**?

## Template F — Is “responsibility” assignable (as load attribution)?
1. Is there settled closure + bounded metrics?
2. Was entry decidable?
3. Which variables were controllable within the closure?
4. Where in topology does load accumulate (latency, fan‑out, buffers, observability)?

---

# Minimal “worked” vignettes (structural, not domain‑specific)

These are intentionally abstract so they do not require specialized domain knowledge.

## Vignette 1 — Coupled executors without closure
- Two executors, **A** and **B**, affect a shared state **S**.
- Actions are irreversible and bounded; failures are costly.
- Both maintain open interpretation over which distinctions matter.

**Result:** coordination pressure rises. Without closure, each action changes the meaning of the state for the other. Viability degrades because interpretation cannot remain open under repeated coupled execution.

**Constraint‑map output:** closure becomes necessary; if someone claims “we can just keep adapting freely,” ask what margin funds that and what topology contains failure.

## Vignette 2 — Metric introduced as interface
- A closure is chosen: only variables {x, y} are tracked; the rest are discarded.
- A metric **M(x, y)** is adopted to coordinate execution.
- Drift causes a new variable **z** (discarded) to drive outcomes.

**Result:** the metric remains determinate but becomes **misleading**; optimization against M amplifies error. If M does not fail explicitly, proxy capture occurs.

**Constraint‑map output:** redesign boundary must reopen the discarded distinction (bring z back into representation) or change closure/horizon. If redesign authority is trapped inside settled metrics, the system ossifies.

## Vignette 3 — Agency claim under refusal asymmetry
- A boundary decision is presented to **B**: “accept plan P or refuse.”
- Refusal exists on paper, but under topology and horizon, refusal triggers catastrophic loss for B (non‑viable), while A can refuse cheaply.

**Result:** the decision is not decidable for B in the structural sense; attributing agency to B for accepting P is invalid for that boundary. Inside execution, B may still exercise discretion.

**Constraint‑map output:** if someone argues “B chose this,” test whether refusal was executable under bounded consequences with known failure semantics.

---

# Failure modes (structural pathologies)

- **False sufficiency:** settlement appears stable due to subsidy/buffering; local viability is illusory.
- **Silent metric saturation:** metrics never fail explicitly, so drift manifests as gaming/proxy capture rather than alarms.
- **Closure without redesign path:** high‑coupling closure hardens; error accumulates until abrupt collapse.
- **Horizon mismatch:** metrics bind short horizons while viability fails on longer horizons (or vice versa).
- **Agency laundering:** responsibility is attributed where refusal was non‑executable, producing structurally invalid blame/credit.
- **Pressure displacement:** coordination costs are exported to less visible layers until they return as systemic fragility.

---

# Closing (compressed summary)

Execution destroys information.  
Topology routes consequence.  
Energy bounds optionality.  
Compression enables repetition.  
Closure hardens into settlement.  
Metrics bind evaluation to closure.  
Agency exists only at decidable boundaries.  
Responsibility follows load in topology.  

Deliberation, ethics, and intent operate before and around execution; they do not propagate through settled closure unless they bind compression.

Only what executes—and survives depletion—persists.
