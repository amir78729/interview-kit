---
id: backend-performance-caching-001
title: "Design a cache safely"
type: technical
domain: backend
category: distributed-systems
difficulty: senior
estimated_minutes: 15
environment: implementation-neutral
tags:
  - backend
  - caching
skills:
  - reliability-reasoning
  - tradeoff-analysis
status: review
---

# Prompt

Describe cache-aside behavior, invalidation, stampede prevention, and correctness risks.

# Expected Answer

Cache-aside reads cache then source and populates misses; writes need an explicit invalidation/update sequence. TTL bounds staleness but is not correctness. Use request coalescing, jitter, admission/size policy, versioned keys, and negative caching carefully. Never share authorization-sensitive results under unsafe keys.

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
