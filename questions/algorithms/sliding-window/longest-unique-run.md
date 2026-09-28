---
id: algorithms-sliding-window-unique-001
title: "Longest substring without repeated symbols"
type: algorithm
domain: algorithms
category: sliding-window
difficulty: intermediate
problem_difficulty: medium
estimated_minutes: 25
problem_family: contiguous-window
data_structures:
  - hash-map
patterns:
  - sliding-window
expected_time_complexity: "O(n)"
expected_space_complexity: "O(k)"
canonical_reference:
  platform: LeetCode
  name: "Longest Substring Without Repeating Characters"
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

Given a string, return the length of its longest contiguous region containing no repeated character. State whether you interpret JavaScript UTF-16 code units or Unicode code points.

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
+- Empty input, repeated single symbol, Unicode interpretation, and repeat before the current window.
+
+# Expected Solution
+
+Maintain a left boundary and each symbol’s latest index. On a repeat inside the current window, move left just beyond the prior occurrence; never move left backward. Each position enters once.
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
+- Return the region itself and define tie-breaking.
+
+# Related Questions
+
+- See the [sliding-window pattern directory](../sliding-window/).
+
+# References
+
+- Canonical name: “Longest Substring Without Repeating Characters” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
