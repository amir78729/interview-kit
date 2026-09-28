---
id: algorithms-backtracking-word-grid-001
title: "Find a word path in a character grid"
type: algorithm
domain: algorithms
category: backtracking
difficulty: intermediate
problem_difficulty: medium
estimated_minutes: 25
problem_family: path-search
data_structures:
  - grid
patterns:
  - DFS
  - backtracking
expected_time_complexity: "O(rows * columns * 4^L)"
expected_space_complexity: "O(L)"
canonical_reference:
  platform: LeetCode
  name: "Word Search"
  url: "https://leetcode.com/problemset/"
tags:
  - blind-75-style
  - backtracking
skills:
  - algorithm-design
  - complexity-analysis
status: review
---

# Prompt

Determine whether a word can be formed by orthogonally adjacent grid cells without reusing a cell within the same path.

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
+- Empty word/grid policy, one cell, repeated letters, restoration after success/failure.
+
+# Expected Solution
+
+Start DFS from matching cells, mark a cell for the current path, explore neighbors for the next symbol, then restore it on backtrack. Early frequency checks can reject impossible words.
+
+## Correctness
+
+State the invariant maintained by the data structure or search state and explain why each discarded alternative cannot contain a missed answer.
+
+## Complexity
+
+- **Time:** O(rows * columns * 4^L) under the stated assumptions.
+- **Space:** O(L); distinguish auxiliary storage from returned output.
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
+Consider the `DFS, backtracking` pattern and name the invariant before coding.
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
+- Find many dictionary words efficiently using a trie.
+
+# Related Questions
+
+- See the [backtracking pattern directory](../backtracking/).
+
+# References
+
+- Canonical name: “Word Search” on LeetCode. The prompt and explanation above are original and are not a reproduction of the platform statement or solution.
