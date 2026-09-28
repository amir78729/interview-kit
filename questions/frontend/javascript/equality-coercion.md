---
id: frontend-js-equality-coercion-001
title: "Explain equality and coercion"
type: technical
domain: frontend
category: javascript
difficulty: intermediate
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - javascript
  - equality-coercion
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain the practical differences among strict equality, loose equality, and `Object.is`.

# Expected Answer

Strict equality avoids type coercion but treats `NaN` as unequal to itself and `+0`/`-0` as equal. `Object.is` reverses those two edge behaviors. Loose equality follows a specified coercion algorithm and can be useful only when its cases are deliberately understood; most application code benefits from explicit normalization and strict equality. Objects compare by identity.

# Key Points

- Know `null == undefined` and no other nullish loose matches; relational and addition coercion have different rules; avoid folklore tables as a substitute for reasoning.
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

- Saying strict equality compares object contents or that all coercion is random.

# Follow-up Questions

- Why do React state comparisons commonly use `Object.is` semantics?

# Related Questions

- Browse other [javascript questions](../javascript/).

# References

- [Javascript documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
