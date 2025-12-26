# A Core Theory of Action for Bounded Agents

*(Precision-Tightened Concise Form — Revised)*

---

## 1. The Problem

Bounded agents must act in environments that are:

* partially observable,
* noisy and non-stationary,
* costly or unsafe to explore,
* and sometimes adversarial.

Repeated trial-and-error is often infeasible because errors can be irreversible, compounding, or fatal **along the agent’s local trajectory**, even when they are predictable in hindsight. As a result, many failures recur across biological, artificial, and institutional systems despite accumulated experience and apparent sophistication.

**The central question is therefore:**

> How can a bounded agent act reliably over time without repeatedly paying for the same mistakes, when mistakes cannot always be safely explored or undone?

---

## 2. The Irreducible Fact

**Action entails irreversible information loss along the agent’s local trajectory.**

Any pipeline from
*world → perception → representation → model → action*
necessarily maps many possible world states to fewer internal distinctions and ultimately to a single act. This mapping is many-to-one and therefore non-invertible **for the acting agent at the time the action is taken**.

This irreversibility is:

* structural rather than merely practical,
* upstream of downstream optimization,
* and unrecoverable within the agent’s current representational regime without explicit redesign.

Even with ideal computation, perfect recall, and arbitrarily rich sensors, action collapses distinctions by committing to one branch of a world that could have unfolded otherwise. Logs, simulations, or external records may allow retrospective analysis, but they do not restore the unrealized alternatives to the agent’s actual trajectory.

Collective or distributed systems may preserve discarded distinctions through redundancy, diversity, or external memory. However, **no individual action escapes local irreversibility**, and all agents act locally.

Action therefore does not merely select outcomes; it commits the agent to a future in which certain distinctions are no longer actionable.

---

## 3. Reframing the Design Problem

Given unavoidable local irreversibility, the primary design problem for an intelligent agent is not action selection per se, but:

> **Which distinctions can be safely discarded while preserving the agent’s viability over its operating horizon?**

*Viability* refers strictly to maintaining the minimal preconditions for continued action, learning, coordination, and redesign **at the relevant timescale and agent boundary**. It does **not** imply optimality, efficiency, growth, dominance, or goal completion.

Intelligence is therefore reframed as a problem of **representation and constraint design**, with optimization understood as a downstream activity that operates only within an already-committed representational regime.

---

## 4. Central Hypothesis

**Constraints are deliberate commitments to equivalence classes over states.**

More precisely:

> A constraint commits the agent to treating distinct world states as behaviorally identical across a specified class of decisions, timescales, and operating conditions.

Constraint design is thus the deliberate destruction of information, chosen so that future decisions remain cheap, stable, and viable under assumed causal invariants.

This implies a characteristic tradeoff:

* higher upfront modeling and inference cost,
* fewer downstream decision points,
* reduced variance under noise,
* lower expected regret *within the assumed regime*,
* increased brittleness under distributional or causal drift if redesign is delayed or blocked.

Constraints do not eliminate uncertainty; they bound which uncertainties are allowed to matter.

---

## 5. What “Safe” Information Loss Means

Information destruction is provisionally safe when the discarded distinctions:

* do not participate in causal pathways relevant to continued viability or stated objectives,
* do not shift outcome distributions beyond tolerated risk bounds,
* and remain approximately invariant across the agent’s expected operating regime and time horizon.

Safety is therefore conditional, probabilistic, and time-bounded—never absolute.

All safety judgments are counterfactual and fallible. They depend on causal relevance that the agent cannot fully observe at the time compression decisions are made. No agent can certify safety *ex ante*; it can only bound expected regret under assumed invariants.

Unsafe compression arises when:

* causal structure is misunderstood or misidentified,
* invariants are assumed prematurely or extrapolated too far,
* redesign signals are suppressed, ignored, or structurally inaccessible,
* or compression authority is exercised without accountability for downstream brittleness and loss.

---

## 6. Phase Structure of Intelligent Systems

Because causal knowledge evolves and environments change, intelligent systems necessarily operate in distinct phases characterized by different relationships to information loss.

### Phase 1: Exploration

* Preserve degrees of freedom.
* Maintain optionality.
* Delay irreversible compression where feasible.
* Accept inefficiency to infer causal structure.

Exploration never literally preserves all information—compression is unavoidable—but it minimizes *commitment* to specific equivalence classes. Exploration is costly and cannot be sustained indefinitely, yet premature termination is a dominant failure mode.

---

### Phase 2: Compression

* Identify relatively stable causal structure.
* Deliberately remove degrees of freedom.
* Encode constraints explicitly.
* Make information loss inspectable and revisable.

Compression decisions are epistemic commitments with long-term consequences. They define which distinctions are allowed to matter and which are rendered invisible to downstream decision-making.

---

### Phase 3: Exploitation

* Act cheaply and repeatably.
* Bound variance.
* Achieve diminishing returns from experience.
* Rely on prior representational commitments.

Efficiency increases while adaptability declines. Performance may continue to improve even as the system becomes increasingly brittle to unmodeled change.

---

### Phase 4: Redesign

Triggered when observed errors cannot be decorrelated, bounded, or corrected within the current representational frame.

* Reintroduce previously discarded distinctions where possible.
* Update representations, constraints, and models.

Redesign is itself costly, disruptive, and lossy. It cannot be assumed to recover discarded information; at best, it reconstructs approximations under new abstractions.

---

Phase boundaries are not directly observable. They are inferred under compression, and delayed or missed transitions are expected failure modes rather than anomalies.

Failure to respect phase boundaries—particularly prolonged exploitation without redesign—is a primary cause of system-level collapse. Authority over when redesign is permitted, delayed, or blocked is therefore a critical determinant of long-term viability.

---

## 7. Derived Consequences

From the above:

* Causal structure learning precedes efficient action.
* Representation choice dominates downstream optimization.
* Decisions are cheap because alternatives were eliminated upstream.
* Performance can improve even as adaptability declines.
* Confidence is not evidence of safety.
* Optimization is meaningful only within a fixed representational regime.
* Redesign capacity and redesign authority are as important as optimization quality.

---

## 8. Models Are Also Subject to the Same Constraints

Causal models are themselves compressed representations and therefore inherit the same limitations.

As a result:

* models age,
* models become brittle,
* and model redesign follows the same phase logic as policy redesign.

Model redesign is itself an action subject to irreversible abstraction. No redesign procedure escapes the same constraints it attempts to correct. There is no final model—only phase-appropriate compression under bounded resources.

---

## 9. Where Values Inevitably Enter

Although this framework does not prescribe goals or utilities, it implies that:

> Every compression decision encodes values by determining which distinctions are allowed to matter, over which timescales, and for whom.

Value alignment and misalignment arise descriptively—not normatively—from:

* what was discarded,
* when it was discarded,
* whose risks were tolerated,
* and who held authority to decide and to redesign.

Governance must therefore attend to epistemic commitments and redesign authority, not solely to stated objectives or observable outcomes.

---

## 10. Core Synthesis

**Intelligent action is the phase-appropriate, deliberate destruction of information—chosen so that future decisions remain cheap, predictable, and viable—until error patterns inconsistent with assumed causal invariants force redesign under loss.**

This framework explains:

* why abstraction is unavoidable,
* why efficiency creates brittleness,
* why failures cluster rather than average out,
* and why authority over redesign determines survival.

---

## Scope Clarification

This framework applies to biological, artificial, institutional, and hybrid agents wherever action requires irreversible abstraction under bounded resources.

---

## What Is Intentionally Deferred to Appendices

The following are valuable but non-core and should live outside the core paper:

* detailed causal class taxonomies,
* adversarial and deceptive stability regimes,
* formal diagnostic metrics,
* compression registers and governance mechanisms,
* institutional and political failure modes,
* explicit critiques of over-formal optimization.

Including these would risk over-closure, premature generality, and reduced accessibility.

---

## Why This Core Holds Together

This framework relies only on unavoidable facts:

* resources are bounded,
* observations are partial,
* action is locally irreversible,
* representation loss is unavoidable,
* commitments shape future blindness,
* environments change.

Everything else is downstream.

---

## License

This work is licensed under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**.

You are free to share and adapt this material for any purpose, including commercial use, **provided appropriate attribution is given**.

License text:
[https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)
