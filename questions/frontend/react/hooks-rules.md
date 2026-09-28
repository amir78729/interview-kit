---
id: frontend-react-hooks-001
title: "Explain the Rules of Hooks"
type: technical
domain: frontend
category: react
difficulty: intermediate
estimated_minutes: 10
environment: modern standards-based web environments
tags:
  - react
  - hooks-rules
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain why hooks must be called consistently and how custom hooks share logic.

# Expected Answer

React relies on a stable call order to associate hook state with a component instance. Hooks therefore run at the top level of components or custom hooks, not conditionally or in ordinary callbacks. Custom hooks share stateful logic, not a single state instance; each call has independent hook state unless it connects to shared external state.

# Key Points

- Hook linting finds many violations; custom hook names begin with `use`; conditional behavior belongs inside a hook/effect where appropriate.
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

- Claiming custom hooks automatically share their local state among callers.

# Follow-up Questions

- How can an early return accidentally violate hook ordering?

# Related Questions

- Browse other [react questions](../react/).

# References

- [React documentation](https://react.dev/learn)
