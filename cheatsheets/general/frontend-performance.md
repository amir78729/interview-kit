---
id: cheatsheet-frontend-performance-001
title: Frontend performance cheatsheet
type: cheatsheet
domain: frontend
category: performance
audience: interview candidates
tags: [performance, web-vitals]
status: review
---

# Diagnose by Category

| Category | Inspect |
| --- | --- |
| Network | TTFB, redirects, cache, compression, priority, waterfalls |
| JavaScript | bundle cost, parse/execute, long tasks, third parties |
| Rendering | style, layout, paint, compositing, DOM size |
| Images/fonts | dimensions, responsive sources, format, loading, shifts |
| Interaction | event work, scheduling, rendering, total INP attribution |

# User Metrics

LCP: loading of the principal content; INP: interaction responsiveness; CLS: unexpected visual instability. Definitions/thresholds evolve—verify current web.dev guidance. Segment field data; use lab traces to diagnose causes.

# Optimization Principles

- Set budgets and prioritize critical journeys.
- Stream/defer/lazy-load only with intentional UX and priority.
- Cache immutable versioned assets; treat personalized data carefully.
- Split long main-thread work and reduce unnecessary client code.
- Reserve dimensions and avoid layout shifts.
- Measure before and after on representative devices.
