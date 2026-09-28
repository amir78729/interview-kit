---
id: frontend-js-event-delegation-001
title: "Explain event delegation"
type: technical
domain: frontend
category: javascript
difficulty: intermediate
estimated_minutes: 10
environment: modern standards-based web environments
tags:
  - javascript
  - event-delegation
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain event delegation, its benefits, and cases requiring care.

# Expected Answer

Delegation attaches a listener to an ancestor and identifies relevant descendants as events propagate. It reduces listener management and naturally handles dynamically added children. Robust code uses `closest` plus containment checks and understands bubbling, composed paths, shadow DOM boundaries, and events that do not bubble in the expected way.

# Key Points

- Distinguish `target` from `currentTarget`; delegation is not automatically faster in every case; accessibility still depends on semantic controls.
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

- Matching only `event.target` when nested elements can be clicked.

# Follow-up Questions

- How does shadow DOM change event retargeting?

# Related Questions

- Browse other [javascript questions](../javascript/).

# References

- [Javascript documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
