---
id: frontend-react-reconciliation-001
title: "Explain reconciliation and keys"
type: technical
domain: frontend
category: react
difficulty: intermediate
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - react
  - reconciliation-keys
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain how element type, position, and keys affect state preservation during reconciliation.

# Expected Answer

React associates state with a component’s position in the rendered tree. Matching types and keys allow reuse; changing a key or type can reset state. Keys identify siblings across reorder/insert/delete operations and must be stable and unique among siblings. They are not passed as a normal prop.

# Key Points

- Index keys are risky for mutable lists; keys can intentionally reset state; reconciliation is an implementation strategy with documented identity behavior.
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

- Using random keys, which remounts items, or claiming keys must be globally unique.

# Follow-up Questions

- How would incorrect keys corrupt input state in a reordered list?

# Related Questions

- Browse other [react questions](../react/).

# References

- [React documentation](https://react.dev/learn)
