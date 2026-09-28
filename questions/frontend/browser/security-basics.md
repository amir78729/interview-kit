---
id: frontend-browser-security-001
title: "Explain foundational frontend security controls"
type: technical
domain: frontend
category: browser
difficulty: senior
estimated_minutes: 18
environment: modern standards-based web environments
tags:
  - browser
  - security-basics
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Describe practical defenses against XSS, CSRF, clickjacking, and unsafe dependency or message handling.

# Expected Answer

Prevent XSS through contextual output encoding, safe DOM APIs, sanitization for intentionally allowed HTML, and defense-in-depth CSP. Address CSRF with SameSite strategy plus tokens/origin checks where needed. Use frame restrictions (`frame-ancestors`), validate `postMessage` origins and payloads, minimize third-party code, and enforce authorization server-side.

# Key Points

- Security headers complement code; HTTPS protects transport, not malicious script; threat modeling determines controls.
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

- Relying on client validation or CSP as the only XSS defense.

# Follow-up Questions

- How would Trusted Types fit into an XSS defense?

# Related Questions

- Browse other [browser questions](../browser/).

# References

- [Browser documentation](https://developer.mozilla.org/en-US/docs/Web)
