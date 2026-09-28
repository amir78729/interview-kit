---
id: algorithms-graph-course-order-001
title: "Find a valid dependency order"
type: algorithm
domain: algorithms
category: graph
difficulty: intermediate
problem_difficulty: medium
estimated_minutes: 25
problem_family: topological-order
data_structures:
  - directed-graph
  - queue
patterns:
  - topological-sort
expected_time_complexity: "O(V + E)"
expected_space_complexity: "O(V + E)"
canonical_reference:
  platform: LeetCode
  name: "Course Schedule II"
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

Given named tasks and prerequisite directed edges, return any ordering that places every prerequisite before its dependent task, or report a cycle.

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
+- Disconnected graph, duplicate edges policy, no edges, cycle.
+
+# Expected Solution
+
+Compute indegrees, enqueue zero-indegree tasks, and remove their outgoing edges conceptually. Processing fewer than all tasks proves a directed cycle. DFS color states are an alternative.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** O(V + E) under the stated assumptions.
+- **Space:** O(V + E); distinguish auxiliary storage from returned output.
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
+Consider the `topological-sort` pattern and name the invariant before coding.
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
+- Return one concrete cycle when no ordering exists.
+
+# Related Questions
+
+- See the [graph pattern directory](../graph/).
+
+# References
+
+- Canonical name: “Course Schedule II” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
