---
id: frontend-css-flexbox-001
title: "Reason about Flexbox sizing and alignment"
type: technical
domain: frontend
category: css
difficulty: intermediate
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - css
  - flexbox
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain the main/cross axes, flex sizing, and a common cause of overflowing flex children.

# Expected Answer

Flexbox lays items along a main axis and aligns across a cross axis. Flex basis establishes the starting size before free space is distributed by grow/shrink factors. Automatic minimum sizes can prevent shrinking below content; `min-width: 0` (or the relevant axis equivalent) is often needed for truncation in a flex child.

# Key Points

- Axes depend on direction/writing mode; `justify-content` uses main axis; gaps avoid margin edge cases.
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

- Treating `flex: 1` as identical in all sizing contexts or memorizing horizontal/vertical alignment.

# Follow-up Questions

- When should Grid be chosen over Flexbox?

# Related Questions

- Browse other [css questions](../css/).

# References

- [Css documentation](https://developer.mozilla.org/en-US/docs/Web/CSS)
