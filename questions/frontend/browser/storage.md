---
id: frontend-browser-storage-001
title: "Compare browser storage choices"
type: technical
domain: frontend
category: browser
difficulty: intermediate
estimated_minutes: 15
environment: modern standards-based web environments
tags:
  - browser
  - storage
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Compare cookies, Web Storage, IndexedDB, and Cache Storage for common frontend needs.

# Expected Answer

Cookies are small strings attached to matching HTTP requests and support security attributes; Web Storage is synchronous key/value string storage and can block; IndexedDB is asynchronous transactional structured storage; Cache Storage stores request/response pairs, commonly with service workers. Selection depends on server visibility, size, query/transaction needs, lifecycle, privacy, and threat model.

# Key Points

- Storage quotas and eviction vary; none should hold secrets vulnerable to script access; consent and partitioning policies matter.
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

- Putting large application state in cookies or treating local storage as secure.

# Follow-up Questions

- How does an HttpOnly cookie change XSS and CSRF considerations?

# Related Questions

- Browse other [browser questions](../browser/).

# References

- [Browser documentation](https://developer.mozilla.org/en-US/docs/Web)
