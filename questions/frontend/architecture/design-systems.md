---
id: frontend-architecture-design-system-001
title: "Design a sustainable component system"
type: technical
domain: frontend
category: architecture
difficulty: staff
estimated_minutes: 25
environment: modern standards-based web environments
tags:
  - architecture
  - design-systems
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Describe the architecture and governance of a design system used by multiple product teams.

# Expected Answer

Start with design tokens and accessible primitives, layer composable components and patterns, and define versioning, documentation, testing, ownership, contribution, deprecation, and migration. Balance consistency with escape hatches and product needs. Measure adoption and defects rather than component count. Distribution and theming contracts should be explicit.

# Key Points

- Accessibility is a default; semantic versions alone do not make migrations easy; cross-framework strategy may emphasize tokens and standards.
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

- Building a component catalog without governance, support, or consumer research.

# Follow-up Questions

- How would you roll out a breaking token change?

# Related Questions

- Browse other [architecture questions](../architecture/).

# References

- [Architecture documentation](https://web.dev/learn/)
