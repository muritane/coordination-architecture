# Architectural Hygiene

## Field Notes on Responsibility Routing, Buffer Ownership, and Topology-Safe Coordination

---

## What This Document Is

This document describes **architectural hygiene** as a property of systems that:

- route execution, disturbance, and responsibility explicitly,
- operate under uncertainty and partial observability,
- include irreversible or horizon-dominant failure modes,
- and must remain viable without relying on hidden sinks, heroics, or moral pressure.

Architectural hygiene is treated as a **topological and structural condition**, not:
- a personal virtue,
- a cultural norm,
- a leadership style,
- or an ethical stance.

The perspective is **operational and diagnostic**, not normative.

---

## What This Document Is Not

This document does **not**:

- prescribe generosity or restraint,
- rank behaviors morally,
- prohibit helping or sacrifice,
- eliminate trust or goodwill,
- require full formalization of all responsibilities.

It does not assume adversarial agents.
It does not assume benevolence.

---

## Intended Use

This document is meant to function as:

- a lens for diagnosing hidden load concentration,
- a vocabulary for discussing responsibility routing failures,
- a way to reason about refusal without moralization,
- a complement to epistemic hygiene and consequence topology.

It is a **thinking aid**, not a governance framework.

---

## Core Observation

Unhygienic systems rely on **implicit sinks**.

Hygienic systems do not.

An implicit sink is any agent, component, or role that absorbs disturbance, risk, or coordination load **without explicit ownership, bounds, or interfaces**.

---

## Architectural Hygiene (Operational Definition)

In this document, **architectural hygiene** refers to:

> the degree to which a system makes the routing of execution, disturbance, and failure explicit enough that no agent functions as an unbounded, unacknowledged sink.

A hygienic architecture:
- makes responsibility routing legible,
- assigns buffer ownership explicitly,
- allows disconnection without collapse,
- and prevents capacity from being silently captured.

---

## The Implicit Sink Anti-Pattern

A recurring coordination failure occurs when:

- disturbance is generated upstream,
- routing is undefined or ambiguous,
- and one agent absorbs the signal by default because they can.

This agent becomes an **implicit sink**.

Implicit sinks:
- reduce short-term noise,
- improve apparent stability,
- suppress visible failure.

They also:
- concentrate load,
- hide topology,
- accumulate buffer debt,
- and guarantee severe transients when disconnected.

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

Healthy systems never infer routing rules from capacity alone.

---

## Responsibility as Explicit Routing

In hygienic systems, responsibility is treated as:

- a declared interface,
- with defined inputs,
- bounded outputs,
- known failure modes,
- and explicit horizons.

Responsibility that cannot be described in routing terms
cannot be safely assigned.

---

## Buffers, Sinks, and Ownership

Buffers include:
- time,
- attention,
- labor,
- money,
- emotional regulation,
- slack capacity.

Buffers do not eliminate disturbance.
They store or transform it.

Every buffer has an owner who bears:
- storage cost,
- maintenance cost,
- opportunity cost,
- tail risk.

Architectural hygiene requires that **buffer ownership be explicit**.

Unowned buffers become implicit sinks.

---

## Failure Localization vs Failure Dissipation

Systems survive disturbance in two ways:

### Failure dissipation (via sinks)
- hides origin,
- delays visibility,
- concentrates debt.

### Failure localization (via routing)
- exposes origin,
- limits blast radius,
- forces redesign.

Architectural hygiene favors **localization**, even when it increases short-term noise.

---

## Disconnection Is a Topological Event, Not a Moral One

When an implicit sink is removed:

- routing changes,
- signals reflect or re-route,
- buffers saturate upstream,
- latent dependencies become visible.

This is not collapse.
It is **topology asserting itself**.

Signals obey conservation.
They must land somewhere.

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
- a signal of missing interfaces.

It is not treated as:
- defiance,
- selfishness,
- betrayal.

Systems that punish refusal
force agents to absorb signals rather than correct topology.

---

## Renegotiation as Topological Maintenance

Renegotiation is often misinterpreted as interpersonal conflict.

Architecturally, it is:
- routing table update,
- buffer reallocation,
- interface clarification.

Discomfort during renegotiation indicates
that previous stability relied on **implicit sinks**.

---

## Moral Framing as Architectural Smell

Unhygienic systems stabilize topology using moral language:

- “being reliable,”
- “stepping up,”
- “not dropping the ball,”
- “doing the right thing.”

These phrases often mean:
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

Architectural hygiene requires epistemic hygiene.

Routing cannot be explicit if:
- structure is opaque,
- buffers are invisible,
- failure paths are mystified.

Inspectable structure is what allows sinks to be removed
without destabilizing the entire system.

---

## Relationship to Consequence Topology

Architectural hygiene is the **preventive counterpart** to consequence topology.

Where consequence topology explains:
- how disturbance propagates after execution,

architectural hygiene ensures:
- that propagation paths are known,
- buffers are owned,
- and horizons are respected **before execution**.

---

## Why Hygienic Systems Feel “Less Warm”

Removing implicit sinks eliminates:
- heroics,
- silent sacrifice,
- flattering dependence.

This can feel:
- colder,
- less personal,
- less generous.

What replaces them is:
- survivability,
- predictability,
- and bounded cooperation under load.

---

## Common Degradation Patterns

Architectural hygiene degrades when systems:

- infer routing from capacity,
- reward absorption over correction,
- personalize topology failures,
- delay renegotiation,
- moralize impedance mismatches,
- treat sinks as virtues.

These failures accumulate quietly until disconnection becomes violent.

---

## Summary (Compressed)

- Architectural hygiene prevents implicit sinks.
- Capacity does not define routing.
- Responsibility must be explicit and bounded.
- Buffers must be owned.
- Signals obey conservation.
- Disconnection reveals topology; it does not create disturbance.
- Refusal is a routing signal, not a breach.
- Trust cannot replace structure.

---

## Status

This document is intentionally incomplete.

Its usefulness depends on:
- exposure to real execution,
- willingness to revise routing,
- resistance to moral substitution.

Systems that require unbounded sinks to function
are not cooperative.

They are **miswired**.

---

## Closing Note

Architectural hygiene is not about doing less.

It is about **not letting systems run on invisible dissipation borrowed from specific agents**.

When topology is honest,
no one needs to be a sink.

Signals route.
Buffers fill.
Systems adapt.

That is cooperation without illusion.
