---
id: frontend-browser-http-cache-001
title: "Design HTTP caching behavior"
type: technical
domain: frontend
category: browser
difficulty: senior
estimated_minutes: 15
environment: modern standards-based web environments
tags:
  - browser
  - http-caching
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain freshness, validation, and a safe caching strategy for versioned assets and personalized API responses.

# Expected Answer

`Cache-Control` defines freshness and storage policy; stale responses can be conditionally validated using validators such as ETag or Last-Modified, yielding 304 when unchanged. Fingerprinted immutable assets can have long freshness. Personalized responses need careful `private`, `no-store`, or `Vary` choices and must not leak across users or shared caches.

# Key Points

- `no-cache` means revalidate, not do not store; CDN and browser caches differ; invalidation often uses versioned URLs.
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

- Applying `public` long-lived caching to authenticated responses without understanding cache keys.

# Follow-up Questions

- Compare stale-while-revalidate at HTTP and application layers.

# Related Questions

- Browse other [browser questions](../browser/).

# References

- [Browser documentation](https://developer.mozilla.org/en-US/docs/Web)
