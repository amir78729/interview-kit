---
id: frontend-architecture-state-001
title: "Choose a frontend state strategy"
type: technical
domain: frontend
category: architecture
difficulty: senior
estimated_minutes: 18
environment: modern standards-based web environments
tags:
  - architecture
  - state-management
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Describe how you classify state and choose ownership and tooling for a large frontend application.

# Expected Answer

Classify local UI, shared client, server/cache, URL/navigation, form, and durable offline state. Keep ownership close to consumers, derive rather than duplicate, and use purpose-built server-state caching for remote data semantics. Choose global tools based on update patterns, debugging, consistency, and team needs—not fashion. Define boundaries and migration paths.

# Key Points

- State synchronization is often the real problem; URL can be a durable/shareable source; external stores need subscription correctness.
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

- Putting all state in one global store or duplicating server cache into client state without a policy.

# Follow-up Questions

- How would you prevent stale state across tabs?

# Related Questions

- Browse other [architecture questions](../architecture/).

# References

- [Architecture documentation](https://web.dev/learn/)
