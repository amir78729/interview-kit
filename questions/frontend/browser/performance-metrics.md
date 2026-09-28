---
id: frontend-browser-performance-001
title: "Use user-centric web performance metrics"
type: technical
domain: frontend
category: browser
difficulty: senior
estimated_minutes: 15
environment: modern standards-based web environments
tags:
  - browser
  - performance-metrics
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain how you would assess loading, responsiveness, and visual stability for real users.

# Expected Answer

Use field data where possible and lab diagnostics to understand it. Core Web Vitals currently emphasize LCP for loading, INP for interaction responsiveness, and CLS for visual stability; definitions and thresholds can evolve, so consult current official guidance. Segment by device/network/page and connect metrics to traces. Optimize causes, not the score alone.

# Key Points

- Field distributions differ from a fast local machine; attribution matters; accessibility and correctness are not captured by performance metrics.
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

- Treating Lighthouse as production truth or optimizing an average while ignoring poor percentiles.

# Follow-up Questions

- What can cause high INP even when individual React renders seem fast?

# Related Questions

- Browse other [browser questions](../browser/).

# References

- [Browser documentation](https://developer.mozilla.org/en-US/docs/Web)
