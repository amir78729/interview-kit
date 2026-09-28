---
id: system-design-backend-jobs-001
title: "Design a reliable background job system"
type: system-design
domain: backend
category: architecture
difficulty: senior
estimated_minutes: 45
scope: backend-led with explicit adjacent-system contracts
dimensions:
  - requirements
  - api-contracts
  - data-contracts
  - data-model
  - performance
  - reliability
  - scalability
  - security
  - observability
  - testing
  - tradeoffs
tags:
  - system-design
  - job-processing
skills:
  - requirements-clarification
  - architecture
  - tradeoff-analysis
status: review
---

# Prompt

Design asynchronous job execution for multiple workloads with retries, scheduling, prioritization, and operational visibility. Lead the design from the backend perspective, but make dependencies and service contracts explicit. Clarify scale and priorities rather than assuming them.

# Clarifying Questions

+- Who are the users, critical journeys, devices/regions, and accessibility needs?
+- What scale, latency, freshness, consistency, availability, privacy, and regulatory constraints matter?
+- Which capabilities are required for the first release, and what can degrade or wait?
+
# Functional Requirements

+- Define core user journeys, states, and administrative/operational workflows.
+- Define failure, empty, loading, permission, and recovery behavior.
+
# Non-functional Requirements

+- Establish measurable performance, reliability, accessibility, security, scalability, and maintainability targets.
+- Identify data sensitivity and retention expectations.
+
# Expected Discussion

+## User Experience
+
+Map primary journeys and make slow, stale, partial, and failed states understandable. Preserve keyboard, screen-reader, localization, and responsive behavior where applicable.
+
+## API and Data Contracts
+
+Define resource/event shape, identity, pagination or streaming semantics, versioning, errors, idempotency, authorization, and evolution. Avoid coupling presentation directly to unstable service internals.
+
+## State and Data Flow
+
+Separate authoritative remote data, cached data, local interaction state, URL/shareable state, and durable offline state. Explain consistency and conflict policy.
+
+## Architecture
+
+Draw responsibilities, boundaries, critical data flow, deployment/runtime assumptions, and incremental evolution. Focus areas include: queue semantics; idempotency; leasing; retry/backoff; dead letters; partitioning; fairness; observability.
+
+## Caching and Performance
+
+Set budgets, choose cache keys/freshness/invalidation, control payload and work, and measure user-visible bottlenecks. Explain hot-path behavior.
+
+## Reliability and Scalability
+
+Cover retries, deduplication, ordering, backpressure, partial failure, recovery, capacity, and graceful degradation as relevant.
+
+## Security and Privacy
+
+Enforce authorization at trusted boundaries, validate input, minimize exposed/collected data, and threat-model cross-origin, injection, abuse, and dependency risks.
+
+## Accessibility
+
+Use semantic interaction, focus/announcement strategy, contrast/motion considerations, and assistive-technology testing for user interfaces.
+
+## Observability
+
+Define privacy-conscious metrics, logs, traces, release context, service-level indicators, alert ownership, and debugging paths.
+
+## Testing
+
+Cover pure logic, components/services, contracts, failure injection, performance, accessibility, end-to-end journeys, and staged rollout.
+
+## Tradeoffs
+
+Compare at least two viable options against clarified priorities and identify what evidence would trigger a redesign.
+
+# Hints
+
+## Hint 1
+
+Start with users, scale, and the failure experience before naming technologies.
+
+## Hint 2
+
+Trace one read path and one write path end to end, then revisit reliability and observability.
+
+# Evaluation Criteria
+
+- **Strong evidence:** Drives clarification, proposes a coherent evolvable design, covers all relevant dimensions, quantifies priorities, and explains tradeoffs/failures.
+- **Adequate evidence:** Sound architecture and major concerns with a few depth gaps.
+- **Partial evidence:** Useful components but weak contracts, requirements, or failure reasoning.
+- **Insufficient evidence:** Technology list without coherent flows, priorities, or tradeoffs.
+
+# Common Mistakes
+
+- Choosing technology before requirements or treating adjacent services as magic.
+- Ignoring degraded states, accessibility, privacy, migration, and operational ownership.
+
+# Follow-up Questions
+
+- What fails first at ten times the expected load, and how would you know?
+- Which decision is hardest to reverse, and how would you reduce that risk?
+
+# Related Questions
+
+- Browse [backend system-design questions](./).
+
+# References
+
+- Add context-specific primary references when converting this review draft to published status.
