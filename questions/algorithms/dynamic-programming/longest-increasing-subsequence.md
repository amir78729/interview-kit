---
id: algorithms-dp-lis-001
title: "Length of a longest increasing subsequence"
type: algorithm
domain: algorithms
category: dynamic-programming
difficulty: intermediate
problem_difficulty: hard
estimated_minutes: 25
problem_family: subsequence-optimization
data_structures:
  - array
patterns:
  - dynamic-programming
  - binary-search
expected_time_complexity: "O(n log n)"
expected_space_complexity: "O(n)"
canonical_reference:
  platform: LeetCode
  name: "Longest Increasing Subsequence"
  url: "https://leetcode.com/problemset/"
tags:
  - blind-75-style
  - dynamic-programming
skills:
  - algorithm-design
  - complexity-analysis
status: review
---

# Prompt

Return the length of a longest strictly increasing subsequence; selected values keep their original order but need not be contiguous.

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
+- Empty, duplicates, decreasing input, strict versus nondecreasing.
+
+# Expected Solution
+
+Maintain the smallest possible tail for an increasing subsequence of each length. Binary-search the first tail not less than each value and replace it. Tail entries support length computation but are not necessarily one actual subsequence.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** O(n log n) under the stated assumptions.
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
+Consider the `dynamic-programming, binary-search` pattern and name the invariant before coding.
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
+- Reconstruct an actual subsequence.
+
+# Related Questions
+
+- See the [dynamic-programming pattern directory](../dynamic-programming/).
+
+# References
+
+- Canonical name: “Longest Increasing Subsequence” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
