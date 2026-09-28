# Contributing

Thank you for improving Interview Kit. Read [AGENTS.md](AGENTS.md), even when authoring manually: it is the canonical operating manual.

> A project license has not yet been selected. Contributions should not be accepted publicly until [LICENSE.md](LICENSE.md) is replaced and contributors understand the chosen terms.

## Authoring workflow

1. Search existing IDs, titles, concepts, aliases, and related links. Extend or cross-link sufficiently similar material instead of duplicating it.
2. Read the relevant file in [templates/](templates/) and inspect nearby published examples.
3. Choose the semantic domain directory. New domains may be added without changing the shared schema.
4. Name files in descriptive kebab-case. IDs are globally unique, lower-case, stable, and domain-prefixed (for example `frontend-js-closure-001`). Never recycle an ID.
5. Complete required metadata and sections. Use `draft`, `review`, `published`, or `deprecated`; new unverified material starts as `draft` or `review`.
6. Use original wording. Cite primary sources when accuracy benefits; do not copy proprietary prompts or solutions.
7. Check relative links, references, interview question IDs, spelling, and YAML syntax.

## Content expectations

- **Questions:** clear prompt, useful expected answer, progressive hints, observable evaluation criteria, mistakes, follow-ups, related content, and references where applicable.
- **Tips:** concise, actionable, contextual—not generic motivation.
- **Cheatsheets:** scannable facts, contrasts, pitfalls, and small examples rather than essays.
- **Interviews:** declarative phases, real question IDs, timing priorities, competencies, and an explicit evaluation model.
- **New domains:** add a directory under the appropriate content roots and use the shared conceptual model. Domain-specific fields may extend, not contradict, the base fields.

Technical statements must distinguish specifications from implementation details and version-dependent behavior. Avoid absolutes when browsers, runtimes, frameworks, or companies vary. Deprecate useful outdated content with a reason and replacement link rather than deleting it.

## Public and private boundaries

Public files must contain reusable, non-personal knowledge only. Candidate answers, scores, employer plans, dates, recruiter details, notes, and histories belong in `.personal/`, which is ignored except for its README. **Never move personal content into public content unless the user explicitly asks.** Remove or anonymize personal examples before proposing public material.

## AI-assisted contributions

AI may help draft or review content, but generated content **must be reviewed by a human before publication**. Verify factual claims and references; do not cite a source the reviewer has not checked. AI agents must follow command safety and privacy rules in [AGENTS.md](AGENTS.md).

## Review checklist

- Unique stable ID, correct path and metadata
- Required sections present and substantive
- Original wording and accurate claims
- No duplicate concept better handled by an existing item
- Relative links resolve; question references exist
- No personal, secret, or company-confidential information
- Published status is justified by human review

For deeper guidance, see [the contribution guide](docs/contribution-guide.md).
