---
id: frontend-js-memory-gc-001
title: "Discuss JavaScript memory and garbage collection"
type: technical
domain: frontend
category: javascript
difficulty: senior
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - javascript
  - memory-garbage-collection
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain how reachability-based garbage collection affects frontend memory leaks and how you would investigate one.

# Expected Answer

Engines reclaim objects that are no longer reachable from roots; exact algorithms and timing are implementation details. Leaks occur when no-longer-useful objects remain reachable through listeners, timers, caches, closures, detached DOM references, or global structures. Investigation uses reproducible actions, heap snapshots, allocation timelines, and retained-path analysis.

# Key Points

- Cleanup lifecycle-owned resources; bounded/weak caches can help in appropriate cases; do not depend on collection timing.
- A strong answer states assumptions and connects the model to practical engineering choices.

# Hints

## Hint 1

Start by identifying the underlying model and the boundary at which the behavior is defined.

## Hint 2

Use a small concrete example, then discuss an edge case or tradeoff.

# Evaluation Criteria

- **Strong evidence:** Accurate model, relevant nuance, practical example, and justified tradeoffs.
- **Adequate evidence:** Core behavior is correct and applicable, with only minor omissions.
- **Partial evidence:** Recognizes the concept but contains a material gap or cannot apply it.
- **Insufficient evidence:** Relies on a misconception or does not demonstrate the target model.

# Common Mistakes

- Claiming circular references inherently leak or presenting one collector algorithm as guaranteed by JavaScript.

# Follow-up Questions

- When would `WeakMap` help, and what can it not guarantee?

# Related Questions

- Browse other [javascript questions](../javascript/).

# References

- [Javascript documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
