---
id: frontend-browser-accessibility-001
title: "Build an accessible interactive control"
type: technical
domain: frontend
category: browser
difficulty: intermediate
estimated_minutes: 15
environment: modern standards-based web environments
tags:
  - browser
  - accessibility
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Describe how to implement and verify an accessible custom interactive control.

# Expected Answer

Prefer a native semantic element because it supplies keyboard, focus, roles, states, and platform behavior. If custom behavior is unavoidable, implement the appropriate accessible name, role/state, keyboard interaction, focus management, and visible focus while preserving pointer/touch operation. Test with keyboard, automated checks, and representative assistive technology.

# Key Points

- ARIA changes accessibility semantics, not behavior; disabled semantics differ; label and instructions matter.
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

- Adding `role="button"` to a div without keyboard and focus behavior.

# Follow-up Questions

- When should focus move after a dialog opens and closes?

# Related Questions

- Browse other [browser questions](../browser/).

# References

- [Browser documentation](https://developer.mozilla.org/en-US/docs/Web)
