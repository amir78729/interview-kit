---
id: frontend-css-cascade-001
title: "Explain the CSS cascade and specificity"
type: technical
domain: frontend
category: css
difficulty: intermediate
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - css
  - cascade-specificity
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain how the browser resolves competing declarations, including origin, importance, layers, specificity, scoping proximity, and source order.

# Expected Answer

The cascade filters by relevance, then considers origin/importance and layer ordering before specificity; later scoping proximity and order can break ties. Specificity compares selector components rather than a base-ten score. Inheritance applies after the cascade when no cascaded value exists for an inheritable property.

# Key Points

- Cascade layers can control architecture; `!important` reverses layer order within an origin; inline style is not simply “infinite specificity.”
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

- Trying to solve architecture with increasingly specific selectors.

# Follow-up Questions

- How do `:is()`, `:where()`, and `:not()` affect specificity?

# Related Questions

- Browse other [css questions](../css/).

# References

- [Css documentation](https://developer.mozilla.org/en-US/docs/Web/CSS)
