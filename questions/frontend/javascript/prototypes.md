---
id: frontend-js-prototypes-001
title: "Describe JavaScript prototype lookup"
type: technical
domain: frontend
category: javascript
difficulty: intermediate
estimated_minutes: 10
environment: modern standards-based web environments
tags:
  - javascript
  - prototypes
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Describe how property lookup and inheritance work through JavaScript prototypes, including what happens for an own property.

# Expected Answer

Objects have an internal prototype reference. A missing own property is looked up along that chain until found or the chain ends at `null`. Own properties shadow inherited properties. Constructor functions and `class` syntax arrange prototypes, but classes do not replace the underlying prototype model.

# Key Points

- Distinguish an object prototype from a function’s `prototype` property; lookup is dynamic; mutation of shared prototypes can affect many instances.
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

- Claiming classes use classical inheritance internally or confusing `__proto__` with the preferred reflective APIs.

# Follow-up Questions

- When should composition be preferred to modifying a prototype chain?

# Related Questions

- Browse other [javascript questions](../javascript/).

# References

- [Javascript documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
