# A Core Theory of Action for Bounded Agents

*(Precision-Tightened Concise Form — Whitelist-Integrated Revision)*

---

## 1. The Problem

Bounded agents must act in environments that are:

* partially observable,
* noisy and non-stationary,
* costly or unsafe to explore,
* and sometimes adversarial.

Repeated trial-and-error is often infeasible because errors can be irreversible, compounding, or fatal **along the agent’s local trajectory**, even when predictable in hindsight. As a result, failures recur across biological, artificial, and institutional systems despite accumulated experience.

**The central question is therefore:**

> How can a bounded agent act reliably over time without repeatedly paying for the same mistakes, when mistakes cannot always be safely explored, undone, or delegated?

---

## 2. The Irreducible Fact

**Action entails irreversible information loss along the agent’s local trajectory.**

Any pipeline from
*world → perception → representation → model → action*
necessarily maps many possible world states to fewer internal distinctions and ultimately to a single act. This mapping is many-to-one and therefore non-invertible **for the acting agent at the time of action**.

This irreversibility is:

* structural rather than merely practical,
* upstream of optimization,
* unrecoverable without explicit redesign of representations and constraints.

Action does not merely select outcomes; it **collapses future option space** by committing the agent to one branch of reality while foreclosing others.

---

## 3. Reframing the Design Problem

Given unavoidable local irreversibility, the primary design problem is not action selection per se, but:

> **Which distinctions, actions, and commitments are permitted at the agent boundary while preserving long-term viability?**

*Viability* refers strictly to maintaining the minimal preconditions for continued action, learning, coordination, and redesign **at the agent’s boundary and timescale**.

Intelligence is therefore reframed as a problem of:

* representation design,
* constraint design,
* and boundary control,

with optimization operating strictly *inside* already-permitted regions of action.

---

## 4. Central Hypothesis (Constraint-as-Whitelist)

**Constraints function as explicit whitelists over admissible actions, commitments, and state transitions.**

More precisely:

> A constraint commits the agent to treating all non-whitelisted distinctions, actions, or transitions as inadmissible by default, while collapsing permitted states into equivalence classes for efficient control.

Constraint design is thus the **deliberate authorization of a limited action space**, not the reactive prohibition of known failures.

This implies:

* higher upfront modeling and boundary design cost,
* fewer downstream decisions,
* reduced variance and surprise,
* bounded regret within assumed invariants,
* brittleness if the whitelist is not explicitly redesigned under drift.

Blacklisting (enumerating forbidden actions) is insufficient under bounded knowledge; **whitelisting is the only scalable boundary strategy** for agents operating under irreversible action.

---

## 5. Safe Information Loss and Safe Action Authorization

Information destruction and action authorization are provisionally safe when discarded distinctions or disallowed actions:

* do not participate in causal pathways critical to viability,
* do not silently consume future agency, resources, or identity,
* remain invariant over the expected operating regime and horizon.

Safety is:

* conditional,
* probabilistic,
* time-bounded.

No agent can certify safety *ex ante*. It can only define **permitted regions** and monitor for violations that trigger redesign.

Unsafe compression or authorization arises when:

* commitments are made without explicit consent,
* scope is unbounded or ambiguous,
* exit or redesign authority is suppressed,
* or irreversible effects are imposed asymmetrically.

---

## 6. Phase Structure of Whitelist-Controlled Agents

### Phase 1: Exploration (Whitelist Construction)

* Preserve degrees of freedom.
* Restrict action to **safe exploration regions**.
* Delay irreversible commitments.
* Discover causal structure.

Exploration occurs **inside externally or internally enforced whitelists**, not in unconstrained space.

---

### Phase 2: Compression (Whitelist Fixation)

* Identify stable causal invariants.
* Explicitly authorize limited actions and commitments.
* Encode constraints as inspectable boundaries.

Compression defines what the agent is **allowed to do**, not merely what it believes.

---

### Phase 3: Exploitation (Whitelist Execution)

* Act cheaply and repeatably.
* Stay within authorized boundaries.
* Improve performance without expanding scope.

Efficiency increases while adaptability declines.

---

### Phase 4: Redesign (Whitelist Revision)

Triggered when:

* errors cluster,
* violations cannot be decorrelated,
* or outcomes escape permitted bounds.

Redesign explicitly **reopens the whitelist**, reintroducing distinctions and revising authorization.

Redesign authority is a first-class survival variable.

---

## 7. Derived Consequences

* Boundary design precedes optimization.
* Safe agency requires whitelists, not blacklists.
* Decisions are cheap because action space was restricted upstream.
* Performance can improve while future agency declines.
* Confidence is not evidence of boundary adequacy.
* Redesign authority determines survival more than optimization quality.

---

## 8. Models Are Also Whitelist-Constrained

Models are compressed representations operating **inside authorized abstractions**.

Therefore:

* models age,
* models lie if treated as complete,
* model redesign follows the same whitelist logic as policy redesign.

There is no final model—only **phase-appropriate authorization under bounded resources**.

---

## 9. Values, Consent, and Governance

Although this framework does not prescribe goals, it implies:

> Every authorization decision encodes values by determining which actions are permitted, for how long, and under whose authority.

Value alignment arises from:

* explicit consent,
* bounded scope,
* symmetric risk,
* and preserved redesign authority.

Governance failures are boundary failures.

---

## 10. Core Synthesis (Whitelist Form)

**Intelligent action is the phase-appropriate, explicit authorization of a limited action space—chosen so that future decisions remain viable—until violations of assumed invariants force redesign under irreversible loss.**

This explains:

* why abstraction is unavoidable,
* why efficiency creates brittleness,
* why failures cluster,
* why exit conditions matter,
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
* boundaries determine agency,
* commitments collapse future options,
* environments change.

Everything else is downstream.

---

## License

This work is licensed under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**.

You are free to share and adapt this material for any purpose, including commercial use, **provided appropriate attribution is given**.

License text:
[https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)
