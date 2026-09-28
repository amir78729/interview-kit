---
id: algorithms-queue-window-maximum-001
title: "Maximum value in each fixed window"
type: algorithm
domain: algorithms
category: queue
difficulty: intermediate
problem_difficulty: hard
estimated_minutes: 25
problem_family: window-aggregate
data_structures:
  - deque
patterns:
  - monotonic-deque
expected_time_complexity: "O(n)"
expected_space_complexity: "O(k)"
canonical_reference:
  platform: LeetCode
  name: "Sliding Window Maximum"
  url: "https://leetcode.com/problemset/"
tags:
  - blind-75-style
  - queue
skills:
  - algorithm-design
  - complexity-analysis
status: review
---

# Prompt

Given numbers and a positive window width, return the maximum for every contiguous window of that width.

# Constraints

+- Inputs fit in memory unless the follow-up changes the model.
+- Clarify mutation, malformed-input behavior, and output ordering before coding.
+
+# Example
+
+Create a small example during the interview and trace the invariant rather than relying on memorized cases.
+
+# Edge Cases
+
+- Width one, width equals length, duplicate maxima, invalid width policy.
+
+# Expected Solution
+
+Maintain candidate indices in decreasing value order. Remove expired front indices and dominated back indices; the front is the maximum. Each index enters and leaves once.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** O(n) under the stated assumptions.
+- **Space:** O(k); distinguish auxiliary storage from returned output.
+
+# Alternative Solutions
+
+- Discuss the straightforward exhaustive or sorting-based baseline and why its tradeoff differs from the expected approach.
+
+# Hints
+
+## Hint 1
+
+Identify what repeated work or impossible candidates can be eliminated.
+
+## Hint 2
+
+Consider the `monotonic-deque` pattern and name the invariant before coding.
+
+# Evaluation Criteria
+
+- **Strong evidence:** Derives a correct invariant, implements it coherently, handles edge cases, and justifies complexity.
+- **Adequate evidence:** Correct main approach and bounds with only minor omissions.
+- **Partial evidence:** Finds a plausible pattern but has a correctness or complexity gap.
+- **Insufficient evidence:** Cannot produce a correct baseline or reason about progress.
+
+# Common Mistakes
+
+- Applying a memorized pattern without proving that its movement/state transitions are safe.
+- Stating complexity without accounting for sorting, recursion, heap operations, or output size.
+
+# Follow-up Variations
+
+- Maintain both minimum and maximum.
+
+# Related Questions
+
+- See the [queue pattern directory](../queue/).
+
+# References
+
+- Canonical name: “Sliding Window Maximum” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
