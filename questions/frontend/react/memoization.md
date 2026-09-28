---
id: frontend-react-memoization-001
title: "Evaluate React memoization"
type: technical
domain: frontend
category: react
difficulty: senior
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - react
  - memoization
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain `memo`, `useMemo`, and `useCallback`, including when they do not help.

# Expected Answer

Memoization is a performance optimization, not a semantic guarantee. `memo` may skip rendering when props compare equal; `useMemo` caches a calculated value and `useCallback` caches a function identity between matching dependencies. They help when measured work or identity-sensitive children justify their comparison, dependency, and complexity costs.

# Key Points

- Fix impure rendering first; unstable object/function props defeat shallow comparison; profile before and after.
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

- Memoizing every value or using memoization to fix correctness.

# Follow-up Questions

- How can moving state or JSX reduce the need for memoization?

# Related Questions

- Browse other [react questions](../react/).

# References

- [React documentation](https://react.dev/learn)
