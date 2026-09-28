# Interview Kit

Interview Kit is a Markdown-first, AI-assisted technical interview preparation system. It combines reusable questions, declarative interview plans, concise references, and private practice records—without an application, database, build step, or internet requirement.

The initial library emphasizes frontend engineering, algorithms, and frontend system design. Its schemas are domain-neutral so backend, mobile, cloud, security, and other tracks can grow alongside them.

> **License notice:** a license has not yet been selected. See [LICENSE.md](LICENSE.md) before redistributing or accepting contributions.

## Start here

1. Read [AGENTS.md](AGENTS.md) if you are an AI agent or content author.
2. Browse [questions/](questions/), [cheatsheets/](cheatsheets/), and [tips/](tips/).
3. Choose a reusable definition in [interviews/](interviews/), or ask OpenCode to run `/interview frontend intermediate 60`.
4. Create `.personal/` files from [templates/interview-session.md](templates/interview-session.md). Personal files are ignored by Git; only [.personal/README.md](.personal/README.md) is public.

## Repository map

| Area | Purpose |
| --- | --- |
| `questions/` | Reusable prompts, answers, hints, rubrics, and references |
| `interviews/` | Public, declarative compositions of question IDs |
| `topics/` | Concept maps and learning paths |
| `tips/`, `cheatsheets/` | Actionable advice and scannable references |
| `resources/study-plans/` | Public study plans that link to repository content |
| `templates/` | Authoritative content shapes |
| `docs/` | Architecture, authoring, interview, and privacy details |
| `.opencode/` | Markdown commands and specialized AI agents |
| `.personal/` | Git-ignored sessions, answers, plans, and progress |

## How interviews work

An interview definition is public and reusable; a session is one private execution. The AI reads a definition, records real local timestamps (with timezone), asks one question at a time, adapts optional sections to actual remaining time, and records evidence—not invented answers. See [the interview engine](docs/interview-engine.md).

```text
/help
/interview frontend senior 60
/question event loop
/hint frontend-js-event-loop-001
/study-plan 14 days frontend performance
```

Run `/help` inside OpenCode to see every project command and examples. All commands are also described in [docs/slash-commands.md](docs/slash-commands.md). OpenCode is helpful but optional: every file remains directly readable and editable.

## Add content

- Copy the closest template, use a kebab-case filename, and assign a globally unique stable ID.
- Search IDs, titles, and concepts before adding a question.
- Keep technical claims accurate and cite primary sources where useful.
- Use relative links and verify referenced question IDs.
- Never commit personal information or move it into public content without the user's explicit request.

See [CONTRIBUTING.md](CONTRIBUTING.md) and [docs/authoring.md](docs/authoring.md) for the full workflow.
