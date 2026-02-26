# Memrail

Deterministic decision infrastructure.

Memrail is a decision plane: a formal layer that selects the correct action for a given context and emits a complete decision trace for every outcome.

---

## The Problem

As systems become more autonomous, decision logic becomes:

- Embedded inside application code  
- Scattered across workflows  
- Mixed with probabilistic model outputs  
- Hard to reason about or safely evolve  

The gap is not intelligence — it is authority.

---

## What Memrail Introduces

Memrail externalizes decision logic into a formal execution layer.

At a named **decision point**, Memrail:

1. Receives structured context  
2. Evaluates explicit policy  
3. Selects the appropriate action  
4. Emits a deterministic decision trace  

Same policy + same context ⇒ same action.

---

## Core Concepts

**Decision point**  
A named boundary in a system where an action must be chosen.

**Context atoms**  
Normalized facts describing system state at that boundary.

**Policy**  
The explicit mapping from context → action.

**Action selection**  
The deterministic resolution of competing admissible actions.

**Decision trace**  
A structured artifact describing:
- The context received  
- The logic evaluated  
- The action selected  
- The rationale and provenance  

---

## Execution Model

```
events / state
        |
        v
  [ decision point ]
        |
        v
  decision plane
    - normalize context
    - evaluate policy
    - resolve action
    - emit trace
        |
        v
  system executes selected action
```

Memrail does not embed business logic inside application code.  
It separates decision authority from execution.

---

## Where It Applies

- AI agents  
- SaaS workflows  
- Trading systems  
- Robotics  
- Clinical decision support  
- Operational governance  

Any system where actions must be explainable, reproducible, and safe to evolve.

---

## Status

Memrail is currently under active development.

Public specifications and reference artifacts will be released in stages.

---

## Links

Website: https://memrail.com  
Entity definition: https://memrail.com/entity  

Built by Cadenzai, Inc.
