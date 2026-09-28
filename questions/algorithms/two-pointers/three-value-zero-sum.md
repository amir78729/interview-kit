---
id: algorithms-two-pointers-three-sum-001
title: "Find unique zero-sum triples"
type: algorithm
domain: algorithms
category: two-pointers
difficulty: intermediate
problem_difficulty: medium
estimated_minutes: 25
problem_family: combination-search
data_structures:
  - array
patterns:
  - sorting
  - two-pointers
expected_time_complexity: "O(n^2)"
expected_space_complexity: "O(1) excluding output"
canonical_reference:
  platform: LeetCode
  name: "3Sum"
  url: "https://leetcode.com/problemset/"
tags:
  - blind-75-style
  - two-pointers
skills:
  - algorithm-design
  - complexity-analysis
status: review
---

# Prompt

Given integers, return every distinct value triple whose sum is zero. Do not return duplicate triples.

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
+- All zeros, many duplicates, fewer than three items, and no triples.
+
+# Expected Solution
+
+Sort first. Fix one value, skip repeated fixed values, and sweep the remainder with two pointers. After a match, move past duplicate endpoint values. Sorting makes movement monotonic and deduplication explicit.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** O(n^2) under the stated assumptions.
+- **Space:** O(1) excluding output; distinguish auxiliary storage from returned output.
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
+Consider the `sorting, two-pointers` pattern and name the invariant before coding.
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
+- How would you find triples for an arbitrary target?
+
+# Related Questions
+
+- See the [two-pointers pattern directory](../two-pointers/).
+
+# References
+
+- Canonical name: “3Sum” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
