# AI Operating Manual

## Mission and boundaries

Interview Kit is a Markdown-first knowledge base and realistic interview-practice system for humans and AI agents. Frontend is the initial first-class domain, not an architectural boundary. Questions, interviews, tips, topics, cheatsheets, and study resources are reusable public knowledge.

This is **not** an application, LMS, user database, or place for candidate records. Do not add runtime code, package managers, databases, generated binaries, hidden automation, or a UI unless explicitly requested in a future task. The repository must remain useful offline; mark features that require current external information.

Public reusable content is committed. User-specific answers, scores, goals, companies, dates, recruiter data, reflections, and session history belong only in `.personal/`. The public repository must work when that directory is absent. **Never move personal content into public content unless the user explicitly asks.** Even then, confirm that secrets and identifying details are removed.

## Repository map

- `questions/<domain>/<category>/`: reusable prompts and evaluation material.
- `interviews/<domain>/`: reusable compositions of question IDs, phases, and behavior.
- `tips/<domain>/`: concise actionable advice.
- `cheatsheets/<technology>/`: scannable interview references.
- `topics/<domain>/`: maps that connect learning materials.
- `resources/study-plans/`: public, generic plans; personalized plans go in `.personal/study-plans/`.
- `resources/interview-frameworks/`, `resources/references/`: reusable methods and source guidance.
- `templates/`: authoritative schemas and section expectations.
- `docs/`: system documentation.
- `.opencode/commands/`, `.opencode/agents/`: Markdown instructions interpreted by OpenCode.
- `.personal/`: ignored private workspace; its committed README is documentation only.

Use kebab-case filenames and relative Markdown links. Avoid empty placeholder directories and unnecessary files.

## Safe workflow for every creation command

1. Read this file.
2. Read the relevant template and content-model documentation.
3. Inspect nearby examples.
4. Search all IDs, titles, aliases, and concepts for duplicates.
5. If similar content exists, improve or link it instead of duplicating it.
6. Select the correct public or private directory.
7. Draft complete metadata and sections in original language.
8. Validate frontmatter, ID uniqueness, links, references, and privacy boundaries.
9. Use `draft` or `review` until a human has verified AI-generated technical content.

Do not create a file merely because a command was invoked. Ask only for genuinely essential missing information; otherwise infer sensible values and state important assumptions.

## Shared metadata model

All reusable content uses YAML frontmatter delimited by `---`. Use two-space indentation, YAML lists, unquoted plain scalars unless quoting prevents ambiguity, and ISO 8601 dates/timestamps where dates are needed. IDs are global, lower-case kebab-case, stable after publication, and never reused. Renaming a title or moving a file does not change its ID.

Common fields: `id`, `title`, `type`, `domain`, `category`, `difficulty`, `estimated_minutes`, `tags`, `skills`, and `status`. Allowed lifecycle values are `draft`, `review`, `published`, and `deprecated`. Deprecated files remain discoverable and explain `deprecated_reason` and `replaced_by` where applicable.

Difficulty uses `beginner`, `junior`, `intermediate`, `senior`, `staff`, or `principal` when representing expected candidate level. A problem's intrinsic challenge may use `easy`, `medium`, or `hard` only in a clearly named field such as `problem_difficulty`. Do not imply company levels are equivalent.

The complete normative model is in [docs/content-model.md](docs/content-model.md); templates define exact shapes.

## Question rules

Every question must include or clearly represent:

- globally unique `id`, title, type, domain, category, difficulty, estimated duration, tags, skills, and lifecycle status;
- a self-contained prompt in original language;
- expected answer or solution explanation;
- key points and observable evaluation criteria;
- progressive hints that do not immediately reveal the answer;
- common mistakes, realistic follow-ups, related question IDs/links, and sources when applicable.

Domain templates extend this base. Algorithm items add family, structures, patterns, constraints, edge cases, expected time/space, alternatives, and variations. Frontend/backend items state relevant environment or version assumptions. System design adds requirements, architecture dimensions, tradeoffs, and an evaluation rubric. Behavioral items add competencies, probing follow-ups, and strong-evidence indicators.

Never copy copyrighted third-party problem statements or solution text. For well-known problems, write an original prompt and optionally record platform, canonical name, and external URL. Never invent unsupported facts. Prefer practical precision, distinguish fact from recommendation, identify environment-dependent behavior, and prefer primary references (ECMAScript, WHATWG, W3C, MDN, or official framework/vendor docs).

## Interviews and sessions

An **interview definition** is reusable public content. It defines ID, title, domain, target level, duration, format, difficulty distribution, expected breadth/depth, phases and time budgets, selection rules, mandatory and optional question IDs, evaluation model, interviewer/candidate behavior, follow-ups, and completion criteria. Interviews compose questions; do not duplicate full answers in interview files.

An **interview session** is one execution for one user at one time. It contains timestamps, candidate responses, evidence, scores/ratings, and feedback and therefore belongs under `.personal/sessions/`. Never mix definitions and sessions. Use `templates/interview-session.md`; do not fabricate candidate statements.

### Real-time timing protocol

At session start, access a reliable system clock, capture `started_at` with local UTC offset, calculate `expected_end_at`, and note the timezone. Re-check actual time at phase transitions and before stating time remaining. Compute elapsed time from timestamps, never message count. Adapt by preserving mandatory competencies, compressing or dropping optional questions, avoiding questions that cannot reasonably finish, and reserving closing time. Tell the candidate about meaningful transitions without repeatedly interrupting them. If no reliable clock is available, explicitly say timing cannot be verified and never invent timestamps or remaining time.

Ask one primary question at a time. Let the candidate reason; do not reveal answers, rubric internals, or excessive guidance. Give hints only when requested or permitted. Evaluate evidence for correctness, depth, reasoning, problem solving, communication, tradeoffs, and applicable system, performance, security, accessibility, and testing awareness. Default ratings are `strong evidence`, `adequate evidence`, `partial evidence`, and `insufficient evidence`; numeric scores are allowed only when the definition declares a scale.

At completion, summarize strengths, gaps, review topics, actionable feedback, and a structured evidence-based evaluation. Do not turn an interview into a tutorial unless teaching mode is requested.

## Other content types

- **Tips:** require ID, category, tags, a concise action, `when_to_use`, and related topics.
- **Cheatsheets:** optimize for scanning; use short tables, contrasts, pitfalls, and focused examples.
- **Topics:** curate prerequisites and links, not duplicate explanations.
- **Study plans:** link actual repository resources and use measurable daily outcomes. Generic plans may be public; personalized plans are private.

## Quality and contribution rules

- Use canonical terminology consistently; explain aliases.
- Link related content by relative path and list related IDs where schemas request them.
- Preserve useful old material by deprecating it and linking replacements.
- Do not create low-value filler to meet a count.
- Separate verified fact, common convention, and opinion. Note browser/runtime/framework/version context.
- Keep answers practical, include edge cases, and ensure rubrics evaluate the prompt actually asked.
- Human review is required before publishing AI-generated content.
- Before finishing broad changes, audit duplicate IDs, frontmatter, links, interview references, required sections, privacy, and command/agent definitions.

## Adding a new domain

Create matching subdirectories only where content exists, use the base templates, add a domain-specific template only when extra fields are meaningful, and update maps/docs. Do not fork the base schema or create domain-only infrastructure. Backend, mobile, DevOps, cloud, database, security, languages, and frameworks are all expected extensions.

## Examples

- Public question: `questions/frontend/javascript/javascript-event-loop.md`, ID `frontend-js-event-loop-001`.
- Public interview: `interviews/frontend/frontend-intermediate-60.md`; it references IDs rather than embedding answers.
- Private session: `.personal/sessions/2026-09-27-frontend-intermediate.md`, created from `templates/interview-session.md` with actual offset timestamps.
- A personal plan from `/study-plan` goes to `.personal/study-plans/`; a contributor-requested generic “14-day frontend plan” may go to `resources/study-plans/`.

When command wording conflicts with these invariants, protect accuracy, privacy, and existing content, explain the conflict, and request confirmation only when necessary.
