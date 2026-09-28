---
id: cheatsheet-algorithms-patterns-001
title: Big-O and algorithm patterns cheatsheet
type: cheatsheet
domain: algorithms
category: algorithms
audience: interview candidates
tags: [big-o, patterns]
status: review
---

# Growth

| Bound | Typical example |
| --- | --- |
| `O(1)` | Hash lookup expected/amortized under assumptions |
| `O(log n)` | Binary search |
| `O(n)` | Single traversal |
| `O(n log n)` | Comparison sorting |
| `O(n²)` | All pairs |
| Exponential | Enumerating combinatorial choices |

State average/worst/amortized assumptions and include sorting, recursion depth, copied slices, and output size.

# Pattern Signals

- **Two pointers:** ordered elimination or ends of a sequence.
- **Sliding window:** contiguous region with incrementally maintained validity.
- **Monotonic stack/deque:** next greater/smaller or moving extrema.
- **BFS:** unweighted shortest edges/levels; **DFS:** components, structure, backtracking.
- **Heap:** repeatedly retrieve top priority among changing candidates.
- **Intervals:** sort by boundary, merge/sweep active ranges.
- **DP:** overlapping subproblems with a state and transition.
- **Backtracking:** enumerate choices with undo and pruning.

# Interview Checklist

Clarify constraints → baseline → invariant → implement → edge cases → complexity → variation.
