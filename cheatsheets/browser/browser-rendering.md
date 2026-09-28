---
id: cheatsheet-browser-rendering-001
title: Browser rendering cheatsheet
type: cheatsheet
domain: frontend
category: browser
audience: interview candidates
tags: [browser, rendering, performance]
status: review
---

# Typical Work

`bytes → parse DOM/CSSOM → computed style → layout → paint → composite`

This is a useful model, not a guaranteed rigid one-pass implementation. Browsers batch, cache, invalidate, and optimize.

| Change | Often affects | Caveat |
| --- | --- | --- |
| Geometry/content | style, layout, paint | Scope depends on containment/tree |
| Color/background | style, paint | May affect large painted area |
| Transform/opacity | compositing | Promotion is implementation-dependent and consumes resources |

# Avoid Forced Synchronization

Batch reads, then writes. Alternating DOM writes with geometry reads can repeatedly flush pending style/layout.

# Diagnose

- Use a performance trace with a specific interaction.
- Inspect long tasks, recalculation, layout, paint, and layer memory.
- Connect lab traces to field LCP, INP, and CLS where available.

# Pitfalls

- “Use `will-change` everywhere.”
- “Every DOM change reflows the whole page.”
- Equating `DOMContentLoaded` with usable.

# Related Content

- [Rendering pipeline question](../../questions/frontend/browser/rendering-pipeline.md)
