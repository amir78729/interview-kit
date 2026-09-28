---
id: frontend-browser-cookies-001
title: "Reason about secure cookies"
type: technical
domain: frontend
category: browser
difficulty: intermediate
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - browser
  - cookies
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain `Secure`, `HttpOnly`, `SameSite`, domain, path, and expiry attributes and their limitations.

# Expected Answer

`Secure` restricts transmission to secure contexts; `HttpOnly` prevents JavaScript access; `SameSite` controls cross-site sending in defined contexts; domain/path scope delivery but are not authorization boundaries; expiry controls persistence. Prefixes can enforce attribute combinations in supporting browsers. Cookies still require server-side validation and appropriate CSRF/XSS defenses.

# Key Points

- Host-only cookies differ from Domain cookies; SameSite behavior has compatibility/context nuances; never trust path isolation for security.
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

- Saying HttpOnly prevents CSRF or SameSite prevents all cross-origin requests.

# Follow-up Questions

- When would a session cookie be preferable to a persistent cookie?

# Related Questions

- Browse other [browser questions](../browser/).

# References

- [Browser documentation](https://developer.mozilla.org/en-US/docs/Web)
