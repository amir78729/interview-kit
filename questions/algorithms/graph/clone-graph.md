---
id: algorithms-graph-clone-001
title: "Clone a connected object graph"
type: algorithm
domain: algorithms
category: graph
difficulty: intermediate
problem_difficulty: medium
estimated_minutes: 25
problem_family: graph-copy
data_structures:
  - graph
  - hash-map
patterns:
  - DFS or BFS
expected_time_complexity: "O(V + E)"
expected_space_complexity: "O(V)"
canonical_reference:
  platform: LeetCode
  name: "Clone Graph"
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

Given a reference to a node in a connected graph, create a deep copy preserving labels and adjacency without reusing original nodes.

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
+- Null reference, self-loop, duplicate labels, parallel-edge policy.
+
+# Expected Solution
+
+Map each original identity to its clone before traversing neighbors. Reuse that mapping when cycles or shared neighbors are encountered.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** O(V + E) under the stated assumptions.
+- **Space:** O(V); distinguish auxiliary storage from returned output.
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
+- Clone a disconnected graph supplied as a node collection.
+
+# Related Questions
+
+- See the [graph pattern directory](../graph/).
+
+# References
+
+- Canonical name: “Clone Graph” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
