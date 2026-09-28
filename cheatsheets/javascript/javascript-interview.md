---
id: cheatsheet-javascript-interview-001
title: JavaScript interview cheatsheet
type: cheatsheet
domain: frontend
category: javascript
audience: interview candidates
tags: [javascript, interview]
status: review
---

# Execution and Types

| Topic | Reminder |
| --- | --- |
| Scope | Lexical; `let`/`const` are block-scoped, `var` is function-scoped |
| Closure | Function plus access to its lexical environment; bindings are live |
| `this` | Ordinary function: call-site rules. Arrow: lexical `this` |
| Equality | Prefer explicit normalization + `===`; know `NaN` and signed-zero edge cases |
| Objects | Compared by identity; property lookup follows the prototype chain |

# Asynchrony

- Current JavaScript job runs to completion.
- Promise reactions and `queueMicrotask` use microtasks; a checkpoint drains them before a later task.
- Timer delay is a minimum threshold, not a schedule guarantee.
- `await` pauses one async function; start independent work before awaiting together.
- Return inner promises; handle rejection and cancellation deliberately.

# Common Pitfalls

- Calling “hoisting” source-code movement; it summarizes declaration instantiation behavior.
- Forgetting that `const` protects a binding, not nested object mutation.
- Assuming circular references inherently leak; continued reachability is the issue.
- Using `forEach` when awaiting each callback is expected to sequence/control completion.

# Interview Reminders

Predict output by listing synchronous work, queued jobs, and binding/call-site rules. State browser versus Node.js assumptions where scheduling differs.

# Related Content

- [Event loop question](../../questions/frontend/javascript/event-loop.md)
- [Closures question](../../questions/frontend/javascript/closures.md)
