---
id: cheatsheet-typescript-interview-001
title: TypeScript interview cheatsheet
type: cheatsheet
domain: frontend
category: typescript
audience: interview candidates
tags: [typescript, types]
status: review
---

# Core Relationships

- Structural typing checks shape, not declared name.
- `unknown` requires narrowing; `any` opts out of safety.
- Union: one of several types; use only currently safe operations.
- Intersection: satisfies all requirements; conflicting members may be impossible.
- Generics preserve relationships; avoid a type parameter used only once.

# Narrowing

Use `typeof`, equality, discriminants, `in`, `instanceof`, predicates, and control flow. Validate unknown runtime input; an assertion does not parse data.

# Utilities

| Utility | Purpose | Reminder |
| --- | --- | --- |
| `Pick` / `Omit` | Select/remove keys | Domain input models may deserve explicit types |
| `Partial` / `Required` | Change optionality | Shallow only |
| `Record` | Key-to-value mapping | Runtime keys still need validation |
| `Exclude` / `Extract` | Filter unions | Conditional-type behavior |

# Inference

`as const` preserves literals/read-only shape; `satisfies` checks a target while retaining useful inferred detail. Annotate public boundaries where clarity outweighs inference.

# Pitfalls

- Treating types as runtime validation.
- Casting instead of proving.
- Deep utility types that erase domain update semantics.
