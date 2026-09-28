---
id: frontend-js-modules-001
title: "Compare JavaScript modules and classic scripts"
type: technical
domain: frontend
category: javascript
difficulty: intermediate
estimated_minutes: 10
environment: modern standards-based web environments
tags:
  - javascript
  - modules
skills:
  - conceptual-reasoning
  - practical-application
status: review
---

# Prompt

Compare browser ECMAScript modules with classic scripts in loading, scope, and dependency behavior.

# Expected Answer

Modules have their own top-level scope, are strict by default, support static imports/exports, and are deferred by default in browsers. Their dependency graph is fetched and evaluated according to module semantics, with live imported bindings. Dynamic `import()` loads asynchronously. Classic scripts have different global and loading behavior.

# Key Points

- Imports are live read-only views for importers; module URLs participate in identity/caching; cycles require care around initialization.
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

- Calling imports copied values or assuming module execution order is simply textual across files.

# Follow-up Questions

- What problems can circular module dependencies create?

# Related Questions

- Browse other [javascript questions](../javascript/).

# References

- [Javascript documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
