---
id: frontend-architecture-data-001
title: "Design frontend data fetching and caching"
type: technical
domain: frontend
category: architecture
difficulty: senior
estimated_minutes: 20
environment: modern standards-based web environments
tags:
  - architecture
  - data-fetching-caching
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Design a data layer for a product with pagination, mutations, intermittent failures, and several views of the same entities.

# Expected Answer

Define stable query identities, normalized or query-oriented ownership, freshness/staleness, deduplication, cancellation, retries with backoff/jitter, pagination semantics, and mutation invalidation or optimistic updates with rollback. Separate transport errors from domain errors and expose explicit loading/empty/stale states. Coordinate HTTP and application caches deliberately.

# Key Points

- Avoid request waterfalls; authorization remains server-side; idempotency affects retries; offline behavior needs conflict policy.
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

- Using one global TTL for all data or optimistic updates without rollback/reconciliation.

# Follow-up Questions

- How would you keep several cached lists consistent after an edit?

# Related Questions

- Browse other [architecture questions](../architecture/).

# References

- [Architecture documentation](https://web.dev/learn/)
