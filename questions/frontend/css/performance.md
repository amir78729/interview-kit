---
id: frontend-css-performance-001
title: "Evaluate CSS performance choices"
type: technical
domain: frontend
category: css
difficulty: senior
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - css
  - performance
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain which CSS performance concerns matter and how you would validate an optimization.

# Expected Answer

Measure style recalculation, layout, paint, compositing, asset transfer, and user metrics before acting. Reduce invalidation and DOM complexity where traces identify costs; avoid forced layout loops, expensive visual effects over large areas, and oversized unused payloads. Modern selector matching is optimized, so simplistic “never use this selector” rules are rarely the primary answer.

# Key Points

- Containment can isolate work but changes layout semantics; animations should respect reduced motion; layer promotion consumes memory.
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

- Micro-optimizing selector syntax while ignoring layout, paint, or network bottlenecks.

# Follow-up Questions

- How can CSS containment improve and harm a component?

# Related Questions

- Browse other [css questions](../css/).

# References

- [Css documentation](https://developer.mozilla.org/en-US/docs/Web/CSS)
