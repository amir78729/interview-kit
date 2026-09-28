---
id: algorithms-dp-house-robber-001
title: "Maximum sum without adjacent choices"
type: algorithm
domain: algorithms
category: dynamic-programming
difficulty: intermediate
problem_difficulty: medium
estimated_minutes: 25
problem_family: sequence-optimization
data_structures:
  - array
patterns:
  - dynamic-programming
expected_time_complexity: "O(n)"
expected_space_complexity: "O(1)"
canonical_reference:
  platform: LeetCode
  name: "House Robber"
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

Given nonnegative rewards in a line, choose a subset with no adjacent positions and maximize total reward.

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
+- Empty, one/two items, all zeros.
+
+# Expected Solution
+
+At each position choose between skipping it (previous optimum) and taking it (reward plus optimum two positions back). Only two prior states are needed. State and justify behavior for empty input.
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
+- What changes when first and last positions are adjacent in a circle?
+
+# Related Questions
+
+- See the [dynamic-programming pattern directory](../dynamic-programming/).
+
+# References
+
+- Canonical name: “House Robber” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
