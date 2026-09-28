---
id: frontend-js-promises-001
title: "Explain promise chaining and error flow"
type: technical
domain: frontend
category: javascript
difficulty: intermediate
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - javascript
  - promises
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain promise state, chaining, value adoption, and how errors travel through a chain.

# Expected Answer

A promise settles once as fulfilled or rejected. `then` returns a new promise: a returned value fulfills it, a thrown error rejects it, and a returned promise or thenable is adopted. Rejections propagate until handled. `finally` is for cleanup and normally preserves the prior outcome unless it throws or returns a rejection.

# Key Points

- Handlers run asynchronously as jobs; attaching handlers does not mutate the original promise; concurrent combinators have distinct failure behavior.
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

- Forgetting to return an inner promise or treating a promise as cancelable by default.

# Follow-up Questions

- Compare `Promise.all`, `allSettled`, `race`, and `any`.

# Related Questions

- Browse other [javascript questions](../javascript/).

# References

- [Javascript documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
