---
id: frontend-css-grid-001
title: "Design a responsive CSS Grid"
type: technical
domain: frontend
category: css
difficulty: intermediate
estimated_minutes: 15
environment: modern standards-based web environments
tags:
  - css
  - grid
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain explicit/implicit grids, track sizing, and a responsive layout without brittle breakpoints.

# Expected Answer

Grid defines rows and columns with track sizing functions. `fr` distributes leftover space after other sizing constraints; `minmax()` and repeat with auto-fit/auto-fill can make content-aware responsive tracks. Implicit tracks are created when placement falls outside the explicit grid. Item minimum content sizes can still cause overflow.

# Key Points

- Named areas improve communication; auto-fit and auto-fill differ in empty-track treatment; source order should remain meaningful.
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

- Assuming `1fr` always allows content to shrink to zero.

# Follow-up Questions

- How would subgrid help align nested content?

# Related Questions

- Browse other [css questions](../css/).

# References

- [Css documentation](https://developer.mozilla.org/en-US/docs/Web/CSS)
