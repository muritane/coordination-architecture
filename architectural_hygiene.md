# Architectural Hygiene  
## Responsibility Routing, Buffer Ownership, and Topology-Safe Coordination

---

## Status

This document describes **architectural hygiene** as a property of systems that:

- route execution, disturbance, and failure explicitly,
- operate under uncertainty and partial observability,
- include irreversible or horizon-dominant risk,
- and must remain viable without relying on hidden sinks, heroics, or moral pressure.

Architectural hygiene is treated as a **topological and structural condition**, not as:

- a personal virtue,
- a cultural norm,
- a leadership style,
- or an ethical stance.

The perspective is **operational and diagnostic**, not prescriptive or moral.

---

## Scope

This account applies to any system that:

- coordinates multiple executors,
- allocates shared resources,
- propagates disturbance across interfaces,
- substitutes operators or evaluators,
- or accumulates load under repeated execution.

Examples include organizations, infrastructures, protocols, institutions, markets, governance systems, and long-running projects.

---

## What This Document Does Not Do

This document does **not**:

- prescribe generosity or restraint,
- rank behavior morally,
- prohibit helping or sacrifice,
- eliminate trust or goodwill,
- assume adversarial intent,
- or require complete formalization of all responsibilities.

It describes **when systems remain structurally legible under load**, not how people ought to behave.

---

## Intended Use

This document is intended as:

- a lens for diagnosing hidden load concentration,
- a vocabulary for discussing responsibility routing failures,
- a way to reason about refusal without moralization,
- a complement to consequence topology and epistemic hygiene.

It is a **thinking aid**, not a governance framework.

---

## Core Observation

Unhygienic systems rely on **implicit sinks**.  
Hygienic systems do not.

An **implicit sink** is any agent, component, or role that absorbs execution pressure, disturbance, or coordination load **without explicit ownership, bounds, or interfaces**.

---

## Architectural Hygiene (Operational Definition)

In this document, **architectural hygiene** refers to:

> the degree to which a system makes the routing of execution, disturbance, and failure explicit enough that no agent functions as an unbounded, unacknowledged sink.

A hygienic architecture:

- makes responsibility routing legible,
- assigns buffer ownership explicitly,
- allows disconnection without collapse,
- prevents capacity from being silently captured.

---

## The Implicit Sink Anti-Pattern

A recurring coordination failure arises when:

- disturbance is generated upstream,
- routing is undefined or ambiguous,
- and one agent absorbs the signal by default because they can.

That agent becomes an **implicit sink**.

Implicit sinks:

- reduce short-term noise,
- improve apparent stability,
- suppress visible failure.

They also:

- concentrate load,
- hide topology,
- accumulate buffer debt,
- guarantee severe transients when disconnected.

This is not resilience.  
It is **topological misdesign**.

---

## Capacity Is Not a Routing Rule

A primary source of architectural decay is the silent rule:

> “Signals flow to whoever can handle them.”

This rule:

- converts capacity into routing,
- routing into expectation,
- expectation into obligation.

Architecturally, this is invalid.

Capacity is an **agent property**.  
Routing is a **system decision**.

Healthy systems never infer routing from capacity alone.

---

## Responsibility as Explicit Routing

In hygienic systems, responsibility is treated as:

- a declared interface,
- with defined inputs,
- bounded outputs,
- explicit horizons,
- known failure semantics.

Responsibility that cannot be expressed in routing terms  
cannot be safely assigned.

Responsibility is not virtue.  
It is **load direction**.

---

## Buffers, Sinks, and Ownership

Buffers include:

- time,
- attention,
- labor,
- capital,
- slack capacity,
- emotional or cognitive regulation.

Buffers do not eliminate disturbance.  
They store, delay, or transform it.

Every buffer has an owner who bears:

- storage cost,
- maintenance cost,
- opportunity cost,
- tail risk.

Architectural hygiene requires that **buffer ownership be explicit**.

Unowned buffers become implicit sinks.

---

## Failure Localization vs Failure Dissipation

Systems respond to disturbance in two structural ways.

### Failure dissipation (via sinks)

- hides origin,
- delays visibility,
- concentrates debt,
- produces brittle stability.

### Failure localization (via routing)

- exposes origin,
- limits blast radius,
- forces redesign,
- increases short-term noise.

Architectural hygiene favors **localization**, even when it is uncomfortable.

---

## Disconnection as a Topological Event

When an implicit sink is removed:

- routing changes,
- signals reflect or re-route,
- upstream buffers saturate,
- latent dependencies become visible.

This is not collapse.  
It is **topology asserting itself**.

Signals obey conservation.  
They must land somewhere.

Disconnection reveals structure; it does not create disturbance.

---

## Irreversibility and Hygiene

Under irreversible or horizon-dominant risk:

- hidden sinks become catastrophic,
- delayed routing decisions amplify transients,
- moral pressure substitutes for structure.

In such environments, architectural hygiene is **not optional**.  
It is a safety requirement.

---

## Refusal as a Routing Signal

In hygienic systems, refusal is treated as:

- an impedance mismatch,
- a routing error indicator,
- a signal of missing or overloaded interfaces.

Refusal is **not** treated as:

- defiance,
- selfishness,
- betrayal,
- lack of commitment.

Systems that punish refusal  
force agents to absorb load rather than correct topology.

---

## Renegotiation as Topological Maintenance

Renegotiation is often framed as interpersonal conflict.

Architecturally, it is:

- routing table update,
- buffer reallocation,
- interface clarification.

Discomfort during renegotiation indicates  
that prior stability relied on **implicit sinks**.

---

## Moral Framing as an Architectural Smell

Unhygienic systems stabilize topology using moral language:

- “being reliable,”
- “stepping up,”
- “not dropping the ball,”
- “doing the right thing.”

Operationally, these phrases often mean:

> “Continue absorbing signals we have not routed.”

Hygienic systems rely on:

- explicit interfaces,
- visible constraints,
- inspectable routing,
- renegotiable ownership.

Morality may exist.  
It must not carry topology.

---

## Relationship to Epistemic Hygiene

Architectural hygiene depends on epistemic hygiene.

Routing cannot be explicit if:

- structure is opaque,
- buffers are invisible,
- failure paths are mystified,
- ownership is ambiguous.

Inspectable structure is what allows sinks to be removed  
without destabilizing the system.

---

## Relationship to Consequence Topology

Architectural hygiene is the **preventive counterpart** to consequence topology.

Where consequence topology explains:

- how disturbance propagates after execution,

architectural hygiene ensures:

- propagation paths are known,
- buffers are owned,
- horizons are respected  
**before execution**.

---

## Why Hygienic Systems Feel “Colder”

Removing implicit sinks eliminates:

- heroics,
- silent sacrifice,
- flattering dependence,
- asymmetric obligation.

This can feel:

- less warm,
- less personal,
- less generous.

What replaces them is:

- survivability,
- predictability,
- bounded cooperation under load.

---

## Common Degradation Patterns

Architectural hygiene degrades when systems:

- infer routing from capacity,
- reward absorption over correction,
- personalize topology failures,
- delay renegotiation,
- moralize impedance mismatches,
- treat sinks as virtues.

These failures accumulate quietly  
until disconnection becomes violent.

---

## Summary (Compressed)

- Architectural hygiene prevents implicit sinks.
- Capacity does not define routing.
- Responsibility must be explicit and bounded.
- Buffers must be owned.
- Signals obey conservation.
- Disconnection reveals topology.
- Refusal is a routing signal.
- Trust cannot replace structure.

---

## Status Note

This document is intentionally incomplete.

Its usefulness depends on:

- exposure to real execution,
- willingness to revise routing,
- resistance to moral substitution.

Systems that require unbounded sinks to function  
are not cooperative.

They are **miswired**.

---

## Closing

Architectural hygiene is not about doing less.

It is about **not letting systems run on invisible dissipation borrowed from specific agents**.

When topology is explicit:

- signals route,
- buffers fill,
- failures localize,
- redesign becomes possible.

No one needs to be a sink.

That is coordination without illusion.
