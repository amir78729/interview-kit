---
id: algorithms-tree-level-order-001
title: "Traverse a tree by depth"
type: algorithm
domain: algorithms
category: tree
difficulty: intermediate
problem_difficulty: medium
estimated_minutes: 25
problem_family: tree-traversal
data_structures:
  - binary-tree
  - queue
patterns:
  - BFS
expected_time_complexity: "O(n)"
expected_space_complexity: "O(w)"
canonical_reference:
  platform: LeetCode
  name: "Binary Tree Level Order Traversal"
  url: "https://leetcode.com/problemset/"
tags:
  - blind-75-style
  - tree
skills:
  - algorithm-design
  - complexity-analysis
status: review
---

# Prompt

Return binary-tree values grouped from root depth downward and left to right within each level.

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
+- Empty tree, one node, wide tree.
+
+# Expected Solution
+
+Use a queue and process its current size as one level before appending newly discovered children. Each node is enqueued once.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** O(n) under the stated assumptions.
+- **Space:** O(w); distinguish auxiliary storage from returned output.
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
+Consider the `BFS` pattern and name the invariant before coding.
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
+- Return alternating left-to-right and right-to-left levels.
+
+# Related Questions
+
+- See the [tree pattern directory](../tree/).
+
+# References
+
+- Canonical name: “Binary Tree Level Order Traversal” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
