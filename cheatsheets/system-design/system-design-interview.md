---
id: cheatsheet-system-design-interview-001
title: System design interview cheatsheet
type: cheatsheet
domain: system-design
category: architecture
audience: interview candidates
tags: [system-design, tradeoffs]
status: review
---

# Flow

1. Clarify users, journeys, scope, scale, and constraints.
2. State functional and measurable non-functional requirements.
3. Define contracts and primary data model.
4. Draw responsibilities and trace one read and one write.
5. Deep-dive critical state, cache, performance, reliability, and scale.
6. Cover security/privacy, accessibility, observability, testing, and rollout.
7. Summarize tradeoffs, risks, and evolution.

# Frontend Dimensions

Rendering/SSR boundaries, URL/local/server/offline state, request waterfalls, cache freshness, responsiveness, loading/failure UX, accessibility, bundle/asset budgets, telemetry privacy, browser/device compatibility.

# Backend Dimensions

Partitioning, replication, consistency, idempotency, queue semantics, backpressure, hot keys, capacity, failover, data migration, operational ownership.

# Tradeoff Frame

`Option → requirement optimized → cost/risk → evidence that changes the choice`

# Common Misses

- Technology before requirements.
- Happy path only.
- Undefined identity, ordering, pagination, retry, and authorization semantics.
- No measurement, rollout, or migration plan.
