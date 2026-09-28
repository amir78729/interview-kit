---
id: frontend-ts-generics-001
title: "Design useful TypeScript generics"
type: technical
domain: frontend
category: typescript
difficulty: intermediate
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - typescript
  - generics
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain when a generic type parameter is useful and how constraints improve an API.

# Expected Answer

Generics express relationships between input and output types while preserving caller-specific information. A parameter should usually appear in more than one meaningful position; otherwise a concrete or unknown type may be clearer. Constraints describe required capabilities without discarding the specific subtype. Inference often makes explicit type arguments unnecessary.

# Key Points

- Use `keyof` relationships for safe property APIs; defaults can simplify APIs; runtime validation is still separate.
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

- Using `any` inside a generic or adding a type parameter that conveys no relationship.

# Follow-up Questions

- How would you type a safe property picker?

# Related Questions

- Browse other [typescript questions](../typescript/).

# References

- [Typescript documentation](https://www.typescriptlang.org/docs/)
