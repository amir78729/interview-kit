---
id: frontend-browser-rendering-001
title: "Explain the browser rendering pipeline"
type: technical
domain: frontend
category: browser
difficulty: senior
estimated_minutes: 15
environment: modern standards-based web environments
tags:
  - browser
  - rendering-pipeline
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Trace a typical path from HTML/CSS bytes to pixels and explain which work frontend code can trigger.

# Expected Answer

The browser parses HTML into a DOM and CSS into a CSSOM, computes styles, creates layout information, paints display items, and composites layers. The exact pipeline and optimizations vary. DOM/style changes can invalidate style or layout; reading geometry after writes can force synchronization. Not every visual change requires layout or paint.

# Key Points

- Streaming and preload discovery affect timing; transforms/opacity can often composite; layers are not free.
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

- Presenting the stages as a rigid one-pass sequence or promoting indiscriminate `will-change`.

# Follow-up Questions

- How would you diagnose layout thrashing?

# Related Questions

- Browse other [browser questions](../browser/).

# References

- [Browser documentation](https://developer.mozilla.org/en-US/docs/Web)
