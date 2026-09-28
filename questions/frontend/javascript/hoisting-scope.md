---
id: frontend-js-hoisting-scope-001
title: "Explain hoisting and scope initialization"
type: technical
domain: frontend
category: javascript
difficulty: intermediate
estimated_minutes: 10
environment: modern standards-based web environments
tags:
  - javascript
  - hoisting-scope
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain what developers call hoisting for function declarations, `var`, `let`, and `const`.

# Expected Answer

Before execution, declarations create bindings during environment setup. Function declarations are initialized to functions; `var` bindings are initialized to `undefined`; lexical bindings for `let`, `const`, and classes exist but cannot be accessed before initialization—the temporal dead zone. “Hoisting” is shorthand, not a specification operation that moves source text.

# Key Points

- Block versus function scope matters; TDZ begins at scope entry; `const` prevents rebinding, not object mutation.
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

- Saying `let` is not hoisted at all or that declarations are physically moved.

# Follow-up Questions

- How do modules change top-level scope and strictness?

# Related Questions

- Browse other [javascript questions](../javascript/).

# References

- [Javascript documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
