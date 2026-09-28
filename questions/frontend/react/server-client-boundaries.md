---
id: frontend-react-server-client-001
title: "Reason about React server and client boundaries"
type: technical
domain: frontend
category: react
difficulty: senior
estimated_minutes: 15
environment: modern standards-based web environments
tags:
  - react
  - server-client-boundaries
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain the architectural concerns when dividing a React application between server-rendered/server components and interactive client components.

# Expected Answer

Exact capabilities depend on the framework and React version. Generally, server execution can reduce shipped client code and colocate secure data access, while client components own browser APIs, local interactivity, and effects. Serializable boundaries, hydration consistency, caching, request waterfalls, security, and bundle placement must be explicit. Server-rendered HTML does not make secrets safe if serialized to clients.

# Key Points

- State the framework/version; minimize client boundaries thoughtfully; avoid environment-dependent values causing hydration mismatches.
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

- Presenting one framework’s conventions as universal React semantics.

# Follow-up Questions

- Where should authentication and authorization checks occur?

# Related Questions

- Browse other [react questions](../react/).

# References

- [React documentation](https://react.dev/learn)
