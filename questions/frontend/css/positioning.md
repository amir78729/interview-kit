---
id: frontend-css-positioning-001
title: "Explain CSS positioning and containing blocks"
type: technical
domain: frontend
category: css
difficulty: intermediate
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - css
  - positioning
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Compare static, relative, absolute, fixed, and sticky positioning and explain containing blocks.

# Expected Answer

Positioned layout offsets an element relative to a containing block determined by position and ancestors. Relative positioning preserves normal-flow space; absolute removes the box from normal flow; fixed is often viewport-relative but transforms and other properties can establish a containing block; sticky behaves relatively until crossing a scroll threshold within its scroll container.

# Key Points

- Stacking contexts affect z-order; sticky needs an inset and available scroll range; overflow ancestors matter.
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

- Trying arbitrary high `z-index` without finding stacking contexts.

# Follow-up Questions

- Which properties create stacking contexts and why does that matter?

# Related Questions

- Browse other [css questions](../css/).

# References

- [Css documentation](https://developer.mozilla.org/en-US/docs/Web/CSS)
