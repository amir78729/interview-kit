---
id: algorithms-sliding-window-minimum-cover-001
title: "Smallest window covering required symbols"
type: algorithm
domain: algorithms
category: sliding-window
difficulty: intermediate
problem_difficulty: hard
estimated_minutes: 25
problem_family: minimum-cover
data_structures:
  - hash-map
patterns:
  - sliding-window
expected_time_complexity: "O(n + m)"
expected_space_complexity: "O(k)"
canonical_reference:
  platform: LeetCode
  name: "Minimum Window Substring"
  url: "https://leetcode.com/problemset/"
tags:
  - blind-75-style
  - sliding-window
skills:
  - algorithm-design
  - complexity-analysis
status: review
---

# Prompt

Given a source string and a requirement string, find the shortest source substring whose symbol counts cover all required counts. Return an empty result if impossible.

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
+- Repeated required symbols, impossible cover, empty requirement policy, and ties.
+
+# Expected Solution
+
+Expand until all required multiplicities are satisfied, then shrink while valid and record the best. Track how many distinct requirements are fully met so validity is O(1) per movement.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** O(n + m) under the stated assumptions.
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
+Consider the `sliding-window` pattern and name the invariant before coding.
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
+- Adapt the method to token sequences rather than strings.
+
+# Related Questions
+
+- See the [sliding-window pattern directory](../sliding-window/).
+
+# References
+
+- Canonical name: “Minimum Window Substring” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
