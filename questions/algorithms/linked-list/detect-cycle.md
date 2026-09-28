---
id: algorithms-linked-list-cycle-001
title: "Detect a cycle in a linked structure"
type: algorithm
domain: algorithms
category: linked-list
difficulty: intermediate
problem_difficulty: easy
estimated_minutes: 25
problem_family: cycle-detection
data_structures:
  - linked-list
patterns:
  - fast-slow-pointers
expected_time_complexity: "O(n)"
expected_space_complexity: "O(1)"
canonical_reference:
  platform: LeetCode
  name: "Linked List Cycle"
  url: "https://leetcode.com/problemset/"
tags:
  - blind-75-style
  - linked-list
skills:
  - algorithm-design
  - complexity-analysis
status: review
---

# Prompt

Determine whether following `next` pointers from a head eventually revisits a node, using constant auxiliary space.

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
+- Empty list, self-cycle, two-node cycle, long acyclic prefix.
+
+# Expected Solution
+
+Move one pointer one step and another two. If a cycle exists they meet; if the fast pointer reaches an end, no cycle exists. The relative movement modulo cycle length explains correctness.
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
+Consider the `fast-slow-pointers` pattern and name the invariant before coding.
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
+- Find the node where the cycle begins.
+
+# Related Questions
+
+- See the [linked-list pattern directory](../linked-list/).
+
+# References
+
+- Canonical name: “Linked List Cycle” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
