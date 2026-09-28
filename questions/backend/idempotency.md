---
id: backend-distributed-idempotency-001
title: "Design idempotent request handling"
type: technical
domain: backend
category: distributed-systems
difficulty: senior
estimated_minutes: 15
environment: implementation-neutral
tags:
  - backend
  - idempotency
skills:
  - reliability-reasoning
  - tradeoff-analysis
status: review
---

# Prompt

Explain idempotency for retried write requests and design a practical idempotency-key flow.

# Expected Answer

The server associates a scoped key with request identity, parameters, processing state, and outcome. Atomic reservation prevents duplicate execution; compatible retries receive the recorded result. Define TTL, conflict behavior, crash recovery, and which side effects participate. Idempotency does not make arbitrary operations inherently safe.

# Key Points

+- State the required invariant and failure assumptions before selecting mechanisms.
+- Cover retries, concurrency, observability, and operational recovery where relevant.
+
# Hints
+
+## Hint 1
+
+What can happen when a process or network fails at each boundary?
+
+## Hint 2
+
+Name the invariant, then choose the smallest guarantee that preserves it.
+
+# Evaluation Criteria
+
+- **Strong evidence:** Correct model, failure analysis, coherent mechanism, and justified tradeoffs.
+- **Adequate evidence:** Correct core behavior with minor operational gaps.
+- **Partial evidence:** Recognizes terminology but misses a material failure or invariant.
+- **Insufficient evidence:** Cannot connect mechanism to correctness.
+
+# Common Mistakes
+
+- Treating a named technology as a guarantee without checking its configuration and failure semantics.
+
+# Follow-up Questions
+
+- How would you test this under concurrency and injected failures?
+
+# Related Questions
+
+- Browse [backend questions](./).
+
+# References
+
+- Add implementation-specific primary documentation for a concrete deployment.
