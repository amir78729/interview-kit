---
id: frontend-architecture-observability-001
title: "Plan frontend observability and quality"
type: technical
domain: frontend
category: architecture
difficulty: senior
estimated_minutes: 18
environment: modern standards-based web environments
tags:
  - architecture
  - observability-testing
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Describe an observability and testing strategy that helps diagnose real user failures without collecting excessive personal data.

# Expected Answer

Combine privacy-conscious error reporting, structured events, performance field metrics, traces/correlation IDs, release metadata, and meaningful product health signals. Apply sampling, redaction, retention, consent, and access controls. Layer static checks, unit/component/integration/contract/end-to-end tests by risk and connect alerts to actionable ownership and runbooks.

# Key Points

- Source maps require controlled access; client telemetry is untrusted; monitor deploy regressions and cohorts.
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

- Logging arbitrary user input or collecting metrics without questions they answer.

# Follow-up Questions

- How would you diagnose a failure spanning browser and backend services?

# Related Questions

- Browse other [architecture questions](../architecture/).

# References

- [Architecture documentation](https://web.dev/learn/)
