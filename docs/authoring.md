# Authoring guide

## Before writing

Read `AGENTS.md`, select the closest template, and inspect two nearby examples. Search by ID, title, synonyms, and underlying concept. Prefer improving an existing item over creating a near duplicate.

## Write for interviews

Make prompts self-contained and scoped to the time estimate. Expected answers should explain why, not merely list terms. Hints progress from framing to stronger guidance. Rubrics describe observable evidence and accept valid alternatives. Include practical edge cases and realistic follow-ups.

Use original wording. For technical claims, prefer primary sources and note relevant standards, runtime, browser, or version context. Distinguish guaranteed behavior from common implementation and recommendations from facts.

## Paths, IDs, and links

Use descriptive kebab-case filenames. Keep IDs stable forever and globally unique. Use relative Markdown links so local clones work. Interview definitions list stable IDs and may include relative links for navigation.

## Status

- `draft`: incomplete or not fact-checked.
- `review`: complete draft awaiting human technical review.
- `published`: reviewed and ready to use.
- `deprecated`: retained for history; state reason and replacement.

AI-created material must not jump directly to `published` without human review. See [the content model](content-model.md) and [contribution guide](contribution-guide.md).
