---
id: algorithms-heap-top-frequent-001
title: "Return the most frequent values"
type: algorithm
domain: algorithms
category: heap
difficulty: intermediate
problem_difficulty: medium
estimated_minutes: 25
problem_family: frequency-ranking
data_structures:
  - hash-map
  - heap
patterns:
  - frequency-map
  - heap
expected_time_complexity: "O(n log k)"
expected_space_complexity: "O(n)"
canonical_reference:
  platform: LeetCode
  name: "Top K Frequent Elements"
  url: "https://leetcode.com/problemset/"
tags:
  - blind-75-style
  - heap
skills:
  - algorithm-design
  - complexity-analysis
status: review
---

# Prompt

Given values and k, return any ordering of the k values with highest frequencies. Define tie behavior if deterministic output is required.

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
+- k equals distinct count, tied frequencies, empty input policy.
+
+# Expected Solution
+
+Count frequencies, then maintain a min-heap of at most k entries, evicting lower priorities. Bucket grouping can achieve linear time when memory and frequency bounds suit it.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** O(n log k) under the stated assumptions.
+- **Space:** O(n); distinguish auxiliary storage from returned output.
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
+Consider the `frequency-map, heap` pattern and name the invariant before coding.
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
+- Handle an unbounded stream approximately.
+
+# Related Questions
+
+- See the [heap pattern directory](../heap/).
+
+# References
+
+- Canonical name: “Top K Frequent Elements” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
