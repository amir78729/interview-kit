---
id: frontend-js-debounce-throttle-001
title: "Compare debounce and throttle"
type: technical
domain: frontend
category: javascript
difficulty: intermediate
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - javascript
  - debounce-throttle
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Compare debounce and throttle, including leading/trailing behavior and cleanup requirements.

# Expected Answer

Debounce delays execution until activity has been quiet for a configured interval; throttle limits execution frequency during continued activity. Production utilities define leading/trailing behavior, preserve arguments/context if needed, expose cancellation, and clean up timers. The choice depends on desired UX, not merely performance.

# Key Points

- Debounce suits settled input such as search; throttle suits periodic updates; rate limiting does not replace efficient work.
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

- Recreating a wrapper on every render or omitting cancellation when an owner unmounts.

# Follow-up Questions

- How would you test timing behavior deterministically?

# Related Questions

- Browse other [javascript questions](../javascript/).

# References

- [Javascript documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
