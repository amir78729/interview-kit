---
id: algorithms-binary-search-rotated-001
title: "Search a rotated sorted sequence"
type: algorithm
domain: algorithms
category: binary-search
difficulty: intermediate
problem_difficulty: medium
estimated_minutes: 25
problem_family: ordered-search
data_structures:
  - array
patterns:
  - binary-search
expected_time_complexity: "O(log n)"
expected_space_complexity: "O(1)"
canonical_reference:
  platform: LeetCode
  name: "Search in Rotated Sorted Array"
  url: "https://leetcode.com/problemset/"
tags:
  - blind-75-style
  - binary-search
skills:
  - algorithm-design
  - complexity-analysis
status: review
---

# Prompt

A strictly increasing array was rotated at an unknown boundary. Return the index of a target value or -1. Values are distinct.

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
+- No rotation, one item, target at pivot, absent target.
+
+# Expected Solution
+
+At least one side around the midpoint is normally ordered. Decide whether the target falls inside that side; retain it or discard it. Each decision halves the candidate range.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** O(log n) under the stated assumptions.
+- **Space:** O(1); distinguish auxiliary storage from returned output.
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
+Consider the `binary-search` pattern and name the invariant before coding.
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
+- What changes when duplicate values are allowed?
+
+# Related Questions
+
+- See the [binary-search pattern directory](../binary-search/).
+
+# References
+
+- Canonical name: “Search in Rotated Sorted Array” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
