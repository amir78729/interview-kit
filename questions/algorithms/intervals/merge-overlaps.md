---
id: algorithms-intervals-merge-001
title: "Merge overlapping intervals"
type: algorithm
domain: algorithms
category: intervals
difficulty: intermediate
problem_difficulty: medium
estimated_minutes: 25
problem_family: interval-normalization
data_structures:
  - array
patterns:
  - sorting
  - intervals
expected_time_complexity: "O(n log n)"
expected_space_complexity: "O(n) output"
canonical_reference:
  platform: LeetCode
  name: "Merge Intervals"
  url: "https://leetcode.com/problemset/"
tags:
  - blind-75-style
  - intervals
skills:
  - algorithm-design
  - complexity-analysis
status: review
---

# Prompt

Given closed intervals, combine all overlaps and return nonoverlapping intervals sorted by start.

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
+- Empty input, contained intervals, touching endpoints, reversed endpoint policy.
+
+# Expected Solution
+
+Sort by start. Compare each interval with the last merged interval: extend its end on overlap; otherwise append a new interval. Define endpoint semantics before using `<=`.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** O(n log n) under the stated assumptions.
+- **Space:** O(n) output; distinguish auxiliary storage from returned output.
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
+Consider the `sorting, intervals` pattern and name the invariant before coding.
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
+- Insert one interval into an already normalized list.
+
+# Related Questions
+
+- See the [intervals pattern directory](../intervals/).
+
+# References
+
+- Canonical name: “Merge Intervals” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
