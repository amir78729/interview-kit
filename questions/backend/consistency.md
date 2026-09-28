---
id: backend-distributed-consistency-001
title: "Compare consistency models"
type: technical
domain: backend
category: distributed-systems
difficulty: senior
estimated_minutes: 15
environment: implementation-neutral
tags:
  - backend
  - consistency
skills:
  - reliability-reasoning
  - tradeoff-analysis
status: review
---

# Prompt

Compare strong consistency, eventual consistency, and client-visible consistency choices for a distributed product.

# Expected Answer

Consistency is a contract about observable ordering/visibility, not simply database branding. Stronger guarantees simplify some invariants but can cost latency/availability under failures; eventual systems need conflict, monotonic-read, read-your-writes, and stale-UX strategies as requirements demand.

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
