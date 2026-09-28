---
id: frontend-ts-unions-intersections-001
title: "Compare unions and intersections"
type: technical
domain: frontend
category: typescript
difficulty: intermediate
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - typescript
  - unions-intersections
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain union and intersection types, especially for object types and discriminated unions.

# Expected Answer

A union represents values assignable to at least one member; code may use only operations safe for the current narrowed member. An intersection combines requirements and must satisfy all members, which can become impossible for conflicting primitives/properties. Discriminated unions model variants with a common literal tag and support exhaustive handling.

# Key Points

- Property access on unions depends on safe common knowledge; intersections do not merge runtime objects automatically.
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

- Assuming `A | B` exposes every property from both or that intersections perform object merging.

# Follow-up Questions

- How can `never` enforce exhaustive switches?

# Related Questions

- Browse other [typescript questions](../typescript/).

# References

- [Typescript documentation](https://www.typescriptlang.org/docs/)
