---
id: algorithms-tree-lca-001
title: "Find a lowest shared ancestor"
type: algorithm
domain: algorithms
category: tree
difficulty: intermediate
problem_difficulty: medium
estimated_minutes: 25
problem_family: tree-relationships
data_structures:
  - binary-tree
patterns:
  - DFS
expected_time_complexity: "O(n)"
expected_space_complexity: "O(h)"
canonical_reference:
  platform: LeetCode
  name: "Lowest Common Ancestor of a Binary Tree"
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

Given a binary tree and two existing node identities, return their lowest node that is an ancestor of both; a node may be its own ancestor.

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
+- One target is ancestor, targets equal policy, skewed tree.
+
+# Expected Solution
+
+Postorder recursion returns a target or evidence from each side. If left and right both return evidence, the current node is the split point; otherwise propagate the nonempty side.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** O(n) under the stated assumptions.
+- **Space:** O(h); distinguish auxiliary storage from returned output.
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
+Consider the `DFS` pattern and name the invariant before coding.
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
+- How does a search-tree ordering change the solution?
+
+# Related Questions
+
+- See the [tree pattern directory](../tree/).
+
+# References
+
+- Canonical name: “Lowest Common Ancestor of a Binary Tree” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
