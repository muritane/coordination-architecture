# A Core Theory of Action for Bounded Agents

*(Precision-Tightened Concise Form — Revised)*

This whitepaper presents a foundational conceptual framework. Formalization, empirical validation, and implementation details are intentionally deferred.

---

## 1. The Problem

Bounded agents must act in environments that are:

* partially observable,
* noisy and non-stationary,
* costly or unsafe to explore,
* and sometimes adversarial.

Repeated trial-and-error is often infeasible because errors can be irreversible, compounding, or fatal **at the level of the agent’s local trajectory**. Many failures are predictable in hindsight yet recur across biological, artificial, and institutional systems.

**The central question is therefore:**

> How can a bounded agent act reliably over time without repeatedly paying for the same mistakes?

---

## 2. The Irreducible Fact

**Action requires irreversible information loss along the agent’s local trajectory.**

Any pipeline from
*world → perception → representation → model → action*
necessarily maps many possible world states to fewer internal distinctions and ultimately to a single act. This mapping is many-to-one and therefore non-invertible **for the acting agent at the time of action**.

This loss is:

* unavoidable (structural, not merely practical),
* upstream of action,
* and irrecoverable *within the current representational regime* without explicit redesign.

Even with ideal computation and sensing, action collapses distinctions. Therefore, the agent does not merely choose actions—it commits to blindness by eliminating alternatives from future consideration.

Collective systems may preserve discarded distinctions through redundancy, diversity, or external memory, but no individual action escapes local irreversibility.

---

## 3. Reframing the Design Problem

Given irreversible information loss, the primary design problem is not action selection, but:

> **Which distinctions can be safely discarded while preserving the agent’s viability over its operating horizon?**

*Viability* refers strictly to maintaining the minimal preconditions for continued action, learning, coordination, and redesign **at the relevant timescale and agent boundary**. It does **not** imply optimality, growth, dominance, or goal completion.

Intelligence is therefore reframed as a problem of **representation and constraint design**, not downstream optimization.

---

## 4. Central Hypothesis

**Constraints are deliberate commitments to equivalence classes over states.**

More precisely:

> A constraint commits the agent to treating distinct world states as behaviorally identical across a specified class of decisions and timescales.

Equivalently, constraint design is the deliberate destruction of information, chosen so that future decisions remain cheap, stable, and viable within an assumed regime.

This predicts a characteristic tradeoff:

* higher upfront modeling and inference cost,
* fewer downstream decisions,
* bounded variance under noise,
* lower long-term regret within the assumed regime,
* increased brittleness under distributional or causal drift if redesign is delayed.

---

## 5. What “Safe” Information Loss Means

Information destruction is provisionally safe when the discarded distinctions:

* do not participate in causal pathways relevant to continued viability or goals,
* do not shift outcome distributions beyond tolerated risk bounds,
* and remain invariant across the agent’s expected operating regime.

Safety is conditional, regime-dependent, time-bounded, and probabilistic—never absolute.

All safety judgments are counterfactual and fallible: they depend on causal relevance the agent cannot fully observe. No agent can certify safety *ex ante*; it can only bound expected regret under assumed invariants.

Unsafe compression arises when:

* causal structure is misunderstood or misidentified,
* invariants are assumed prematurely,
* redesign signals are suppressed, ignored, or structurally inaccessible,
* or compression authority is exercised without accountability for downstream brittleness.

---

## 6. Phase Structure of Intelligent Systems

Because causal knowledge evolves, intelligent systems necessarily operate in distinct phases.

### Phase 1: Exploration

* Preserve information.
* Maximize optionality.
* Delay irreversible compression.
* Accept inefficiency to infer causal structure.

Exploration is costly and cannot be sustained indefinitely, but premature termination is a dominant failure mode.

---

### Phase 2: Compression

* Identify relatively stable causal structure.
* Deliberately remove degrees of freedom.
* Encode constraints explicitly.
* Make information loss inspectable and revisable.

Compression decisions are epistemic commitments with long-term consequences.

---

### Phase 3: Exploitation

* Act cheaply and repeatably.
* Bound variance.
* Gain diminishing returns from experience.
* Rely on prior representational commitments.

Efficiency increases while adaptability declines.

---

### Phase 4: Redesign

Triggered when observed errors cannot be decorrelated or reduced by parameter adjustment within the current representational frame.

* Reintroduce previously discarded distinctions.
* Update representations, constraints, and models.

Redesign is itself costly, disruptive, and lossy. It cannot fully recover discarded distinctions, only reconstitute approximations under new abstractions.

---

Phase boundaries are not directly observable. They are inferred under compression, and delayed or missed transitions are expected failure modes, not anomalies.

Failure to respect phase boundaries—particularly prolonged exploitation without redesign—is a primary cause of system-level collapse.

Authority over when redesign is permitted or blocked is therefore a critical determinant of long-term viability.

---

## 7. Derived Consequences

From the above:

* Causal modeling precedes efficient action.
* Learning structure matters more than accumulating experience.
* Decisions become cheap because alternatives were eliminated upstream.
* Performance can improve even as adaptability declines.
* Confidence is not evidence of safety.
* Optimization is meaningful only within a fixed representational regime and cannot repair errors introduced by inappropriate compression.
* Redesign capacity and redesign authority are as important as optimization quality.

---

## 8. Models Are Also Subject to the Same Constraints

Causal models are themselves compressed representations.

Therefore:

* models age,
* models become brittle,
* and model redesign obeys the same phase logic as policy redesign.

Model redesign is itself an action subject to irreversible abstraction. No redesign procedure escapes the same constraints it attempts to correct.

There is no final model—only phase-appropriate compression.

---

## 9. Where Values Inevitably Enter

Although the framework does not prescribe goals, it implies that:

> Every compression decision encodes values by selecting which distinctions are allowed to matter, over which timescales, and for whom.

Value alignment and misalignment arise descriptively—not normatively—from:

* what was discarded,
* when it was discarded,
* whose risks were tolerated,
* and who held authority to decide and to redesign.

Governance must therefore attend to epistemic commitments and redesign authority, not only observable outcomes or stated objectives.

---

## 10. Core Synthesis

**Intelligent action is the deliberate, phase-appropriate destruction of information—chosen so that future decisions remain cheap, predictable, and viable—until error patterns inconsistent with assumed causal invariants force redesign under loss.**

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
