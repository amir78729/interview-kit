---
id: frontend-react-effects-001
title: "Use React effects appropriately"
type: technical
domain: frontend
category: react
difficulty: intermediate
estimated_minutes: 15
environment: modern standards-based web environments
tags:
  - react
  - effects
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain what effects are for, how dependencies work, and when an effect is unnecessary.

# Expected Answer

Effects synchronize React with external systems such as subscriptions, network connections, imperative widgets, or browser APIs. Dependencies list reactive values read by the effect; cleanup undoes setup before rerun/unmount. Pure derivation and event-specific logic usually belong in render or event handlers, not effects. Development replays can reveal missing cleanup.

# Key Points

- Avoid suppressing dependency analysis; handle races/cancellation; effects run after commit and do not make server rendering perform client effects.
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

- Using an effect to mirror props into redundant state or making an async effect callback directly.

# Follow-up Questions

- How would you prevent stale network responses from winning?

# Related Questions

- Browse other [react questions](../react/).

# References

- [React documentation](https://react.dev/learn)
