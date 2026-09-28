# Architecture

Interview Kit is a filesystem knowledge graph expressed in Markdown. Directories provide broad taxonomy, frontmatter provides machine-readable identity and classification, Markdown links provide navigation, and stable IDs let interview definitions reference questions even when files move.

## Layers

1. **Reusable public knowledge:** `questions/`, `tips/`, `cheatsheets/`, `topics/`, and `resources/`.
2. **Public orchestration:** `interviews/` declares sequences and selection rules without copying answers.
3. **Authoring contracts:** `templates/`, [the content model](content-model.md), and root `AGENTS.md`.
4. **AI interface:** `.opencode/` contains human-readable commands and agents; it is not a runtime.
5. **Private execution:** `.personal/` stores user-specific sessions and progress and is ignored by Git.

No database or generated index is authoritative. Content remains usable with a text editor offline. External links are references, not required dependencies.

## Growth model

Domains are semantic folders, not code modules. A new mobile or security track uses the shared ID/lifecycle/linking model and adds specialized fields only when valuable. At scale, contributors can work in separate domain/category paths while global IDs and review prevent collisions.

## Design invariants

- Reusable knowledge is Markdown with YAML frontmatter.
- IDs are stable and globally unique; paths may change.
- Interviews reference questions by ID; sessions reference interviews by ID.
- Public definitions contain no candidate history.
- Behavior is documented, never hidden in application logic.
- Relative links work in local clones and any future hosting location.
