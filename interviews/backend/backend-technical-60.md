---
id: backend-technical-senior-60
title: "Backend Technical — Senior — 60 Minutes"
type: interview
domain: backend
level: senior
duration_minutes: 60
format: conversational technical interview
difficulty_distribution:
  senior: 6
skills:
  - distributed-systems
  - data
  - reliability
  - operations
status: review
---

# Purpose

Demonstrate that the shared architecture supports backend depth without changing the content model.

# Question Selection

## Mandatory question IDs

- `backend-distributed-idempotency-001`
- `backend-performance-caching-001`
- `system-design-backend-jobs-001`

## Optional question IDs

- `backend-distributed-consistency-001`
- `backend-data-transactions-001`
- `system-design-backend-rate-limiter-001`

Use mandatory questions in listed competency order. Select optional questions only when time and candidate responses permit. A same-skill substitution is allowed when the candidate has recently seen an item, but the replacement ID must exist and be recorded in the private session.

# Interview Structure

## Phase 1 — Introduction (5 minutes)

Use this phase to gather evidence for the declared competencies; transition naturally when its actual-time budget ends.

## Phase 2 — Correctness and failure semantics (15 minutes)

Use this phase to gather evidence for the declared competencies; transition naturally when its actual-time budget ends.

## Phase 3 — Data and caching (12 minutes)

Use this phase to gather evidence for the declared competencies; transition naturally when its actual-time budget ends.

## Phase 4 — System design (20 minutes)

Use this phase to gather evidence for the declared competencies; transition naturally when its actual-time budget ends.

## Phase 5 — Follow-ups (5 minutes)

Use this phase to gather evidence for the declared competencies; transition naturally when its actual-time budget ends.

## Phase 6 — Close (3 minutes)

Use this phase to gather evidence for the declared competencies; transition naturally when its actual-time budget ends.

# Evaluation Model

Rate each observed competency as **strong evidence**, **adequate evidence**, **partial evidence**, or **insufficient evidence**. Judge correctness, depth, reasoning, problem solving, communication, and tradeoffs; add performance, security, accessibility, testing, or system thinking only where relevant. Insufficient evidence means not demonstrated in this session. No numeric aggregate is defined.

# Interviewer Behavior

Ask one primary question at a time. Let the candidate reason; clarify without solving. Give a progressive hint only on request or after an explicitly acknowledged stall. Do not expose answers or rubric internals during the evaluation. Follow actual candidate evidence rather than a fixed script.

# Candidate Expectations

Clarify assumptions, explain choices, test reasoning, and discuss tradeoffs. A candidate may request a hint and should state uncertainty rather than fabricate facts.

# Timing and Adaptation

Capture real local `started_at` and calculated `expected_end_at` with timezone offset. Re-check the clock at every phase boundary and before any remaining-time statement. Never estimate from message count. Preserve mandatory competencies, shorten follow-ups and omit optional questions when behind, avoid starting work that cannot finish, and reserve the final phase. If clock access fails, state that timing cannot be verified.

# Follow-up Policy

Use follow-ups from the question only when they probe an observed answer or required depth. Prefer one discriminating follow-up over broad trivia. Record hints because they affect evidence interpretation.

# Completion Criteria

Finish when actual duration is reached or all mandatory competencies have enough evidence and the candidate has had closing time. Provide strengths, gaps, evidence limitations, review topics, and actionable next steps. Store all user-specific results only under `.personal/`.
