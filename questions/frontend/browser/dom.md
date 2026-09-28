---
id: frontend-browser-dom-001
title: "Explain the DOM as a platform API"
type: technical
domain: frontend
category: browser
difficulty: junior
estimated_minutes: 10
environment: modern standards-based web environments
tags:
  - browser
  - dom
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain what the DOM represents and how it relates to HTML source and JavaScript objects.

# Expected Answer

The DOM is a tree-oriented object model exposed by the browser for a parsed document. It can differ from source markup because parsing repairs or inserts nodes and scripts mutate it. DOM nodes are host objects with interfaces, events, relationships, and lifecycle; the DOM is not JavaScript itself.

# Key Points

- Distinguish attributes from properties; live and static collections differ; semantic structure affects accessibility.
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

- Calling the DOM the raw HTML string or assuming invalid markup remains unchanged.

# Follow-up Questions

- What is the difference between `textContent` and `innerHTML`?

# Related Questions

- Browse other [browser questions](../browser/).

# References

- [Browser documentation](https://developer.mozilla.org/en-US/docs/Web)
