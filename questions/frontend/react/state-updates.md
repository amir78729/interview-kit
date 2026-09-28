---
id: frontend-react-state-001
title: "Reason about React state updates"
type: technical
domain: frontend
category: react
difficulty: intermediate
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - react
  - state-updates
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain batching, snapshots, and functional state updates in React.

# Expected Answer

Each render observes a snapshot of state. Setting state requests a future render; it does not alter the current render’s captured value. React commonly batches updates. When next state depends on previous state, an updater function avoids stale snapshot assumptions and composes queued updates correctly. State should be treated immutably so identity changes communicate updates.

# Key Points

- Derived values often need no state; preserve minimal source of truth; updates may be prioritized.
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

- Mutating an object and setting the same reference or expecting a setter to update a local variable immediately.

# Follow-up Questions

- When should state be lifted, colocated, or derived?

# Related Questions

- Browse other [react questions](../react/).

# References

- [React documentation](https://react.dev/learn)
