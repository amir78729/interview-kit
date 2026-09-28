# Content model

YAML frontmatter is the machine-readable contract; the body is the human-readable content. The templates are normative examples. Use lower-case kebab-case values and two-space YAML indentation.

## Identity and lifecycle

Every reusable item has a globally unique stable `id`, descriptive `title`, `type`, `domain`, category/tags as appropriate, and `status` of `draft`, `review`, `published`, or `deprecated`. Do not change an ID when wording or file location changes. Deprecated content adds a reason and replacement ID/link where possible.

Question IDs conventionally follow `<domain>-<category>-<concept>-<sequence>`, such as `frontend-js-event-loop-001`. Interview IDs should convey domain, level, and duration, such as `frontend-intermediate-60`. Uniqueness matters more than a rigid prefix.

## Base question

Required frontmatter:

```yaml
id: frontend-js-event-loop-001
title: Explain the JavaScript event loop
type: technical
domain: frontend
category: javascript
difficulty: intermediate
estimated_minutes: 10
tags:
  - javascript
  - asynchronous-programming
skills:
  - runtime-model
  - reasoning
status: published
```

Required body concepts are Prompt, Expected Answer, Key Points, Hints, Evaluation Criteria, Common Mistakes, Follow-up Questions, Related Questions, and References when applicable. Related questions use stable IDs and preferably relative links.

## Specialized questions

- **Algorithm:** `problem_family`, `problem_difficulty`, `data_structures`, `patterns`, `expected_time_complexity`, and `expected_space_complexity`; body includes Constraints, Edge Cases, Solution, Alternatives, and Variations.
- **Frontend/backend technical:** `environment` and optionally `version_context`; explicitly separate standards, runtime behavior, and recommendations.
- **System design:** `scope`, `dimensions`, and body sections for clarifications, requirements, contracts/components, state/data, architecture, performance/scalability, reliability, security, accessibility where applicable, observability, testing, and tradeoffs.
- **Behavioral:** `competencies`; body includes prompt, probing questions, strong-evidence indicators, and red flags without prescribing one “correct” life story.

## Interview definition

Required fields: `id`, `title`, `type: interview`, `domain`, `level`, `duration_minutes`, `format`, `difficulty_distribution`, `skills`, and `status`. The body declares phases with budgets, mandatory and optional IDs, selection rules, scoring/evaluation model, interviewer and candidate behavior, timing adaptation, follow-ups, and completion criteria.

Question references use YAML lists inside fenced examples or body labels; the Markdown remains declarative. Every referenced ID must exist.

## Tip and cheatsheet

A tip uses `id`, `title`, `type: tip`, `domain`, `category`, `tags`, `status`, plus Content, When to Use, and Related Topics. A cheatsheet uses identity fields, audience/tags, compact tables or lists, pitfalls, and related content.

## Topic and study plan

Topics map prerequisites, concepts, questions, references, and next steps. Public study plans describe a reusable audience and schedule and link real content. Personalized schedules, targets, and results belong in `.personal/`.

## Session

Sessions are private and use `session_id`, `interview_id`, `started_at`, `expected_end_at`, `timezone`, and status. Timestamps are ISO 8601 with an explicit offset. A session records actual prompts, candidate responses, timing events, evidence, final evaluation, and follow-up topics. It never fabricates missing data.
