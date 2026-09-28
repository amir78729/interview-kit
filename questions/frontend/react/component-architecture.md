---
id: frontend-react-component-architecture-001
title: "Design resilient React component APIs"
type: technical
domain: frontend
category: react
difficulty: senior
estimated_minutes: 18
environment: modern standards-based web environments
tags:
  - react
  - component-architecture
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Describe principles for designing reusable component APIs in a large frontend codebase.

# Expected Answer

Good APIs encode accessible defaults, separate behavior from presentation when useful, support composition rather than boolean-prop explosions, and make controlled/uncontrolled ownership explicit. Components should have clear responsibilities, stable semantics, and testable boundaries. Escape hatches are deliberate and documented.

# Key Points

- Prefer domain concepts over implementation props; use children/slots or compound patterns judiciously; preserve type and accessibility guarantees.
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

- Abstracting before repeated use cases are understood or exposing internal DOM structure as a contract.

# Follow-up Questions

- How would you evolve a component API without breaking consumers?

# Related Questions

- Browse other [react questions](../react/).

# References

- [React documentation](https://react.dev/learn)
