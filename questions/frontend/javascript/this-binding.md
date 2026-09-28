---
id: frontend-js-this-001
title: "Reason about JavaScript this binding"
type: technical
domain: frontend
category: javascript
difficulty: intermediate
estimated_minutes: 12
environment: modern standards-based web environments
tags:
  - javascript
  - this-binding
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain how `this` is selected for a function call and how arrow functions differ.

# Expected Answer

For ordinary functions, `this` depends on the call form: method receiver, explicit `call`/`apply`/`bind`, constructor invocation, or default binding (which differs by strict mode and environment). Arrow functions do not define their own `this`; they resolve it lexically. Extracting a method can therefore lose its receiver.

# Key Points

- Call site matters more than declaration site for ordinary functions; `bind` returns a bound function; arrows are unsuitable when a dynamic receiver is required.
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

- Saying `this` always means the object where a function was defined.

# Follow-up Questions

- Predict `this` after passing an object method as a callback.

# Related Questions

- Browse other [javascript questions](../javascript/).

# References

- [Javascript documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
