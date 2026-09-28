---
id: frontend-html-semantics-001
title: "Explain semantic HTML decisions"
type: technical
domain: frontend
category: browser
difficulty: junior
estimated_minutes: 10
environment: modern standards-based web environments
tags:
  - browser
  - semantics
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain why semantic elements matter and how you choose between native elements and generic containers.

# Expected Answer

Semantic elements communicate document structure and control behavior to browsers, assistive technologies, search systems, and maintainers. Choose an element by meaning and expected interaction, not appearance; style it as needed. Generic `div`/`span` remain valid when no semantic element fits. Correct heading, landmark, list, link, and button semantics reduce custom behavior.

# Key Points

- A link navigates and a button performs an action; visual order and DOM order should remain coherent.
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

- Choosing elements for default styling or adding redundant/incorrect ARIA.

# Follow-up Questions

- When is a heading visually hidden but still useful?

# Related Questions

- Browse other [browser questions](../browser/).

# References

- [Browser documentation](https://developer.mozilla.org/en-US/docs/Web)
