---
id: frontend-ts-narrowing-001
title: "Explain TypeScript narrowing"
type: technical
domain: frontend
category: typescript
difficulty: intermediate
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - typescript
  - narrowing
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Describe control-flow narrowing and safe treatment of unknown external input.

# Expected Answer

TypeScript narrows unions using checks such as `typeof`, equality, property presence, `instanceof`, truthiness, discriminants, and user-defined predicates. `unknown` requires evidence before use and is safer than `any` at boundaries. Compile-time narrowing does not validate runtime data by itself; parsers or validators are needed for untrusted input.

# Key Points

- Mutations/aliases can invalidate assumptions; assertions bypass proof; truthiness may wrongly exclude valid zero/empty values.
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

- Casting API data to an interface and calling it validated.

# Follow-up Questions

- What is the difference between a type predicate and an assertion function?

# Related Questions

- Browse other [typescript questions](../typescript/).

# References

- [Typescript documentation](https://www.typescriptlang.org/docs/)
