---
id: algorithms-backtracking-combination-001
title: "Enumerate combinations reaching a target"
type: algorithm
domain: algorithms
category: backtracking
difficulty: intermediate
problem_difficulty: medium
estimated_minutes: 25
problem_family: combinatorial-search
data_structures:
  - array
patterns:
  - backtracking
expected_time_complexity: "output-sensitive"
expected_space_complexity: "O(target depth) excluding output"
canonical_reference:
  platform: LeetCode
  name: "Combination Sum"
  url: "https://leetcode.com/problemset/"
tags:
  - blind-75-style
  - backtracking
skills:
  - algorithm-design
  - complexity-analysis
status: review
---

# Prompt

Given distinct positive candidate values and a target, return combinations whose sum is the target; a candidate may be reused and combination order does not distinguish results.

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
+- Target zero policy, candidate above target, no solution, nonpositive candidates must be excluded or handled differently.
+
+# Expected Solution
+
+Sort candidates and recurse from a start index. Choose a candidate, reduce the remainder, and recurse with the same index for reuse. Stop branches once values exceed the remainder. Start index avoids permutations.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** output-sensitive under the stated assumptions.
+- **Space:** O(target depth) excluding output; distinguish auxiliary storage from returned output.
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
+Consider the `backtracking` pattern and name the invariant before coding.
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
+- Allow each candidate at most once when input may contain duplicates.
+
+# Related Questions
+
+- See the [backtracking pattern directory](../backtracking/).
+
+# References
+
+- Canonical name: “Combination Sum” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
