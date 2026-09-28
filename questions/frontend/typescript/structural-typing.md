---
id: frontend-ts-structural-typing-001
title: "Explain structural typing and excess property checks"
type: technical
domain: frontend
category: typescript
difficulty: senior
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - typescript
  - structural-typing
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain TypeScript structural compatibility and why object literals can be checked differently from variables.

# Expected Answer

Compatibility is primarily based on members rather than declared nominal identity. Fresh object literals receive excess property checks in certain assignment/call contexts, catching likely mistakes; assigning through a variable may allow additional properties because structural values can contain more than required. These checks do not strip properties at runtime. Branding patterns can approximate nominal distinctions.

# Key Points

- Function compatibility has additional variance rules; private/protected class members affect compatibility; `satisfies` checks without replacing inferred type.
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

- Believing an interface changes runtime objects or that excess checks enforce exact object shapes universally.

# Follow-up Questions

- When would a branded ID type be worth the cost?

# Related Questions

- Browse other [typescript questions](../typescript/).

# References

- [Typescript documentation](https://www.typescriptlang.org/docs/)
