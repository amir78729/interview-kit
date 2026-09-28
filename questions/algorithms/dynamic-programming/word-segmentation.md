---
id: algorithms-dp-word-break-001
title: "Determine whether a string can be segmented"
type: algorithm
domain: algorithms
category: dynamic-programming
difficulty: intermediate
problem_difficulty: medium
estimated_minutes: 25
problem_family: prefix-feasibility
data_structures:
  - set
  - array
patterns:
  - dynamic-programming
expected_time_complexity: "O(n^2) checks"
expected_space_complexity: "O(n)"
canonical_reference:
  platform: LeetCode
  name: "Word Break"
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

Given a string and a set of nonempty dictionary words, determine whether the entire string can be formed by concatenating dictionary entries, allowing reuse.

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
+- Empty string, overlapping words, unreachable suffix, Unicode slicing assumptions.
+
+# Expected Solution
+
+Let dp[i] mean the prefix ending before i is segmentable. It is true when some earlier reachable j has substring j..i in the set. Bound checks by maximum word length when useful.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** O(n^2) checks under the stated assumptions.
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
+Consider the `dynamic-programming` pattern and name the invariant before coding.
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
+- Return one valid segmentation or count segmentations.
+
+# Related Questions
+
+- See the [dynamic-programming pattern directory](../dynamic-programming/).
+
+# References
+
+- Canonical name: “Word Break” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
