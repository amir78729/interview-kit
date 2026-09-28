---
id: frontend-css-responsive-001
title: "Plan responsive, content-driven CSS"
type: technical
domain: frontend
category: css
difficulty: intermediate
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - css
  - responsive-design
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Describe a responsive strategy that works across devices, zoom levels, and content variation.

# Expected Answer

Start with flexible flow, intrinsic sizing, relative units, and resilient components; add media or container queries where layout genuinely needs to change. Preserve readable line lengths, touch targets, zoom/reflow, and source order. Test long text, localization, user font settings, and reduced-motion/preferences.

# Key Points

- Breakpoints should follow content; container queries support reusable components; responsive images reduce waste.
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

- Designing only for a list of device widths or disabling zoom.

# Follow-up Questions

- How would you select `srcset` and `sizes` for a responsive image?

# Related Questions

- Browse other [css questions](../css/).

# References

- [Css documentation](https://developer.mozilla.org/en-US/docs/Web/CSS)
