# Declarative interview engine

The “engine” is a documented protocol interpreted by a human or AI. There is no application runtime. A definition selects content and behavior; a private session records one execution.

## Starting a session

1. Resolve the requested domain, level, duration, and focus against `interviews/`. Ask only for missing essentials.
2. Read the selected definition and verify referenced question IDs.
3. Query a reliable local system clock. Record `started_at` in ISO 8601 with local offset, preserve the timezone, and calculate `expected_end_at` from `duration_minutes`.
4. Create a private session from `templates/interview-session.md` when filesystem writes are allowed. If not, keep transient context and offer a private record afterward.
5. Explain format briefly, then ask one primary question at a time. Do not expose answers or internal rubric details.

If a reliable clock is unavailable, state that timing cannot be verified. Never invent a timestamp or remaining-time claim.

## Timing model

At each phase boundary—and before asserting time remaining—read the clock and calculate:

```text
elapsed = now - started_at
remaining = expected_end_at - now
```

Do not estimate from turns or message count. A typical 60-minute flow is 0–5 calibration, 5–20 initial technical work, 20–40 core depth, 40–52 design/deeper work, 52–57 follow-ups, and 57–60 candidate questions and close. The interview definition overrides this example.

When behind schedule, preserve mandatory competency coverage, shorten follow-ups, skip optional items, and reserve closing time. When ten minutes remain, do not start a task that cannot reasonably finish. Inform the candidate at natural transitions. Being ahead permits optional depth, not arbitrary extra grading dimensions.

## Interaction

- Ask one primary question and allow silence/reasoning.
- Clarify ambiguity without solving the problem.
- Give hints only on request or when the definition permits; advance one hint at a time.
- Ask follow-ups based on the candidate's actual answer.
- Record evidence, not inferred intentions or fabricated quotations.
- Distinguish technical correctness, reasoning, and communication.
- Teaching mode is separate and begins only by request.

## Evaluation

Default dimensions include correctness, depth, reasoning, problem solving, communication, and tradeoff analysis. Add system thinking, performance, security, accessibility, observability, and testing only where relevant. Rate evidence qualitatively: `strong evidence`, `adequate evidence`, `partial evidence`, or `insufficient evidence`. “Insufficient” means not demonstrated, not necessarily incapable. Numeric scoring is valid only when the definition declares a scale and anchors.

At close, summarize observed strengths, gaps, review topics, concrete next actions, and limitations in the evidence. Store personal results only under `.personal/`.
