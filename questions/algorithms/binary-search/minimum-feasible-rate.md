---
id: algorithms-binary-search-answer-001
title: "Find the minimum feasible processing rate"
type: algorithm
domain: algorithms
category: binary-search
difficulty: intermediate
problem_difficulty: medium
estimated_minutes: 25
problem_family: optimization
data_structures:
  - array
patterns:
  - binary-search on answer
expected_time_complexity: "O(n log M)"
expected_space_complexity: "O(1)"
canonical_reference:
  platform: LeetCode
  name: "Koko Eating Bananas"
  url: "https://leetcode.com/problemset/"
tags:
  - blind-75-style
  - binary-search
skills:
  - algorithm-design
  - complexity-analysis
status: review
---

# Prompt

Given positive job sizes and a fixed number of whole time units, find the smallest integer rate that finishes all jobs when one job can be processed per unit and partial work rounds up.

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
+- One job, abundant time, overflow in summed time, and impossible-policy assumptions.
+
+# Expected Solution
+
+Feasibility is monotonic: if a rate works, every greater rate works. Binary-search the bounded rate space and use ceiling division to test total time.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** O(n log M) under the stated assumptions.
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
+Consider the `binary-search on answer` pattern and name the invariant before coding.
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
+- Which optimization problems cannot use binary search on the answer?
+
+# Related Questions
+
+- See the [binary-search pattern directory](../binary-search/).
+
+# References
+
+- Canonical name: “Koko Eating Bananas” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
