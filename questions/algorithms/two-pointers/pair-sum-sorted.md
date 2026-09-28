---
id: algorithms-two-pointers-pair-sum-001
title: "Find a target pair in a sorted sequence"
type: algorithm
domain: algorithms
category: two-pointers
difficulty: intermediate
problem_difficulty: easy
estimated_minutes: 25
problem_family: pair-search
data_structures:
  - array
patterns:
  - two-pointers
expected_time_complexity: "O(n)"
expected_space_complexity: "O(1)"
canonical_reference:
  platform: LeetCode
  name: "Two Sum II - Input Array Is Sorted"
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

Given a nondecreasing integer sequence and a target, return the indices of two distinct values whose sum is the target, or report that no pair exists. Assume at most one result is required.

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
+- Duplicates, negative values, minimal length, and no solution.
+
+# Expected Solution
+
+Compare the end values: a sum below target requires a larger left value; a sum above target requires a smaller right value. This safely eliminates one endpoint each step.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** O(n) under the stated assumptions.
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
+Consider the `two-pointers` pattern and name the invariant before coding.
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
+- How does the solution change for an unsorted sequence?
+
+# Related Questions
+
+- See the [two-pointers pattern directory](../two-pointers/).
+
+# References
+
+- Canonical name: “Two Sum II - Input Array Is Sorted” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
