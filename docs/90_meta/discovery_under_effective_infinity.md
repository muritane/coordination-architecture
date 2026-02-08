# Discovery Under Effective Infinity  
## Bounded Traversal, Prioritized Expansion, and Path Dependence as Executional Invariants

---

## Status and Intent

This document formalizes **discovery** as an executional process that occurs in
**effectively infinite spaces relative to an agent’s resources**.

It is written to be:

- structurally compatible with the **Load-Bearing Stack** type system,
- grounded in **constraint-native agency**,
- and explicit about the executional assumptions that govern discovery.

This is not a psychological, moral, or motivational account.
It is a **structural description of how discovery behaves under bounded execution**.

---

## Core Claim

Discovery is not the act of finding what exists.

Discovery is the process by which an agent
**traverses a space partially**
and thereby determines **what becomes reachable**
*before execution halts*.

In effectively infinite spaces,
**reachability replaces existence**
as the relevant category.

---

## Executional Assumptions (Required)

All claims in this document are typed relative to the following invariants:

1. **Bounded resources**  
   Time, attention, energy, memory, and coordination capacity are finite.

2. **Irreversible execution**  
   Traversal destroys information and collapses alternative paths.

3. **Endogenous or forced halting**  
   Exploration terminates due to resource exhaustion, opportunity cost,
   or external interruption — not optimal completion.

4. **Representational bottlenecks**  
   The agent cannot represent the full space simultaneously;
   representations are shaped incrementally by traversal history.

5. **Delayed or partial evaluation**  
   Value signals are costly, noisy, subjective, drifting, or only locally valid.

These are not pathologies.
They are the baseline conditions for agents acting in real systems.

---

## Effective Infinity

A space need not be mathematically infinite
to behave as infinite for an agent.

A space is **effectively infinite** when:

- full enumeration is infeasible before halting,
- traversal cost dominates evaluation benefit,
- drift invalidates static maps,
- opportunity cost enforces early stopping,
- or representational limits prevent global comparison.

Effective infinity is an **executional property**, not a set-theoretic one.

---

## Closed-World vs Open-World Regimes

### Closed-World (Optimization-Dominant)

Global optimization is well-typed only when all of the following hold:

- a finite and tractable state space,
- explicit and stable objectives,
- cheap evaluation relative to search,
- full observability or enumerable uncertainty,
- reversible or low-cost backtracking.

Examples include:

- sorting,
- shortest-path problems,
- bounded scheduling,
- small games at fixed depth.

In these regimes:

- traversal can be exhaustive,
- rankings are globally meaningful,
- path dependence can be minimized or eliminated.

---

### Open-World (Discovery-Dominant)

Discovery dominates when **any** closed-world condition fails.

Typical failures include:

- unbounded or expanding state spaces,
- expensive or subjective evaluation,
- implicit, contested, or drifting objectives,
- scarce attention and irreversible time,
- high cost of revisiting abandoned paths.

Examples include:

- language acquisition,
- social and cultural discovery,
- scientific research,
- career navigation,
- dating markets,
- large-scale search and recommendation systems.

In these regimes:

- traversal is necessarily partial,
- early paths shape future reachability,
- exclusion emerges silently and structurally.

Global optimization is ill-typed here.

---

## Bounded Traversal

Traversal is movement through a possibility space under execution.

Traversal is bounded because:

- time cannot be rewound,
- attention cannot be duplicated,
- energy cannot be spent twice,
- continuation competes with stopping,
- representation saturates.

Therefore the operative question is never:

> “What exists?”

But always:

> “What becomes reachable before traversal halts?”

---

## Halting and Reachability

Halting is a first-class executional primitive.

Traversal halts when:

- resources are exhausted,
- marginal returns fall below opportunity cost,
- external constraints intervene,
- or continuation becomes non-viable.

Once traversal halts:

- unreached regions remain structurally undiscovered,
- not-discovered carries no evaluative meaning,
- absence of discovery is non-informative.

Discovery is defined relative to halting, not existence.

---

## Prioritized Expansion

Because traversal is bounded,
expansion must be prioritized.

Expansion follows signals that have already shown payoff, such as:

- salience,
- frequency,
- reward,
- social reinforcement,
- probability mass in learned models.

This produces:

- rich-get-richer dynamics,
- early advantage amplification,
- starvation of low-signal regions.

This is not bias in the moral sense.
It is an **executional necessity under bounded resources**.

---

## Path Dependence

Path dependence means:

> Future discoverability depends on past traversal.

Once a path is taken:

- alternative regions become costly or unreachable,
- representations are shaped by prior exposure,
- missed structures compound into long-term exclusion.

Traversal is lossy.
Backtracking is expensive or impossible.

Learning sequences
(e.g. alphabet → words → syntax → semantics)
illustrate path dependence clearly.

Discovery presupposes prior representational closure.

---

## Discovery Is Agent-Relative

Discovery does not exist without an agent.

An agent must possess:

- a representation (however partial) of the space,
- a policy for traversal,
- a prioritization scheme,
- and a stopping rule.

Without these:

- nothing is discoverable,
- exposure remains noise.

Discovery is active traversal,
not passive availability.

---

## Machines and Models

Machine systems differ in scale, not in kind.

Large crawlers, recommender systems, and models operate under:

- traversal budgets,
- prioritized expansion,
- rank-biased exploration,
- irreversible conditioning,
- representational compression.

Language models instantiate:

- bounded traversal of a learned manifold,
- prioritized expansion via probability mass,
- path dependence via sequential conditioning.

“Next token” is a special case of:

> next admissible state under bounded resources and a learned prior.

---

## Misclassification Error

Many systems misclassify open-world discovery problems
as closed-world optimization problems.

This produces systematic errors:

- assuming equal access implies equal discovery,
- treating visibility as quality,
- interpreting non-discovery as failure,
- offering advice that presumes exhaustive search.

These are **type errors**, not moral failures.

They arise from denying effective infinity.

---

## Implications

In effectively infinite spaces:

- equal access does not imply equal reachability,
- improvement does not guarantee visibility,
- failure to be discovered is not evidence of low quality,
- responsibility cannot be assigned via outcome alone,
- optimization claims require explicit viability witnesses.

Systems that deny effective infinity
misattribute agency, merit, and blame.

---

## Compression

Discovery is not finding what exists.

Discovery is the bounded traversal of what
prior paths, constrained resources,
representational bottlenecks,
and halting rules make reachable
before execution stops.

Global optimization re-emerges
only when the space collapses back into a closed world.

Everything else is discovery —
and discovery is path-dependent by construction.
