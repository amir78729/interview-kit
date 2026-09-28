---
id: algorithms-stack-next-greater-001
title: "Distance to the next warmer reading"
type: algorithm
domain: algorithms
category: stack
difficulty: intermediate
problem_difficulty: medium
estimated_minutes: 25
problem_family: next-greater-element
data_structures:
  - stack
patterns:
  - monotonic-stack
expected_time_complexity: "O(n)"
expected_space_complexity: "O(n)"
canonical_reference:
  platform: LeetCode
  name: "Daily Temperatures"
  url: "https://leetcode.com/problemset/"
tags:
  - blind-75-style
  - stack
skills:
  - algorithm-design
  - complexity-analysis
status: review
---

# Prompt

For each daily measurement, return how many positions ahead the next strictly greater measurement occurs, or zero if none does.

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
+- Equal readings, decreasing sequence, one item.
+
+# Expected Solution
+
+Keep indices whose answer is unresolved in a decreasing stack. A greater new value resolves and pops all smaller tops. Each index is pushed and popped at most once.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** O(n) under the stated assumptions.
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
+Consider the `monotonic-stack` pattern and name the invariant before coding.
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
+- Solve while streaming if past answers may be emitted later.
+
+# Related Questions
+
+- See the [stack pattern directory](../stack/).
+
+# References
+
+- Canonical name: “Daily Temperatures” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
