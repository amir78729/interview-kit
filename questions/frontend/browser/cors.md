---
id: frontend-browser-cors-001
title: "Explain CORS and preflight requests"
type: technical
domain: frontend
category: browser
difficulty: intermediate
estimated_minutes: 15
environment: modern standards-based web environments
tags:
  - browser
  - cors
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain what CORS controls, when a preflight occurs, and why it is not a server authorization system.

# Expected Answer

CORS is a browser-enforced policy controlling whether frontend JavaScript may read cross-origin responses. Some non-simple requests trigger an `OPTIONS` preflight describing method/headers. The server opts in through response headers. Non-browser clients are not constrained by CORS, so authentication and authorization remain server responsibilities.

# Key Points

- Origin includes scheme/host/port; credentials require explicit compatible headers; wildcard rules have limits.
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

- Trying to fix CORS only in client code or treating a blocked response as a request that never reached the server.

# Follow-up Questions

- How should preflight responses be cached safely?

# Related Questions

- Browse other [browser questions](../browser/).

# References

- [Browser documentation](https://developer.mozilla.org/en-US/docs/Web)
