---
description: Show all Interview Kit slash commands and examples
---

Show the Interview Kit command reference below. Keep every command in the response. If `$ARGUMENTS` names a command, show the complete list first, then add a short focused explanation and examples for that command. Do not create or modify repository content.

# Interview Kit commands

## Practice and learning

- `/interview [domain] [level] [minutes]` — Start a realistic, time-aware interview from a repository definition. Examples: `/interview`, `/interview frontend senior 60`, `/interview system-design senior 45`.
- `/question <query>` — Find a repository question and optionally explain it. Examples: `/question event loop`, `/question binary search`.
- `/hint <question-id>` — Reveal only the next progressive hint without giving away the complete answer. Example: `/hint frontend-js-event-loop-001`.
- `/explain <topic>` — Explain a topic at interview depth using existing repository content. Examples: `/explain closures`, `/explain browser rendering`.
- `/evaluate <question/session and answer>` — Evaluate an answer from the current context, a question plus answer, or a private session reference. Example: `/evaluate frontend-js-closures-001 "My answer..."`.

## Study and progress

- `/study-plan <goal and period>` — Create a personalized study plan under `.personal/study-plans/` by default. Example: `/study-plan 14 days frontend performance`.
- `/progress` — Summarize evidence from private `.personal/` progress and sessions without exposing it publicly.
- `/tip <query>` — Find an existing interview tip or safely draft one when requested. Examples: `/tip communication`, `/tip system design`.
- `/cheatsheet <topic>` — Retrieve an existing scan-first cheatsheet or safely create one when requested. Examples: `/cheatsheet javascript`, `/cheatsheet browser rendering`.

## Content authoring

- `/add-question <description>` — Create a complete, non-duplicate question from the correct template. Example: `/add-question intermediate frontend question about WebSocket reconnection`.
- `/add-topic <domain> <topic>` — Create a topic learning map that links existing repository material. Example: `/add-topic frontend web security`.
- `/generate-interview <domain> <level> <minutes> [focus]` — Create a reusable public interview definition referencing real question IDs. Example: `/generate-interview frontend senior 60 performance`.

## Review and maintenance

- `/review [path or current content]` — Review targeted content for metadata, accuracy, links, duplication, references, and privacy. Example: `/review questions/frontend/javascript/event-loop.md`.
- `/audit-content` — Run a repository-wide content, schema, reference, timing, and privacy audit.
- `/help [command]` — Show this complete command list. Optionally request more detail for one command. Examples: `/help`, `/help interview`.

Remind the user that commands which create content follow `AGENTS.md`, inspect templates and nearby examples, prevent duplicates, validate metadata and links, and preserve the public/private boundary.
