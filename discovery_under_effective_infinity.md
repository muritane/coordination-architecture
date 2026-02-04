# Discovery Under Effective Infinity

## Bounded Traversal, Prioritized Expansion, and Path Dependence as Executional Invariants

---

## Status and Intent

This document formalizes **discovery** as an executional process that occurs in spaces that are **effectively infinite relative to an agent’s capacity**.

It extends the **Constraint-Native Agency** and **Load-Bearing Stack** frameworks by specifying:

* when bounded traversal and path dependence dominate,
* when global optimization is viable,
* and why many modern systems systematically misclassify open-world discovery problems as closed-world optimization problems.

The perspective is structural, not psychological or normative.

---

## Core Claim

Discovery is not universal exploration of what exists.

Discovery is **bounded traversal of what becomes reachable** before execution halts.

This condition holds whenever:

* the state space grows faster than agent capacity,
* evaluation is costly or subjective,
* objectives drift,
* or full enumeration is infeasible in principle.

In such regimes, global optimization is ill-typed.

---

## Effective Infinity (Key Distinction)

A space need not be mathematically infinite to behave as infinite.

A space is **effectively infinite** for an agent when:

* the agent cannot enumerate all options before acting,
* traversal cost dominates evaluation benefit,
* drift invalidates static maps,
* opportunity cost enforces early stopping.

Effective infinity is an **executional property**, not a set-theoretic one.

---

## Closed-World vs Open-World Regimes

### Closed-World (Optimization-Dominant)

Global optimization is viable when all of the following hold:

* finite, tractable state space,
* explicit and stable objectives,
* cheap evaluation relative to search,
* full observability or enumerable uncertainty.

Examples:

* sorting lists
* shortest-path problems
* bounded scheduling
* small games at fixed depth

In these regimes:

* traversal can be exhaustive,
* rankings are meaningful,
* path dependence can be controlled or eliminated.

---

### Open-World (Discovery-Dominant)

Discovery dominates when one or more of the above conditions fail.

Typical failures:

* state space is unbounded or growing,
* evaluation is expensive or subjective,
* objectives are implicit or shifting,
* attention and time are scarce.

Examples:

* language acquisition
* social discovery
* dating markets
* culture and science
* career navigation
* large-scale search and feeds

In these regimes:

* traversal is necessarily partial,
* early paths dominate future reachability,
* exclusion is emergent and silent.

---

## Bounded Traversal

Traversal refers to movement through a possibility space.

Traversal is bounded because:

* time is irreversible,
* attention is finite,
* energy is limited,
* continuation competes with stopping.

Thus the relevant question is never:

> “What exists?”

But always:

> “What becomes reachable before traversal halts?”

---

## Prioritized Expansion

Because traversal is bounded, expansion must be prioritized.

Expansion proceeds along directions that have already shown payoff, such as:

* salience
* frequency
* reward
* social reinforcement
* probability mass (in models)

This produces:

* rich-get-richer dynamics,
* early advantage amplification,
* starvation of alternative paths.

This is not bias in the moral sense.
It is an executional necessity.

---

## Path Dependence

Path dependence means:

> Future discoverability depends on past traversal.

Once a path is taken:

* alternative regions become unreachable or costly to recover,
* representational capacity is shaped by prior exposure,
* missed structures compound into long-term exclusion.

Learning sequences (e.g. alphabet → words → syntax → semantics) illustrate this clearly.

Discovery presupposes prior representational closure.

---

## Discovery Requires an Agent

Discovery is agent-relative.

An agent must already possess:

* a representation of the space,
* a policy for movement,
* a stopping rule.

Without these:

* nothing is discoverable,
* exposure remains noise.

Discovery is active traversal, not passive availability.

---

## Machines and Models

Machine systems differ in scale, not structure.

Even large crawlers and models operate under:

* traversal budgets,
* prioritized expansion,
* rank-biased exploration,
* path dependence.

Language models instantiate:

* bounded traversal of a learned manifold,
* prioritized expansion via probability mass,
* irreversible collapse via sequential conditioning.

“Next token” is a special case of:

> next admissible state under bounded resources and a learned prior.

---

## Implications

In effectively infinite spaces:

* equal access does not imply equal discovery,
* improvement does not guarantee visibility,
* failure to be discovered is not evidence of low quality,
* advice assuming exhaustive search is under-typed.

Systems that deny effective infinity misattribute agency and responsibility.

---

## Compression

Discovery is not finding what exists.

Discovery is traversing what prior paths, bounded resources, and stopping rules make reachable before execution halts.

Global optimization re-emerges only when the space collapses back into a closed world.

Everything else is discovery — and discovery is path-dependent by construction.
