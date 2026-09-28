---
id: frontend-react-rendering-001
title: "Explain React rendering and committing"
type: technical
domain: frontend
category: react
difficulty: intermediate
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - react
  - rendering
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain what it means for a React component to render and how that differs from updating the DOM.

# Expected Answer

Rendering calls components to calculate a next UI description. React then reconciles that result with previous work and commits necessary host changes. A component can render without its DOM changing. Render should be pure because work may be repeated, interrupted, or discarded in modern React environments.

# Key Points

- State updates request work rather than synchronously mutating DOM; commit is where effects tied to the DOM occur; development Strict Mode can expose impurities.
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

- Treating every render as a DOM rewrite or placing side effects in render.

# Follow-up Questions

- What causes a component to render, and which causes can memoization skip?

# Related Questions

- Browse other [react questions](../react/).

# References

- [React documentation](https://react.dev/learn)
