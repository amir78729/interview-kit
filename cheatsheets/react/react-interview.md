---
id: cheatsheet-react-interview-001
title: React interview cheatsheet
type: cheatsheet
domain: frontend
category: react
audience: interview candidates
tags: [react, components]
status: review
---

# Mental Model

- Render calculates UI; commit applies host changes. A render need not change DOM.
- State is a snapshot per render; setters request later work.
- State identity follows tree position, element type, and key.
- Render must be pure. Effects synchronize external systems after commit.

# Tool Choice

| Need | Prefer |
| --- | --- |
| Derived value | Calculate during render |
| User-triggered side effect | Event handler |
| External subscription/widget | Effect with cleanup |
| Previous-state update | Functional updater |
| Cross-cutting stable dependency | Context, scoped thoughtfully |
| Proven expensive recalculation | `useMemo` after profiling |

# Pitfalls

- Index/random keys in reorderable lists.
- Redundant state synchronized by effects.
- Mutation followed by setting the same object identity.
- Memoizing everything without measurement.
- Presenting framework-specific server/client behavior as universal React behavior.

# Performance Checklist

Profile representative production work; inspect state placement, expensive commits, effect loops, list size, request waterfalls, and browser layout/paint—not just render counts.

# Related Content

- [Rendering](../../questions/frontend/react/rendering.md)
- [Effects](../../questions/frontend/react/effects.md)
