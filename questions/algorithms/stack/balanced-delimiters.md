---
id: algorithms-stack-delimiters-001
title: "Validate nested delimiters"
type: algorithm
domain: algorithms
category: stack
difficulty: intermediate
problem_difficulty: easy
estimated_minutes: 25
problem_family: parsing
data_structures:
  - stack
patterns:
  - stack
expected_time_complexity: "O(n)"
expected_space_complexity: "O(n)"
canonical_reference:
  platform: LeetCode
  name: "Valid Parentheses"
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

Given a sequence containing bracket characters, determine whether every closer matches the most recent unmatched opener and all openers are closed.

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
+- Empty input, starts with closer, odd length, crossing pairs.
+
+# Expected Solution
+
+Push openers. For a closer, the stack top must be its matching opener; reject otherwise. Accept only if the stack is empty at the end.
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
+Consider the `stack` pattern and name the invariant before coding.
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
+- How would you report the first error location?
+
+# Related Questions
+
+- See the [stack pattern directory](../stack/).
+
+# References
+
+- Canonical name: “Valid Parentheses” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
