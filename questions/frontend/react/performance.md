---
id: frontend-react-performance-001
title: "Diagnose React performance"
type: technical
domain: frontend
category: react
difficulty: senior
estimated_minutes: 15
environment: modern standards-based web environments
tags:
  - react
  - performance
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

A React page feels slow. Describe a measurement-first investigation and likely optimization categories.

# Expected Answer

Separate network, scripting, rendering, layout, and memory costs using browser tooling and React profiling. Reproduce a user interaction, identify expensive commits/components, then address root causes: state placement, excessive effects, unstable identities, expensive calculations, large DOM/list virtualization, request waterfalls, or asset costs. Verify user-centric metrics after changes.

# Key Points

- Production builds and representative data matter; memoization is one tool; responsiveness includes main-thread work outside React.
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

- Guessing that “too many renders” are the cause without measuring duration or browser work.

# Follow-up Questions

- How would you decide between virtualization and pagination?

# Related Questions

- Browse other [react questions](../react/).

# References

- [React documentation](https://react.dev/learn)
