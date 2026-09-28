---
id: algorithms-graph-islands-001
title: "Count connected land regions"
type: algorithm
domain: algorithms
category: graph
difficulty: intermediate
problem_difficulty: medium
estimated_minutes: 25
problem_family: connected-components
data_structures:
  - grid
patterns:
  - DFS or BFS
expected_time_complexity: "O(rows * columns)"
expected_space_complexity: "O(rows * columns) worst case"
canonical_reference:
  platform: LeetCode
  name: "Number of Islands"
  url: "https://leetcode.com/problemset/"
tags:
  - blind-75-style
  - graph
skills:
  - algorithm-design
  - complexity-analysis
status: review
---

# Prompt

Given a rectangular grid of land and water cells, count groups of land connected orthogonally.

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
+- Empty grid, all one type, narrow grid, mutation versus visited set.
+
+# Expected Solution
+
+Scan every cell. When unvisited land is found, increment the count and traverse its entire component, marking nodes so no land cell starts another component.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** O(rows * columns) under the stated assumptions.
+- **Space:** O(rows * columns) worst case; distinguish auxiliary storage from returned output.
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
+Consider the `DFS or BFS` pattern and name the invariant before coding.
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
+- Count diagonal connections or return component sizes.
+
+# Related Questions
+
+- See the [graph pattern directory](../graph/).
+
+# References
+
+- Canonical name: “Number of Islands” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
