---
id: frontend-js-closures-001
title: "Explain closures in JavaScript"
type: technical
domain: frontend
category: javascript
difficulty: intermediate
estimated_minutes: 10
environment: modern standards-based web environments
tags:
  - javascript
  - closures
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Explain what a closure is, when it is created, and one useful and one risky use in production code.

# Expected Answer

A closure is a function together with access to the lexical environment in which it was created. The function can read bindings from outer scopes after that outer invocation has returned. Closures enable factories, encapsulated state, callbacks, and memoization. They can also retain reachable objects longer than intended; this is reachability, not an automatic memory leak.

# Key Points

- Lexical scope determines captured bindings; closures capture bindings rather than frozen value snapshots; each factory call can create an independent environment.
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

- Saying closures copy all outer values at declaration time, or that every closure inherently leaks memory.

# Follow-up Questions

- How does using `var` versus `let` in a loop affect callbacks?

# Related Questions

- Browse other [javascript questions](../javascript/).

# References

- [Javascript documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
