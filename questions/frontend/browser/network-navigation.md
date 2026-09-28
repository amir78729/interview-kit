---
id: frontend-browser-navigation-001
title: "Trace browser navigation and loading"
type: technical
domain: frontend
category: browser
difficulty: senior
estimated_minutes: 18
environment: modern standards-based web environments
tags:
  - browser
  - network-navigation
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Trace major steps from entering a URL to an interactive page, noting where performance can be improved.

# Expected Answer

A navigation may involve URL processing, service worker interception, cache lookup, DNS, connection establishment, TLS, HTTP exchange, redirects, response streaming, parsing, subresource discovery, script/style execution, rendering, and later hydration or app startup. Protocol, cache, and browser details vary. Improvements target actual bottlenecks: fewer redirects, connection reuse, compression, critical resources, streaming, reduced blocking work, and smaller client execution.

# Key Points

- Server response time and client work are separate; preload has costs; DOMContentLoaded is not synonymous with usable.
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

- Reciting a fixed order that ignores caches, service workers, multiplexing, or streaming.

# Follow-up Questions

- How would you find the cause of a poor Largest Contentful Paint?

# Related Questions

- Browse other [browser questions](../browser/).

# References

- [Browser documentation](https://developer.mozilla.org/en-US/docs/Web)
