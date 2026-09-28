---
id: frontend-ts-inference-001
title: "Reason about TypeScript inference and conditional types"
type: technical
domain: frontend
category: typescript
difficulty: senior
estimated_minutes: 15
environment: modern standards-based web environments
tags:
  - typescript
  - inference-advanced
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain contextual typing, literal widening, and one practical use of conditional types with `infer`.

# Expected Answer

Inference flows from initializers, arguments, return expressions, and contextual expected types. Mutable declarations often widen literals while `as const` preserves literal/readonly information. Conditional types can extract related pieces using `infer`, such as a function return type, but distributive behavior over unions must be understood. Explicit annotations are useful at public boundaries.

# Key Points

- `satisfies` validates compatibility while retaining useful inference; overloads and generics can influence inference direction.
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

- Using `as const` everywhere or building opaque type puzzles instead of clear contracts.

# Follow-up Questions

- How can tuple wrapping prevent distributive conditional behavior?

# Related Questions

- Browse other [typescript questions](../typescript/).

# References

- [Typescript documentation](https://www.typescriptlang.org/docs/)
