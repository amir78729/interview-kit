---
id: frontend-react-context-001
title: "Design with React context"
type: technical
domain: frontend
category: react
difficulty: intermediate
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - react
  - context
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain when context is appropriate and how it affects rendering and architecture.

# Expected Answer

Context supplies a value to descendants without passing it through each intermediate component. It fits cross-cutting values such as theme or authenticated capabilities, but it is not automatically a complete state-management solution. Consumers update when provider value changes; splitting contexts, stabilizing values, and colocating providers can limit unnecessary work.

# Key Points

- Context creates dependency coupling; defaults do not override an explicit `undefined`; composition may be simpler for local concerns.
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

- Putting a rapidly changing monolithic application state into one context without measuring consumers.

# Follow-up Questions

- How would you expose state and actions through context safely?

# Related Questions

- Browse other [react questions](../react/).

# References

- [React documentation](https://react.dev/learn)
