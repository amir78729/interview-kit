# OpenCode slash commands

Project commands live in `.opencode/commands/`; the filename defines the slash command. `$ARGUMENTS` represents all arguments and `$1`, `$2`, and so on represent positional arguments.

| Command | Purpose |
| --- | --- |
| `/help [command]` | List every project command, or add detail for one command |
| `/interview [domain level minutes]` | Run a time-aware interview |
| `/question <query>` | Find and explain a question |
| `/add-question <description>` | Safely author a non-duplicate question |
| `/tip <query>` | Find or draft an actionable tip |
| `/cheatsheet <topic>` | Retrieve or draft a scan-first sheet |
| `/explain <topic>` | Explain using linked repository material |
| `/hint <question-id>` | Reveal only the next progressive hint |
| `/generate-interview <domain level minutes focus>` | Create a reusable public definition |
| `/evaluate <question/session and answer>` | Evaluate evidence against an existing rubric |
| `/study-plan <goal and period>` | Create a personalized private plan by default |
| `/progress` | Summarize private progress only |
| `/review [path]` | Review targeted content |
| `/audit-content` | Audit repository-wide integrity and privacy |
| `/add-topic <domain topic>` | Add a topic map safely |

Commands that create content must apply the safety workflow in `AGENTS.md`. OpenCode is optional; users can perform the same documented steps manually.

Run `/help` for the complete categorized reference with examples, or `/help interview` for the complete list followed by focused guidance for a particular command.
