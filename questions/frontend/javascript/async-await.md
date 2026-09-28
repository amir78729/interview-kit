---
id: frontend-js-async-await-001
title: "Reason about async and await"
type: technical
domain: frontend
category: javascript
difficulty: intermediate
estimated_minutes: 10
environment: modern standards-based web environments
tags:
  - javascript
  - async-await
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Describe what `async` and `await` do, including sequencing, errors, and independent operations.

# Expected Answer

An async function always returns a promise. `await` pauses that async function, not the whole thread, and continuation is scheduled asynchronously after the awaited value settles. Rejection behaves like a thrown exception and can be handled with `try`/`catch`. Independent operations should often be started before awaiting them together to avoid accidental serialization.

# Key Points

- Await accepts non-promises through promise resolution; use structured error handling; concurrency is not parallel CPU execution.
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

- Awaiting independent requests one by one without recognizing the latency cost.

# Follow-up Questions

- How would you handle cancellation with `AbortController`?

# Related Questions

- Browse other [javascript questions](../javascript/).

# References

- [Javascript documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
