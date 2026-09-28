---
id: frontend-react-testing-001
title: "Plan tests for a React feature"
type: technical
domain: frontend
category: react
difficulty: intermediate
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - react
  - testing
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Describe a test strategy for an interactive React feature without overcoupling tests to implementation details.

# Expected Answer

Test observable user behavior and accessible roles with component/integration tests, reserve unit tests for isolated logic, and cover critical end-to-end journeys at system boundaries. Control network responses and time deterministically. Include loading, failure, keyboard, and cleanup behavior. Avoid asserting component internals that users cannot observe.

# Key Points

- Layer tests by risk; accessibility queries improve resilience but do not replace full audits; use realistic boundaries.
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

- Snapshotting large trees as the primary confidence mechanism.

# Follow-up Questions

- What belongs in a contract test for the feature API?

# Related Questions

- Browse other [react questions](../react/).

# References

- [React documentation](https://react.dev/learn)
