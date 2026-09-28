# Private workspace

This directory is the local, Git-ignored layer for one user's interview preparation. The repository functions without it. Only this README is intentionally tracked; `.gitignore` excludes everything else under `.personal/`.

Suggested local structure:

```text
.personal/
├── profile.md
├── goals.md
├── progress.md
├── sessions/
├── answers/
├── notes/
└── study-plans/
```

- `profile.md`: optional experience and target roles.
- `goals.md`: private outcomes, dates, or companies.
- `progress.md`: evidence-based strengths, gaps, and reviewed topics.
- `sessions/`: one file per interview execution, copied from [`templates/interview-session.md`](../templates/interview-session.md).
- `answers/`, `notes/`: candidate work and reflections.
- `study-plans/`: personalized plans created by `/study-plan`.

Sessions preserve actual `started_at` and `expected_end_at` ISO 8601 timestamps with timezone offset. They may contain candidate answers and evaluations and must never be stored in public `interviews/`. Avoid secrets even here; Git ignore is protection from accidental commits, not encryption or access control.

**Never move personal content into public content unless the user explicitly asks.** Before sharing any derived lesson publicly, remove identity, employer, recruiter, date, and confidential interview details.
