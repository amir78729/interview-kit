---
id: frontend-js-event-loop-001
title: "Explain the JavaScript event loop"
type: technical
domain: frontend
category: javascript
difficulty: intermediate
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - javascript
  - event-loop
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain how browser tasks, microtasks, and rendering opportunities coordinate when asynchronous JavaScript runs.

# Expected Answer

A browser event loop selects a task, runs it to completion, then performs a microtask checkpoint before the user agent may render and continue. Promise reactions and `queueMicrotask` enqueue microtasks; timers enqueue tasks after their delay threshold, not at an exact execution time. A long task or endless microtask production can delay rendering and input.

# Key Points

- Run-to-completion applies to a job; microtasks drain before the next task; rendering scheduling remains user-agent controlled.
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

- Calling every asynchronous callback a macrotask, or promising that `setTimeout(fn, 0)` runs immediately.

# Follow-up Questions

- How can recursive microtasks make a page unresponsive?

# Related Questions

- Browse other [javascript questions](../javascript/).

# References

- [Javascript documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
