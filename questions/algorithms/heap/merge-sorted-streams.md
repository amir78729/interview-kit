---
id: algorithms-heap-merge-sorted-001
title: "Merge several sorted sequences"
type: algorithm
domain: algorithms
category: heap
difficulty: intermediate
problem_difficulty: hard
estimated_minutes: 25
problem_family: multiway-merge
data_structures:
  - heap
patterns:
  - min-heap
expected_time_complexity: "O(N log k)"
expected_space_complexity: "O(k)"
canonical_reference:
  platform: LeetCode
  name: "Merge k Sorted Lists"
  url: "https://leetcode.com/problemset/"
tags:
  - blind-75-style
  - heap
skills:
  - algorithm-design
  - complexity-analysis
status: review
---

# Prompt

Merge k individually sorted sequences into one sorted result without repeatedly scanning every current head.

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
+- Empty sequences, duplicates, one sequence, stable tie policy.
+
+# Expected Solution
+
+Put each nonempty sequence’s current head and source position in a min-heap. Pop the least value, emit it, and push the next value from that source. Heap size is at most k.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** O(N log k) under the stated assumptions.
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
+Consider the `min-heap` pattern and name the invariant before coding.
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
+- Produce a lazy iterator instead of storing all output.
+
+# Related Questions
+
+- See the [heap pattern directory](../heap/).
+
+# References
+
+- Canonical name: “Merge k Sorted Lists” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
